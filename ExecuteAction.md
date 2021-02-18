1. 
Name: ExecuteAction (EA)


2. 
Description: Executes a special action.


3. 
Parameters:


a. 
Action
     A number indicating what action should be executed. Range is from 1 to 10.


b. 
Action value
     A value to pass to the action. Can be numbers or text.


4. 
Examples:
```json
ExecuteAction:[3|"Autopsy Report"];

EA:[9|"Trucy"];
```

 



5. 
Remarks:

> Most of the actions will not be necessary for you. You probably only need action 3 and 4 and action 9 and 10. The rest is covered through other instructions.
> 
 

Detail descriptions of the actions:


1. 

GetId

Only for internal use. 

 



2. 

DisplayEvidence

Displays a piece of evidence in the top left corner. It's recommended to use the DisplayEvidence instruction instead.

 



3. 

RevealFromRecord

Reveals a piece of evidence from the court record which was hidden before. Pass the name or the ID of the evidence you want to to reveal as the value parameter.

 



4. 

HideFromRecord

Hide a revealed piece of evidence from the court record. Pass the name or the ID of the evidence you want to hide as the value parameter.

 



5. 

DecreaseHealth

Decreases the health. It's recommended to use the DecreaseHealth instruction instead.

 



6. 

IncreaseHealth

Increases the health. It's recommended to use the IncreaseHealth instruction instead.

 



7. 

DisplayHealthBar

Displays the health bar in the top right corner. It's recommended to use the DisplayHealth instruction instead.

 



8. 

PickEvidence

Only for internal use.

 



9. 

RevealPerson

Reveal a hidden person profile from the record. Pass the name or the ID of the person you want to reveal as the value parameter.

 



10. 

HidePerson

Hide a revealed person profile from the record. Pass the name or the ID of the person you want to hide as the value parameter.
