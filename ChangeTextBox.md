[Back to overview](index.md)

---
# ChangeTextBox
---
- **Name:** ChangeTextBox (CTB)
- **Description:** Changes what custom textbox should be used.
- **Parameters:** 
  - **Name:**      
    The name of the image (without file extension) of the textbox.

- Examples:
```
1:  ChangeTextBox:["Dual Destinies"];
2:  CTB:[-];
```
- Remarks:
> This option permanently changes the textbox, so you only have to call it once, for example at the beginning of the script.  
If you pass the null character (-) the textbox will be changed to the default style again.  
To use an image, you have to save it in the "UI" folder of the theme you wish to use.  
If your textbox also has a version without the namebox, add the image with the same name + "_NoName".

---
[Back to overview](index.md)