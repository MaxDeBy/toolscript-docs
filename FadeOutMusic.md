[Back to overview](index.md)

---
# FadeOutMusic
---
- **Name:** FadeOutMusic (FoutM)
- **Description:** Fades out the currently playing music.
- **Parameters:**
  - **Delay:**  
     The amount of miliseconds it takes to fade out the scene.

- Examples:
```
1:  FadeOutMusic:[1000];
2:  FoutM:[-];
```

- Remarks:
> 
If you pass an empty parameter as delay, it will default to one second (1000 miliseconds).  
After the music has faded out, it has not stopped. It is still "playing", just not audibly.

---
[Back to overview](index.md)