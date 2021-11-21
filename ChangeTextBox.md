[Back to overview](index.md)

---
# ChangeTextBox (CTB)
---
### Description
Changes the textbox to use custom images in the "UI" folder.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Name|String|The file name without file extension.|✓|-|

### Examples:
#### Example #1: Changing the custom textbox visuals to a custom file called "Dual Destinies.png" in the "UI" folder.
```
1:  ...
2:  ChangeTextBox:["Dual Destinies"];
3:  ...
```

#### Example #2: Resetting the custom visuals.
```
1:  ...
2:  CTB:[-];
3:  ...
```

### Remarks:
This option permanently changes the textbox, so you only have to call it once, for example at the beginning of the script. 
If you pass the null character (-) the textbox will be changed to the default style again. 
To use an image, you have to save it in the "UI" folder of the theme you wish to use.  
If your textbox also has a version without the namebox, add the image with the same name + "_NoName".

You can specify a textbox directly in the Theme, as well.

---
[Back to overview](index.md)