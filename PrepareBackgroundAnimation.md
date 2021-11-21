[Back to overview](index.md)

---
# PrepareBackgroundAnimation (PrepareBackAnim)
---
### Description
Prepares an animated background to be played at a later point.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Name|String|The filename of the animation, without the file extension.|✓|-|
|Loop|Boolean|Whether or not the animation should loop.|✗|true|

### Examples:
#### Example #1: Prepares the animation 'CaseIntro' and specify it should not loop.
```
1:  PrepareBackgroundAnimation:["CaseIntro"|false];
```

#### Example #1: Prepares the animation 'Perceive' and specify it should loop.
```
1:  PrepareBackAnim:["Perceive"|true];
```

### Remarks:
The file for the specified animation has to be within the "Misc" folder which can be found under Assets>Images>Misc. The file must be a GIF or animated PNG file.

During the beta, it was not necessary to prepare background animations. However, with the full release, the way animations are played was changed. Animations are no longer rendered on-the-fly, but instead pre-loaded before displayed. There have been systems implemented that will start loading an animation before it's needed, 
to ensure there are no wait times for character animations. However, animated backgrounds are not predicted and thus need to be prepared manually.  

If not prepared, the animated backgrounds would have a very noticable delay before being played, if you try to start them at the same time as a [LoadCharacter](LoadCharacter.md), for example.

After being prepared, you can start an animated background instantly by calling [PlayBackgroundAnimation](PlayBackgroundAnimation.md). Make sure to prepare the animation early enough to not experience any delays when playing.

---
[Back to overview](index.md)