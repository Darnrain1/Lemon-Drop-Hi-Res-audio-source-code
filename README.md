![Untitled](https://github.com/Darnrain1/Lemon-Drop-Hi-Res-audio-source-code/assets/170971862/270e5b01-fdbb-455f-84a4-b0ff12d4be0d)
## Lemon Drop Hi-Res audio source code
Welcome to the future of music...<br>
The Lgv20 was first with the Android Nougat operating system.<br>
Now it's the first running in True Native Mode.<br>
With audio perfictly centered, ballanced, and dynamic normalization.<br>
A 24/32bit QuadDAC in True Stereo.<br>
16bit and 24bit file formats supported.<br>
With all 4 DACs enabled.<br>
DAC 0 = low-range<br>
DAC 1 = mid-range<br>
DAC 2 = high-range<br>
DAC 3 = offload<br>

16BIT wired<br>
Channels = 12,288<br>
KHZ = 705.6<br>
BIT = 256<br>
True Native Mode? Yes.<br>

24BIT wired<br>
Channels = 12,288<br>
KHZ = 705.6<br>
BIT = 384<br>
True Native Mode? Yes.<br>

16BIT bluetooth<br>
Channels = 768<br>
KHZ = 44.1<br>
BIT = 16<br>
True Native Mode? Yes.<br>

24BIT bluetooth<br>
Channels = 768<br>
KHZ = 44.1<br>
BIT = 24<br>
True Native Mode? Yes.<br>

16bit Internal Speaker<br>
Channels = 768<br>
KHZ = 44.1<br>
BIT = 16<br>
True Native Mode? Yes.<br>

24bit Internal Speaker<br>
Channels = 768<br>
KHZ = 44.1<br>
BIT = 24<br>
True Native Mode? Yes.<br>


latest release: v349.1<br>

Lemon Drop Hi-Res Addons<br>
https://mega.nz/folder/Ru9UlbJS#4DuzyC38K3cN9OpjJL2x7Q<br>

### How did you find this True Native Mode code?
If your curious on how I found the True Native Mode code, I will show you. Someone left about 0.5% of the code in the original mixer_paths_tasha.xml file for the Lgv20. Go to line number 278 through 287 you will see the 0.5% of the True Native Mode code that I found. As you can see, INI1 HPHL, INI2 HPHR, INI7 SPKRL, INI8 SPKRR, INI3 LO1, INI4 LO2, INI5 LO3, INI6 LO4, lines of code are partially there, the absolute perfect base starting point for me, to create the True Native Mode code. LO1 even started with INI3 that gave me a clue. The other 99.5% I made with my own hands, all by myself. With trial and error and logic and my advanced Linux computer skills, if the code does not exist, make it yourself. No external resource was utilized, to my knowledge there is no  external resource of this nature. If you want to confirm that this original mixer_paths_tasha.xml is authentic, I will give you the link to the Lgv20 rom that has this 0.5% True Native Mode code.<br> https://androidfilehost.com/?fid=1322778262904012823

### What is True Native Mode on a computer?
"(1) The normal running mode of a computer, executing programs from its built-in instruction set. Contrast with emulation mode. See native language. (2) The highest performance state of a computer."<br>

### What is True Native Mode on the Saber ESS 9218 DAC?<br>
The highest performance state of a of the QuadDAC, or the best audio the QuadDAC can produce.<br>

### What do I need to set my 24bit Hi-Res music player at?
You need to choose 24bit Hi-Res at 44.1kHz as the source, that's how I programed the DAC, it takes a 44.1kHz audio and up-samplese the audio.<br>

### What files were modded?
The 24bit mod. The files I changed are under.<br>
You will need to look at the diff files to see what I changed in the files. No notes were left as there can no be no spaces.<br>
Files modded:<br>
/system/vendor/audio/audio_policy_configuration.xml<br>
/system/vendor/audio_policy.conf<br>

Programing the QuadDAC.<br>
Files modded:<br>
I left notes in both files.<br>
/system/vendor/mixer_paths_tasha.xml<br>
/system/vendor/audio_platform_info.xml<br>

### How can I add this True Native Mode Code to my phone?
You need to have a ESS QuadDAC installed in your phone. So like the lg v series. But this mod was custom made for the Lgv20. However the Enable System Wide QuadDAC Support build.prop tweaks should work on any phone with a DAC. It will enable Hardware-Offloaded Audio Processing. In other words all the audio will be directed to the DAC.<br>

### How long did it take you to program the QuadDAC?
About two years, it was a very large project. The mixer_paths_tasha.xml file is over 30,000 lines.<br>

MIT License<br>

Copyright (c) 2023 darnrain1<br>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:<br>

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.<br>

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.<br>
