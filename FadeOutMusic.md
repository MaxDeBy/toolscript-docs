1. 
Name: FadeOutMusic (FoutM)


2. 
Description: Fades out the currently playing music.


3. 
Parameters:


a. 
Delay
     The amount of miliseconds it takes to fade out the scene.


4. 
Examples:
```json
FadeOutMusic:[1000];

FoutM:[-];
```

 



5. 
Remarks:

> If you pass an empty parameter as delay, it will default to one second (1000 miliseconds).
> 
> After the music has faded out, it has not stopped. It is still "playing", just not audibly.