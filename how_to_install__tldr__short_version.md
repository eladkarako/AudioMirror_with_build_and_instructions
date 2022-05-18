TL;DR

0. on a VM only!
1. CMD as ADMIN, `bcdedit.exe -set loadoptions DDISABLE_INTEGRITY_CHECKS`, `bcdedit.exe -set TESTSIGNING ON`, reboot.
2. extract `x64_driver.zip` anywhere.
3. install `AudioMirror.cer` as `Trusted R00t Certification Authorities`, reboot.
4. CMD as ADMIN, `devcon.exe install "AudioMirror.inf" "Root\AudioMirror"`, reboot.
5. Windows audio settings, set `AudioMirror` as your default speakers and microphone.
6. done. play audio, use a recording software to record AudioMirror (raw wave input). make sure your headphones are disconnected, the headphone-jack detection switches overrides the "default" speakers while it is connected. Chrome needs to restart after each time you change your default device, so the change would take effect.
7. expect BSOD, requiring you to reset the machine, happens ever long usage (buffer) or trying to switch default device while it is recording. if possible when not needed for some time, disable those devices.