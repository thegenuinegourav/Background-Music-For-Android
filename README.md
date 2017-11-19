# Background-Music-For-Android  
An Android App that shows how to add background music in your android app using MediaPlayer class.  
  
Can be used for long clips in Game Development.  
  
Demo Video on [Youtube](https://www.youtube.com/watch?v=s67KnuSd3Js)  
  
## MediaPlayer Vs SoundPool  
Sound pool is actually audio mixer. It can play short clips only regardless of whether they are encoded as ogg or mp3 or they are 
uncompressed. Sound pool always store them in memory uncompressed, and you must know that limit is 1 MB.  
If your clip is too big in memory, sound pool will fall silent, and you'll find following error: "AudioFlinger could not create track. 
status: -12" Media player plays stream and decode it in real time. So it can play much longer clips but needs processor power for it.  
  
So Media player is better for background music, while sound pool is better fort short audio effects (clicks, explosions, sound loops). 
In addition, sound pool can play more clips simultaneously, and has volume and speed control. Also it can play loops.  
  
One note: you can't play music from sound pool if clip isn't fully loaded and decoded. So you must use OnLoadCompleteListener 
(Android 10 or above) to check it. If you try to play sound before it is decoded, sound pool will be mute.  
  
Media player doesn't suffer from these problems.  
  
  
**If it is helpful to you then follow me (you can give it a star too), I will make some more useful standard codes..   
Happy Coding :)**
