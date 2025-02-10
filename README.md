![Untitled](https://github.com/Darnrain1/Lemon-Drop-Hi-Res-audio-source-code/assets/170971862/270e5b01-fdbb-455f-84a4-b0ff12d4be0d)
## Lemon Drop Hi-Res audio source code
Welcome to the future of music...<br>
The Lgv20 was first with the Android Nougat operating system.<br>
Now it's the first running in True Native Mode.<br>
With audio perfictly centered, ballanced, and normalized audio.<br>
With all 4 DACs enabled.<br>
DAC 0 = low-range<br>
DAC 1 = mid-range<br>
DAC 2 = high-range<br>
DAC 3 = offload<br>

16BIT<br>
Channels = 12,288<br>
KHZ = 705.6<br>
BIT = 256<br>

24BIT<br>
Channels = 12,288<br>
KHZ = 705.6<br>
BIT = 384<br>

latest release: v285.1<br>

"Sounds amazing, outstanding and breathtaking" - Darnrain1<br>

### How did you find this True Native Mode code?
If your curious on how I found the True Native Mode code, I will show you. Someone left about 0.5% of the code in the original mixer_paths_tasha.xml file for the Lgv20. Go to line number 278 through 287 you will see the 0.5% of the True Native Mode code that I found. As you can see, INI1 HPHL, INI2 HPHR, INI7 SPKRL, INI8 SPKRR, INI3 LO1, INI4 LO2, INI5 LO3, INI6 LO4, lines of code are partially there, the absolute perfect base starting point for me, to create the True Native Mode code. LO1 even started with INI3 that gave me a clue. The other 99.5% I made with my own hands, all by myself. With trial and error and logic and my advanced Linux computer skills, if the code does not exist, make it yourself. No external resource was utilized, to my knowledge there is no  external resource of this nature. If you want to confirm that this original mixer_paths_tasha.xml is authentic, I will give you the link to the Lgv20 rom that has this 0.5% True Native Mode code.<br> https://androidfilehost.com/?fid=1322778262904012823

### What is True Native Mode on a computer?
"(1) The normal running mode of a computer, executing programs from its built-in instruction set. Contrast with emulation mode. See native language. (2) The highest performance state of a computer."<br>

### What is True Native Mode on the Saber ESS 9218 DAC?<br>
I created all 1568 lines of the True Native Mode code myself, with the help of echo and nano, there are 786 mixer paths for True Native Mode that places the QuadDAC into it's highest performance state. The very essence of True Native Mode it's self allows the DAC to have more than two channels, like one for left and one for right. I have the QuadDAC overclocked so we can have more than 3072 channels. There are 768 channels going to each DAC, 768 X 64 = 49152 then divide 49152 by 2 = 24576 for each DAC for a total of 98304 channels. We can only hear up to 20kHz however the more channels there are the better the audio sounds to us, it's like SD video vs HD video.<br>

### How did you program and tune the QuadDAC?
When programing a QuadDAC you do not have visual gauges to view to see if you have done something wrong, its all done by the sound of the DAC. For example if you have increased the amount of channels way to high or messed up on your programing code, then the DACs volume will be decreased or the music will not sound like its full of life. The only way to accomplish that, is to lower the AVC volume. In other words it decreases the power to the DAC so you can program and tune the DAC. In v142.1 and higher the AVC volume is set to the maximum. I know with out a doute that the True Native Mode code is pristine, I had echo print out the numbers, then I cut and pasted 768 times. I used nano's macro feature to program True Native Mode.<br>

I guess you could say I have a gift that allows me to think outside of the box. I was always seeing LO in the True Native Mode code. I was like what is LO??? Then it hit me it's the bass. I came up with MI and HI for mid-range and treble myself and it worked!!! Also I was always seeing RX everywhere I looked, I was like well if there is an RX there has to be a TX. I guess you could say it was trial, error, logic and my advanced Linux computer skills, is how I programed the Saber ESS 9218 DAC. The devs that programed the Saber ESS DAC chip are professionals, you need to think like how they think. They would not make it to complicated to program the QuadDAC. To me it was the ultimate puzzle that needed to be solved and I did solve it. It feels good.<br>

### I want to add this True Native Mode code, to my Android phone?
It is my understanding that the two files responsible for making this all happen are, audio_platform_info.xml and mixer_paths_tasha.xml. Duplicate all the changes I made leaving intact your unique settings. I made notes in both files, to help you along the way. Keep in mind everthing in the mixer_paths file must be absolutely perfect, zero typos or mistakes, this is not for the novice computer user. The QuadDAC also needs Enable System wide QuadDAC support v8.2 aka build.prop audio tweaks. All the other files were from my previous attempts to increase the audio quality of the Lgv20 without avail.<br>

### What do I need to set my Hi-Res music player at?
You need to choose 24bit 44.1kHz as the source, that's how I programed the DAC, it takes a 44.1kHz audio signal and upsamples the audio eight times to 32bit 352.8kHz. On wired headphones the output is 32bit 352.8kHz, all other devices the output is 44.1kHz 24bit or 16bit. If set to anything other than, 44.1kHz the audio does not get upsampled eight times or it does not multiply evenly into 352.8kHz. In other words, your not going to get the absolute best audio quality.<br>

### There is three different kinda of recordings of music out there. 
My 24/32bit QuadDAC will play all three, but you will know when you have music recorded in True Native Mode because it's amazing and mind blowing. All the newer music should be in True Native Mode, older music is not unless it's remastered. I know Elephunk - Black Eyed Peas opus format, on YouTube Music is in True Native Mode. Get opus format over mp4 it's so much better. Newer technology..<br>
One. Low. aka free.<br>
Two. Medium. aka paid.<br>
Three. High True Native Mode. aka $5000+ dollar Hi-Res music player..<br>

### FAQ.
How did you program a QuadDAC?<br>
Well it was not easy, and took over two years. Everything has to be perfect. That's why it has taken me so long. Also I wrote over 25,000 lines of code for the QuadDAC to run in True Native Mode.<br>

Was it worth all the time you put into this project?<br>
I now have a $5000+ 24bit Hi-Res Music Player. One word, yes.<br>

Do I have to use a 24bit Music Player to listen to True Native Mode?<br>
Nope, 16bit and 24bit music players work in True Native Mode.<br>

What is Hardware-Audio Offloaded Processing?<br>
All the music goes directly to the QuadDAC, bypassing Android.<br>

Can I stream music on a 16bit music player and listen to True Native Mode?<br>
If the music was recorded in True Native Mode then yes. Most newer music is but some is not.<br>
 
Check out my other project perfect for downloading music..<br>
https://github.com/Darnrain1/yt-playlist.<br>

Don't forget to power off your phone after your flash Lemon Drop HI-Res for settings to take affect.
 
### A little backstory.
I remember when I first found the True Native Mode code, I was like ooh what's that. They left about 0.5% of the True Native Mode code in the original mixer_paths_tasha.xml file, I put the other 99.5% of the True Native Mode code together myself. Just think if they would have never left that small peace of code in the original mixer_paths_tasha.xml file this would have never had happened. All I can say is that must have been a mistake, the Lgv60 does not have that small piece of code, only the Lgv20 does. I bet this is the same True Native Mode code as a $2000 Hi-Res music player. Most likely they have a computer program that programs the QuadDAC for True Native Mode, me on the other hand, this True Native Mode code was all hand made by me. So in other words, the Lgv20 will sound like no other Hi-Res music player in the world. A computer program cannot replace the very essence, of what a human is able to accomplish when programing a QuadDAC.<br>

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
