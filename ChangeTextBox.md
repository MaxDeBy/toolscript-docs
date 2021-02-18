1. Name: ChangeTextBox (CTB)
2. Description: Changes what custom textbox should be used.
3. Parameters:
  
    a. Name
    
    The name of the image (without file extension) of the textbox.
4. Examples:
```json
ChangeTextBox:["Dual Destinies"];
CTB:[-];
```
5. Remarks:
> This option permanently changes the textbox, so you only have to call it once (for example at the beginning of the script).
> If you pass the null character (-) the textbox will be changed to the default style again.
>  
> To use an image, you have to save it in the "Misc" folder under Assets>Images. If your textbox also has a version without the namebox, add the image with the same name + "_NoName".