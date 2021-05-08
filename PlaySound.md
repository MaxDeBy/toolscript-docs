1. Name: PlaySound (PS)


2. Description: This instruction plays a sound effect.


3. Parameters:


a. 
Sound name
The name of the sound effect that should be played.


b. 
Delay
The amount of miliseconds the engine should wait before playing. For example to sync up a deskslam sound with the animation.


c. 
Loop (optional)
A boolean value determining if the sound should loop.


d. 
Loop delay (optional)
A delay between each loop.


e. 
Loop length (optional)
If greater than 0, AACT will loop the sound after this many miliseconds. If this is set to 0, AACT will loop the sound after it finished playing.
 


4. 
Examples:
```json
PlaySound:["Deskslam"|600];

PS:["GavelSlam"|300];

PlaySound:["Clap"|0|true|100|0];

PS:["Chalkboard"|20|false|0|30];

```
 



5. 
Remarks:

> If you don't want the sound to loop, you can omit the 3rd and 4th parameter.