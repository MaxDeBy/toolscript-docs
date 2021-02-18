1. Name: DisplayPopup (DP)



2. Description: This instruction displays a popup image.


3. Parameters:


a. 
Popup name
The name of the popup that should be displayed.


b. 
Looping (optional)
A boolean value determining if the popup should loop or not.
 

4. Examples:
```json
DisplayPopup:["HoldIt"];

DP:["Objection"];

DisplayPopup:["Testimony"|true];

DP:["TakeThat"|false];
```

 



5. 
Remarks:

> The popup will not vanish until the background changed.
> 
> If you don't want the popup to loop, you can omit the last parameter.