long version, also included as `how_to_install__long_version.txt` inside `x64_driver.zip`


instructions are based on  
https://github.com/microsoft/Windows-driver-samples/tree/master/audio/sysvad  
and  
https://docs.microsoft.com/en-gb/windows-hardware/drivers/develop/preparing-a-computer-for-manual-driver-deployment  


<h3>

```diff
- ===============================================
- WARNING! NO SUPPORT!
- WARNING:
-   only do this on a virtual-machine!
-   NEVER your-own computer!!!
- ===============================================
```

</h3>

0. download `x64_driver.zip`, unzip it anywhere, a short path is advised (no spaces).

<hr/>

1. open CMD as admin.

2. run:
`bcdedit.exe -set loadoptions DDISABLE_INTEGRITY_CHECKS`

3. run:
`bcdedit.exe -set TESTSIGNING ON`

4. reboot (when the machine will be up, you'll see a little note on the bottom right corner).

<hr/>

5. open the folder of where you've extracted the `x64_driver.zip`.

6. double click `AudioMirror.cer`.

7. click <kbd>install certificate</kbd> button.

8. set `store location` to `local machine`.

9. select `place all certificates in the following store`.

10. click <kbd>browse</kbd> button, select `Trusted R00t Certification Authorities` (click <kbd>OK</kbd>).

11. finish installation.

12. reboot (again).

<hr/>

13. open CMD as admin.

14. change folder to where you've extracted the archive.

15. run:
`devcon.exe install "AudioMirror.inf" "Root\AudioMirror"`

16. a driver installation pop-up would come up, click install.

17. in the CMD console, you should get a message, similar to this:
Device node created. Install is complete when drivers are installed...
Updating drivers for Root\AudioMirror from C:\Users\Elad\Desktop\x64_driver\AudioMirror.inf.
Drivers installed successfully.

18. run:
`devmgmt.msc`

19. you should have under `Audio inputs and outputs`:
`Microphone (AudioMirror VirtualDevice)`  
`Speakers (AudioMirror Virtual Device)`  

in addition to what you would normally have:  
`Microphone (High Definition Audio Device)`  
`Speakers (High Definition Audio Device)`  
(or something similar).

20. you should have under `Sound, video and game controllers`
`AudioMirror Virtual Device`  

in addition to what you would normally have:
`High Definition Audio Device`
(or something similar).

21. run:
`"C:\Windows\system32\rundll32.exe" shell32.dll,Control_RunDLL mmsys.cpl,,sounds`

or right click the Windows volume icon, and choose `sounds` .

22. switch to the `Recording` tab,  
right click the Microphone with the description of `AudioMirror Virtual Device`,  
choose `Set as Default Device`.

23. right click it again, choose: `Set as Default Communication Device`.

24. switch to the `Playback` tab, in a similar way to before, right click the Speakers with the description of `AudioMirror Virtual Device`, choose `Set as default device`.

25. and in a similar way, right click it again, choose: `Set as Default Communication Device`.

26. you are pretty much done with the configuration. install some kind of a audio recording program, such as audacity or adobe audition.

27. make sure the audio input (wave in) source is set to the `microphone` described as `AudioMirror Virtual Device`, it should be already set that way due to setting it as the default device for Windows.

28. start playing any audio from any source, it can be a <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">YouTube video</a>, a video call, etc..  
the audio would be played using the speakers described as `AudioMirror Virtual Device` (since you've set it to be the default device).

29. you'll be able to record that audio. 
you WILL NOT be able to hear it at the same time (from your real speakers, or earphones). 
you can adjust the volume of the speakers ("AudioMirror Virtual Device") using the Windows volume icon, 
and it will effect the recording volume in real time.
you are recording in raw wave, this is what the device provides (every device), 
your recording program might be able to save it in various formats afterwards (mp3, m4a, oga, etc..).  

make sure your headphones are disconnected, the headphone-jack detection switches overrides the "default" speakers while it is connected.  
restart Chrome after each time you change the default device, for the change to take effect.  

I advise to reboot.  
Microsoft Edge (Chromium/Chrome based) for example,  
tends to run in the background as soon as you start Windows (some nasty update service).  
this means that while you've changed the default device,  
it was already running (and as explained above, it has problems switching devices).

note: old programs that were not designed for the new audio devices scheme of Windows 10 will act funny/not record.  
in most of the cases you'll have to take control over the whole files, and configure some group policy and apply registry patches to make every file execution as admin, without monitoring desktop applications or applications installed on secure locations such as program files. it is messy, even for a VM. adobe audition 1.5 is like that.  

just use audacity, get the latest zip version from their github page (instead of the download page),  
https://github.com/audacity/audacity/releases/latest  
for example:  
https://github.com/audacity/audacity/releases/download/Audacity-3.1.3/audacity-win-3.1.3-64bit.zip  


30. when you're done,  
right click the Windows volume button, and open `sounds` again, switch to the recording and playback tabs,  
and set your normal speakers and microphone to be the deafult devices so you'll be able to use your machine again normally.
expect BSOD, requiring you to reset the machine, happens ever long usage (buffer) or trying to switch default device while it is recording. if possible when not needed for some time, disable those devices.  

31. uninstalling the driver is done through opening `devmgmt.msc` as ADMIN (as explained above), 
then right-click, "uninstall" for all the AudioMirror items.  
it is best to pre-set the default devices to another device before doing so,  
you can choose to remove the actual driver software as well,  
this driver does not have an additional software so it does not matter,  
you can check it if you want.  
after a reboot your machine would be clean.  

32. again, do not install it on your own computer, only a virtual-machine!

