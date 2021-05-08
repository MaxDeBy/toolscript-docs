Investigations are the biggest and most complex feature, so make sure to read the following article carefully to avoid mistakes while using them and prevent unexpected behaviour.

Investigations are annoying to set up as there are many parts, but that's also a bonus. There are a lot of interactions you can set up for a good and "close-to-original" experience.

Let's take a look at the basic script that template is created when using autocomplete.
![](https://www.debygames.com/aacs/drex_investigation__c__custom.png)

As you can see, an investigation consists of 6 container instructions: FirstEntrance, SecondEntrance, Talking, Moving, Presenting and Examining.

(Fun fact, these aren't container instructions. They actually don't exist. They're only there to make it easier to parse the script.)

Moving, talking, presenting, and examining will be documented in further detail in the chapters below. This page contains information on entrances, how investigations work in the background, and the best practices when creating investigations.

FirstEntrance contains regular instructions that are executed on the first ever entrance to an investigation sequence. Use this for the green typewriter describing time and place, or for whatever else you might want to do in there.

SecondEntrance contains regular instructions that will be executed on every entrance to an investigation sequence, including the first one. Use this to set the background and the character on entrance. Be aware that FirstEntrance will be executed BEFORE SecondEntrance (and no, the position in the script doesn't matter).

Now, why is it important to know about how investigations work in the background? Easy: because they may take up more RAM than necessary if done wrong. An investigation will wait until it's finished to release the RAM it occupies, and it never ends automatically under any circumstance (Exception being the engine crashes). The only way to end an investigation manually is through the FinishInvestigation instruction. Furthermore, investigations are parallel processes, meaning that they run in the background almost independent from the engine itself. This processing requires CPU usage, and, although very small, the effects can be noticed. The problem is that if you execute a PlayInvestigation instruction for an investigation you have not yet finished, you will create a completely new sequence. Obviously stuff like first entrance won't be called, but now there are two processes of the same investigation, but only one of them can actually be controlled. In short, it is wasting CPU usage, RAM space, and there is a chance the engine will ultimately crash because the thread pool can only hold so many threads. 

How to avoid all that chaos? That and more will be explained by the following best practices:

- Execute a frame when entering an investigation sequence that finishes all investigations that the player can come from. Alternatively, you can swap the PlayInvestigation instruction from the Moving hybrid instruction with a PlayFrame instruction that executes a PlayInvestigation followed by a FinishInvestigation of the last investigation.


- If you want multiple investigations (locations) in one sequence use the StartInvestigation instruction and enter the ID of the first investigation as parameter. This instruction will execute that investigation and wait until every investigation sequence has been finished, even the ones that are not actually part of the current investigation section. You can simply use the FinishAllInvestigation instruction to easily end all sequences with one single instruction and thus move on from the StartInvestigation Instruction.

- Create as few investigations as possible. If you have gathered a piece of evidence that, for example, unlocks a new topic to talk about with a character, do not create a new investigation for that. Instead, the best thing would be to have one investigation per location. Make use of the ability to hide and reveal topics and locations.

- If you don't want a certain option (examining, talking, etc.) to be available in one investigation sequence, leave the corresponding container empty. The button for that action will be invisible then.

And now for the actual interactions in the investigation, choose from the topics below:

<span style="color: blue"> The contents of Investigation (C) </span>