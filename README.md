<sub>=-DO NOT FORK THIS REPOSITORY-=</sub><br/>
<sub>=--this is not a fork of the original repository,<br/>just build and instructions.<br/>if you do want to fork something, fork the original repository.--=</sub>

<br/>

Windows x64 (AMD64) driver build of  
https://github.com/JannesP/AudioMirror  

<img src="/screenshots/screenshot.png" /><br/>

<hr/>

<blockquote>

this is a virtual audio driver,  
that will allow you to record whatever you play on the speakers (same quality).

<hr/>

it is an alternative to:

- plugging the audio-out on your sound-card, to your line-in (or mic-in), via some kind of an aux-cable (looses quality, line-in not available on some sound-cards).  
- using in-mix/internal-mixer as a recording device (removed in most sound-cards and newer OS).
- buying a some kind of a fance-setup sound-card (this works on the one you already have).

</blockquote>

```diff
+ tested, works on Windows 10 and Windows 11.
```

<hr/>

<h3>

```diff
- no support. 
- installation is complex. developers only!
- security risk: requires trusting a self-signed certificate as trusted CA.
```

</h3>

<hr/>

<h2>

```diff
- to be PERFECTLY clear:
-   this is a highly unstable kernel-driver,  
-   it produces a $h!t-ton of blue-screen-of-death (BSOD),  
-   it will be rebooting a LOT!
+ using on a virtual-machine is advised.

! you have been warned!
```

</h2>

<hr/>

```diff
+ that said, 
+ it is fun to test/play with,  
+ and a good way of learning to write your C++ kernel-driver.
```

<hr/>


<h3>

short instructions no how to install.
- <a href="/how_to_install__tldr__short_version.md">how_to_install__tldr__short_version.md</a><br/>

long instructions no how to install.
- <a href="/how_to_install__long_version.md">how_to_install__long_version.md</a><br/>

a kit ready to be use, packed with just the things you need (binaries, certificate, the long instructions and `devcon.exe`).
- <a href="/x64_driver.zip">x64_driver.zip</a>(58KB)<br/>

five short videos, showing how a full installation, and how to work with it. (include some of my mistakes as informational content).
- <a href="/screenshots/1_allowing_testing_certificate_reboot.mp4">/screenshots/1_allowing_testing_certificate_reboot.mp4</a><br/>
- <a href="/screenshots/2_installing_testing_certificate_reboot.mp4">/screenshots/2_installing_testing_certificate_reboot.mp4</a><br/>
- <a href="/screenshots/3_developer_installation_of_driver_with_devcon_problem_with_old_recording_programs_in_windows_10_reboot.mp4">/screenshots/3_developer_installation_of_driver_with_devcon_problem_with_old_recording_programs_in_windows_10_reboot.mp4</a><br/>
- <a href="/screenshots/4_success_using_new_windows_10_compatible_recording_program_and_exporting_result_as_mp3.mp4">/screenshots/4_success_using_new_windows_10_compatible_recording_program_and_exporting_result_as_mp3.mp4</a><br/>
- <a href="/screenshots/5_a_quick_way_to_disable_driver_when_not_needed_to_avoid_errors.mp4">/screenshots/5_a_quick_way_to_disable_driver_when_not_needed_to_avoid_errors.mp4</a><br/>

information on the build and testing details:
- <a href="/build_and_testing_information.md">build_and_testing_information.md</a><br/>

</h3>

<br/>

<hr/>
<br/>
<br/>