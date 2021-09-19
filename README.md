# Dot Piano Midi Player
A script that allows you to play custom .mid files through https://dotpiano.com

### Download <a href="https://github.com/TOG11/DotPianoMidiPlayer/releases/tag/Script">script.js<a> in releases

# Getting The Midi File To Play & How The Midi Tracks Work
find a midi file with **ONE TRACK ONLY** If the midi file has more than **1** **track** in it, the script will auto set to play track 1. <br>
**currently you cannot play multiple midi tracks.** <br><br>
if you would like to switch the midi tracks the script plays on, then at the top of script.js, look for, 
```node 
const midiTrack = 1 //<-CHANGE THIS NUMBER TO THE TRACK NUMBER YOU WANT TO PLAY 
```
most of the time you want track 1, however for advanced users i added this setting to the script.

# Upload Midi Files To Server                                
 After you have found your midi file, we need to upload it to a File Server with CORS enabled.
                               <br><br>
Now heres where things **WOULD** get tricky, however luckily for you, i host my own Public File Server W/ CORS Enabled on it.
### https://tog1.cloud is where you can access it from.                               
simply create a one-click account and upload your midi file.
<br>
After your files have been uploaded, copy the link to the .mid file download, go to the config for script.js (at the top of script.js) and paste it here,
 ```node
  const fileurl = 'DownloadLinkGoesHere'
  ```
  
  Your config should look somthing like this afterwards, 
  ```node
  //CONFIG

//the url of the midi file, the site that hosts this file MUST have cors enabled!
const fileurl = 'https://togi.cloud.ngrok.io/data/uploads/users/?img=Dotpiano/media/example.mid'


//the track of the midi file to play. only one track can be played currently.

const midiTrack = 1

//END OF CONFIG
  
  ```
 # Running Our Script (Chrome)                             
   After script.js is configured,<br> go to 
  ### https://dotpiano.com/
  and go to the "Listen" tab.
  <br>
  <br>
  **IMPORTANT: Pause the current playing paino song** <br><br>
  Press F12 on your keyboard, this should open the Developer Menu. 
  <br> Then go to the "Console" Tab at the top of the Menu. <br>
  copy the configured script code, and then paste it into the Console. (**Dependning on the speed of your PC this could take a moment**) <br>
  After its been pasted into the Console, press Enter. <br>
  This should load your midi into Dotpiano <br>
  <br>
  **IF YOU GET A "forEach" ERROR PLEASE RELOAD THE  PAGE AND TRY AGAIN! <br> (im not sure what the culprit of this error is, but i think it has somthing to do with the midi being over 2mins.**

  <br> <br> <br>
  **I am in no way affiliated with https://dotpiano.com, all rights to them for the amazing website!**
  <br>
  <br>
Script Created in Affiliation With TMG Inc. https://togar.media                         
