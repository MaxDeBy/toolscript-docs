[Back to overview](index.md)

---
# PanCamera
---
- **Name:** PanCamera (Cam)
- **Description:** Pans the camera to a different spot of the current super location.
- **Parameters:**
  - **Position X:**  
    The destination position of the camera on the X axis of the background image. The value describes the leftmost pixel which should be visible.
  - **Position Y:**  
    The destination position of the camera on the Y axis of the background image. The value describes the topmost pixel which should be visible.
  - **Duration: (optional)**  
    The time in miliseconds the panning should take.
  - **Linear: (optional)**  
    Whether the panning should occurr with a consistent speed or ease in and out.
  - **Wait: (optional)**  
    Whether or not the engine should wait until the panning has been completed before continuing.

- Examples:
```
1:  PanCamera:[1200|400|2000|true|true];
2:  PanCamera:[640|-|500|false];
3:  Cam:[1280|720];
```

- Remarks
> Super locations are locations that extent beyond the screen dimensions, on both the X and the Y axis. Background and/or foreground image can be bigger than the screensize and will be displayed without resizing.  
> Characters can be set on any position, regardless if the current location is a super location or not. See more under [LoadCharacter](LoadCharacter.md).
>  
> Since AACT is a 2D engine, a "camera" in traditional sense does not exist. Instead, camera here refers to an element that will affect its children. The children can be configured via themes. This instruction, however, is independant from the setup in themes.
> 
> This instruction fades out the dialog box before starting the panning.
>
> This instruction will automatically move all characters on the screen as well.

---
[Back to overview](index.md)