This is how I calculated the amount of mixer paths to program in for True Native Mode for the QuadDAC. Bass, mid-range and treble all require 16 mixer paths each for a QuadDAC. So 16 X 3 = 48 then for a QuadDAC you want to times 48 X 16 = 768. So 768 is our magic number.


When programing the mixer paths for a QuadDAC you want two DACs on TX and two on RX like this. This applies to everything. Because you have a left and right channel or TX or RX and you do not want all 4 DACs working on the same thing and the same time.

	<ctl name="RX INT6 SPLINE MIX LO4 Native Switch" value="2" />
	<ctl name="RX INT6 SPLINE MIX LO4 Switch" value="2" />
	<ctl name="RX INT9 SPLINE MIX MI5 Native Switch" value="2" />
	<ctl name="RX INT9 SPLINE MIX MI5 Switch" value="2" />
	<ctl name="RX INT10 SPLINE MIX HI6 Native Switch" value="2" />
	<ctl name="RX INT10 SPLINE MIX HI6 Switch" value="2" />
	<ctl name="TX INT11 SPLINE MIX LO7 Native Switch" value="2" />
	<ctl name="TX INT11 SPLINE MIX LO7 Switch" value="2" />
	<ctl name="TX INT12 SPLINE MIX MI8 Native Switch" value="2" />
	<ctl name="TX INT12 SPLINE MIX MI8 Switch" value="2" />
	<ctl name="TX INT13 SPLINE MIX HI9 Native Switch" value="2" />
	<ctl name="TX INT13 SPLINE MIX HI9 Switch" value="2" />

It is my understanding that the two files responsible for making this all happen are, audio_platform_info.xml and mixer_paths_tasha.xml. I disconnected the QuadDAC from the Android mixer in audio_platform_info.xml and programed the QuadDAC for True Native Mode in the mixer_paths_tasha.xml. The QuadDAC also needs Enable System wide QuadDAC support v8.2 aka build.prop audio tweaks. All the other files were from my previous attempts to increase the audio quality of the Lgv20 without avail.

I made two diffrent flavors of Lemon Drop Hi-Res but only one souce code. To change the DAC modes search for: <path name="speaker-initialization-switch">


treble
	<ctl name="SpkrLeft COMP Switch" value="2" />
	<ctl name="SpkrLeft BOOST Switch" value="0" />
	<ctl name="SpkrLeft VISENSE Switch" value="0" />
	<ctl name="SpkrLeft WSA PA Mute" value="0" />
	<ctl name="SpkrLeft SWR DAC_Port Switch" value="2" />
	<ctl name="SpkrRight COMP Switch" value="2" />
	<ctl name="SpkrRight BOOST Switch" value="0" />
	<ctl name="SpkrRight VISENSE Switch" value="0" />
	<ctl name="SpkrRight WSA PA Mute" value="0" />
	<ctl name="SpkrRight SWR DAC_Port Switch" value="2" />

bass+
	<ctl name="SpkrLeft COMP Switch" value="2" />
	<ctl name="SpkrLeft BOOST Switch" value="2" />
	<ctl name="SpkrLeft VISENSE Switch" value="2" />
	<ctl name="SpkrLeft WSA PA Mute" value="0" />
	<ctl name="SpkrLeft SWR DAC_Port Switch" value="2" />
	<ctl name="SpkrRight COMP Switch" value="2" />
	<ctl name="SpkrRight BOOST Switch" value="2" />
	<ctl name="SpkrRight VISENSE Switch" value="2" />
	<ctl name="SpkrRight WSA PA Mute" value="0" />
	<ctl name="SpkrRight SWR DAC_Port Switch" value="2" />

Will this True Native Mode code work on other Android phones other than the Lgv20?

I can't say for absolutely certain, I can say for certain that the True Native Mode code runs excellent, on both of my Lgv20's, my main phone DeGoogled and the spare one with Google intact both running Stock Oreo ezV2020 v1.0 Kernel. Who knows this True Native Mode code may work universally across all QuadDACs on all Android phones. It's up to you guys to beta test this code, my job is all done, I just had to recreate the True Native Mode code and make it work. The LG V series of phones, will have the best chance of this True Native Mode code working. Also keep in mind that I officially got True Native Mode working in v169.1, on 01-17-24 phones manufactured after that date may have True Native Mode disabled on the QuadDAC chip.
What brand of QuadDAC is this code compatible with?

Saber ESS QuadDACs only. The worlds best audio, requires the worlds best!
I want to add this True Native Mode code, to my Android phone?

My theory is that the two files responsible for making this all happen are, audio_platform_info.xml and mixer_paths_tasha.xml. All the other files are associated with the Android mixer and are the left over reminisce of my previous attempts of trying to increase the audio quality on the Lgv20 without avail. However I may be entirely wrong. It's up to you guys to find out how to make it work on other phones. It works on my Lgv20, it's using all the modded files. The initial mixer settings is the most important part of the QuadDAC. If there are duplicates or errors or mistakes in that location. Then it will effect the audio quality of the QuadDAC and or the QuadDAC will simply not function. You will know when you have messed up, your phone will not boot and or there will be no sound. There is over 6,000 lines of code in that location. If you are attempting to add my code to your mixer_paths file. Just remember that this is a puzzle, and 95% of the peaces were missing. I not only had to make the 95% of the missing code and program the QuadDAC. I also had to fight with the original mixer_paths file, it was FUBAR. Who ever programed the Lgv20's original mixer_paths.xml file, had absolutely no clue what they where doing. This was very challenging for me, and fun. You will also need to make the missing peaces of your unique initial mixer settings. You need to work in the initial mixer settings, as well as adding my code to your mixer_paths file. I already programed the QuadDAC, you just need to make sure the initial mixer settings are the same as your phone. Your welcome to delete the initial mixer settings of the Lgv20, some settings are going to be the same like the volume settings. It's going to take time, it has taken me over a year.

The QuadDAC also needs Enable System wide QuadDAC support v8.2 aka build.prop audio tweaks. The QuadDAC needs exactly 4MB cache size. This also will enable Hardware Offloaded Audio Processing. In other words all audio including bluetooth is routed through the QuadDAC. Android has no say, when it has to do with the audio. This also means that the QuadDAC must stay enabled at all times. This was the only way, I was able to get around the audio limitations set in place by Android. In other words, checkmate.

When programing the mixer_paths file, I only use the tab key not the spacebar, it's just a pet peeve. ;)

I cant program with how disorganized the original mixer_paths file is. This is how I tabbed all lines and fixed it. I use arch linux.

Example:

cat your_mixer_paths_file.xml | sed 's/^[ \t]*//' > new_mixer_paths_file.xml

sed commands:
Move all lines to the left:

sed 's/^[ \t]*//'

Tab all lines:

sed 's/^/\t/'

This is how I debugged the code. I copied a section, pasted into a file test.txt then removed all the lines that have RX. Then I looked over test1.txt there should be groups of 4 or 3 and so on. If not then I knew I messed up. I did the same thing with RX.

cat test.txt | grep TX > test1.txt

The mixer_paths.xml file must have zero duplicates, or your phone will not boot. The initial mixer settings is the most important part, there should be zero duplicates, zero mistakes, zero errors. Copy a section, paste it into a file test.txt. This command will print all duplicates including all the spaces. A little tip, if you stdout into a file. Just scroll down, all the spaces are at the top. Yeah I found that out the hard way. lol

sort test.txt | uniq -D


