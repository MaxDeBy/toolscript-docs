1. 
Name: SoundPause


2. 
Description: A second way of pausing for a little. Instead of using miliseconds, you can input the name of a sound effect, and the engine will wait until the sound effect's full duration has passed before it proceeds.


3. 
Parameters:


a. 
Sound name
The name of the soundeffect which length should be waited for.


4. 
Examples:
```json
SoundPause:["Deskslam"];
```

 



5. 
Remarks:

> The engine will wait, regardless if the sound is actually played or not.