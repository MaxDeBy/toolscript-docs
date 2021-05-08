[Back to overview](index.md)

---
# ToolScript Best Practices
---
AACS is not a real scripting language, but there are still best practices you should follow in order make it easier to read, edit, and maintain. Following are a list of best practices you should consider doing:

1. Use frames only when necessary. Frames are required when you want to execute a lot of instructions withing a single instruction. They are not meant for the main script. Use the Break instruction if you need the player's consent to continue.

2. Don't overdo it with recursive calls. Sometimes it is required for a frame to call itself again. For example, when you leave the player with a choice, and the player can choose a "wrong option" which eventually goes back to said choice. While in general it is not considered bad practice to use recursive calls in AACS, it is best to minimize it.  
Consider using [Branch Instructions](Branch-Instructions.md) instead.

3. Don't write everything in one script. Split up your scripts. For example, one script containing all the frames that will be used in a specific Cross Examination and then another script containing the actual cross examination and then *another* script which contains the main string of scripts. Splitting up your script into different modules helps maintaining your project more easily if you happen to write a very long script.

4. Frames and other Container Instructions don't require you to use numbers as ID. If you choose to do so, keep spaces between the IDs. If you use Frames for Cross Examinations, Investigations, or other Instructions, keep spaces between them. It is wise to reserve at least 10 IDs in advance. For example, your first Cross Examinations uses 4 Frames, with the IDs 10, 11, 12, and 13. Now, reserve IDs from 14 to 23. If you need to go back to edit this cross examination because you want to add statements or other sequences, you now have some IDs left that are close to the initial frames. This makes it easier to read and understand what a frame is used for. It is hard to maintain a script if you have a cross examinations with the frames, 10, 11, 12, 13, 27, 36, 55 and 24. Of course, even better is not using numbers at all and instead use meaningful text IDs.

5. AACS can be very forgiving. For example, technically it doesn't matter what kind of brackets you use, most of the time. For example, a Branch Instruction works perfectly well with \{\} brackets. And a hybrid can absolutely use \(\). You can even switch the <> brackets for another kind. But this possibility should not actually be exploited. It's best to use the brackets as intended (<> for Frames, \{\} for Hybrids and \(\) for Branches). The behaviour of the script parser can change with every update, possibly breaking non-standard behaviour.

---
[Back to overview](index.md)