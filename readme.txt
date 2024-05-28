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

It is my understanding that the two files responsible for making this all happen are, audio_platform_info.xml and mixer_paths_tasha.xml. I disconnected the QuadDAC from the Android mixer in audio_platform_info.xml and programed the QuadDAC for True Native Mode in the mixer_paths_tasha.xml. The QuadDAC also needs Enable System wide QuadDAC support v8.2 aka build.prop audio tweaks. All the other files were from my previous attempts to increase the audio quality of the Lgv20 without avail. I have been working on this project for a long time, I lost track.

At the very least you need these 4 build.prop lines to increase the buffer size for the QuadDAC so it can run in True Native Mode.
audio.offload.size.kb=4096
audio.offload.buffer.size.kb=8192
venter.audio.offload.size.kb=4096
venter.audio.offload.buffer.size.kb=8192

Your welcome to look over all my notes in the mixer_paths_tasha.xml and audio_platform_info.xml files, my hope is by documenting all the modifications I made is to have people reprogram other Android phones so everyone can enjoy Hi-Res audio.

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
