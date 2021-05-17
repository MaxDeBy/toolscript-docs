[Back to overview](index.md)

---
# LoadScene
---
- **Name:** LoadScene (LS)
- **Description:** The LoadScene instruction updates the background AND the character. It also removes a popup if the background changes.
- **Parameters:**
  - **Stagename:**  
    The name of the background that you want to display. This can be either the actual name you entered in the tool UI or the ID of the background.
    You can pass an empty argument by using a null character (-) to not change the background. But this will also not remove a popup if one is displayed.

  - **Character name:**  
    The name of the character you want to display. This can be either the actual name you entered in the tool UI or the ID of the character.
    You can pass an empty argument by usinga  null character (-) to not load a character.

  - **Emote name:**  
    The name of the emote that the character should use. This can be either the actual name you entered in the tool UI or the ID of the emote.
    You **cannot** leave this argument empty. It will be ignored however, if you left the character name empty. So if you did, then you also can use a null character (-) for this 	parameter.

  - **Play pre:**  
    A boolean value indicating whether the preanimation of this emote should be played or not. Use `true` or `false`, `true` meaning the preanimation will be played.

  - **Wait for pre:**  
    A boolean value indicating whether the engine should wait for the pre animation to wait before continuing with the next line. Use `true` or `false`, `true` meaning that the engine will wait.

  - **Character position (optional):**  
    The position of the character.

- Example:
```
1:  LoadScene:["Defense"|"Athena"|"Thinking"|false|false];
2:  LoadScene:[-|"Phoenix"|"Point"|true|true];
3:  LoadScene:["WitnessStand"|-|-|false|false];
4:  LoadScene:["WitnessStand"|-|-|false|false|"Center"];
5:  LoadScene:["JudgeBench"];
6:  LS:["Agency"];
```
- Remarks:
> If you just want to load a scene without loading a character, you can shorten the parameters. In that case you can just use the Stagename parameter as shown as in the last example. All the character parameters can be omitted.
> 
> There are 3 character positions: `Right`, `Left` and `Center`.  
> Although, they can be combined. Valid position combinations are: `RightLeft`, `RightCenter`, `LeftCenter` and `All`.
> 
> This counts for all instructions that use character positions. When omitted or invalid, the default value is `Center`.

---
[Back to overview](index.md)
