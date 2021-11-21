[Back to overview](index.md)

---
# Shake
---
- **Name:** Shake
- **Description:** Shakes the screen with a specified intensity and duration.
- **Parameters:**
  - **Intensity:**  
    The intensity of the shaking. Must be a value between 0-255.
  - **Duration:**  
    The duration of the shaking in miliseconds. Must be a value between 10-65535.

- Examples:
```
1:  Shake:[20|5000];
```

- Remarks
> Shaking effect is only applied to the camera layers. Every other layer remains still during a shake effect.
> Shaking is an asynchronous effect, meaning the engine will not wait for it to finish before continuing.
>  
> Since AACT is a 2D engine, a "camera" in traditional sense does not exist. Instead, camera here refers to an element that will affect its children. The children can be configured via themes.
> Only those children will be affected by this instruction.

---
[Back to overview](index.md)