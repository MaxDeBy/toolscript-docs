1. Name: Presenting

2. Description: Presenting refers to the action of showing a person a piece of evidence outside of court in order to elicit dialogue or progress the story. There are 4 different types of presenting: Evidence, Profile, DefaultEvidence and DefaultProfile. For each piece of evidence you want to be display you use Evidence, and for each profile you wish to display you use Profile. All other pieces of evidence or profiles are covered through the DefaultEvidence or DefaultProfile, which will be executed when a piece or profile is shown that isn't covered throughan Evidence or Profile instruction (for irrelevant evidence and profiles).

A presenting instruction is built like the following scheme:
```json
TYPE:{NAME|FIRST PRESENT|SECOND PRESENT};
```

3. Parameters

    a. Type
    
    Determines the object being presented. Can be either "Evidence" or "Profile"
    
    b. Name
    
    The name of the evidence or the profile that can be presented.

    c. First Present

    A regular instruction that is executed the first time a piece of evidence or profile is presented.

    d. Second Present
    
    A regular instruction that is executed every additional time a piece of evidence or profile is presented.


4. Examples:
>None

5. Remarks
>TYPE can also be "DefaultEvidence" or "DefaultProfile"; however, in that case the hybrid has only one parameter: a regular instruction that gets executed when a piece of evidence or a profile is presented that is not covered by another present instruction. You can define as many DefaultEvidence or DefaultProfile instructions as you want but only the first one of each will be used.
Example: 
>```
DefaultEvidence:{PlayFrame:[12]};