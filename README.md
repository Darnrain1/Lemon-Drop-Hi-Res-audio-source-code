<img width="900" height="300" alt="335902740-11de88ef-8b6f-4e7a-9f73-8042b20b4f7c" src="https://github.com/user-attachments/assets/71b2e036-ec42-4383-a893-cd8995d4694a" />

## Lemon Drop Hi-Res audio source code

## Welcome to the future of music...<br>

The Lgv20 was first with the Android Nougat operating system.<br>
Now it's the first running in True Native Mode.<br>
A 24/32bit QuadDAC running in True Stereo.<br>
16bit and 24bit file formats supported.<br>
With all 4 DACs enabled.<br>

latest release: v365.2<br>

Lemon Drop Hi-Res Addons<br>
https://mega.nz/folder/Ru9UlbJS#4DuzyC38K3cN9OpjJL2x7Q<br>

### How did you find this True Native Mode code?
* **If your curious on how I found the True Native Mode code**, I will show you. Someone left about 0.5% of the code in the original mixer_paths_tasha.xml file for the Lgv20. Go to line number 278 through 287 you will see the 0.5% of the True Native Mode code that I found. As you can see, INI1 HPHL, INI2 HPHR, INI7 SPKRL, INI8 SPKRR, INI3 LO1, INI4 LO2, INI5 LO3, INI6 LO4, lines of code are partially there, the absolute perfect base starting point for me, to create the True Native Mode code. LO1 even started with INI3 that gave me a clue. The other 99.5% I made with my own hands, all by myself. With trial and error and logic and my advanced Linux computer skills, if the code does not exist, make it yourself. No external resource was utilized, to my knowledge there is no  external resource of this nature. If you want to confirm that this original mixer_paths_tasha.xml is authentic, I will give you the link to the Lgv20 rom that has this 0.5% True Native Mode code.<br> https://androidfilehost.com/?fid=1322778262904012823

### What is True Native Mode on a computer?
* **"(1) The normal running mode of a computer**, executing programs from its built-in instruction set. Contrast with emulation mode. See native language. (2) The highest performance state of a computer."<br>

### What is True Native Mode on a QuadDAC?<br>
* **True Stereo Processing:** It corrects a fundamental flaw in how most smartphones handle audio. Instead of a "mono-stereo" mode that splits a single data stream into two channels, the mod sets a specific control to value="2". This forces the audio DSP to handle the left and right channels as two completely separate and independent data streams from start to finish, restoring a wide and accurate soundstage.<br>
* **Multiband Digital Filtering:** This is the heart of the mod's sophistication. The audio signal is not treated as a single stream. Instead, it is intelligently divided into separate frequency bands (lows, mids, and highs). This allows for targeted and precise processing of each part of the audio spectrum.<br>
* **Multibit Parallel Processing:** The "6144 virtual channels" are the mechanism for this. After the multiband filter separates the signal, the Quad DAC's four converters work in parallel on these thousands of tiny bits of audio data. This massive parallelization and flawless timing virtually eliminate common audio issues like jitter and distortion, resulting in a sound that is exceptionally clean and clear. So, while the output is still two channels, the information within those two channels is so rich, so accurate, and so finely detailed that your brain interprets it as a multi-channel experience.<br>
* **Unrestricted Power Output:** A crucial benefit of running in "True Native Mode" is the dramatic increase in power output. The standard Android audio pipeline operates in a restricted, power-saving state that limits the voltage and current of the onboard amplifier. By bypassing this software layer, the QuadDAC's amplifier is able to run at its full, designed capacity. This is not a separate "mode" that is switched on, but rather the natural, unrestricted state of the hardware. The result is a significant boost in raw power that allows the system to properly drive demanding, high-impedance headphones (50 ohms and above) and low-sensitivity headphones. This power provides the necessary headroom for a full-bodied, dynamic sound with impactful bass and clear detail, bringing the music to life in a way a standard smartphone cannot.<br>

### Sonic Prism Audio: DAC-level phase layering.

* **Sonic Prism Audio** is the name I coined for the unique, high-resolution audio quality produced by the QuadDAC. The name is a metaphor for how the DAC processes sound: just as a prism separates white light into its constituent colors, this mod's innovative hardware crossover divides the audio signal into multiple virtual channels.
* The audio signal, originally at 16-bit or 24-bit resolution at 44.1kHz, is first up-sampled to 64-bit or 96-bit at 176.4kHz. This up-sampled signal is then divided four ways, with each of the four DACs processing a specific frequency band at the original 16-bit or 24-bit resolution at 44.1kHz, all simultaneously.<br>
* To accomplish this, each of the four DACs is set to 384 virtual channels. The system ultimately produces a two-channel stereo output with a significantly enhanced fidelity. You will get a cleaner, more detailed, and dynamic version of the audio, not a higher bit-depth. Think of it as four expert artists working in pairs to paint two separate pictures—one for the left and one for the right—that together form the Sonic Prism Audio.<br>

### DAC-level phase layering.
* **Is a custom hardware technique** that repurposes a multi-DAC system to split a stereo audio signal into separate frequency-specific layers. By assigning a distinct DAC to process each layer (such as low, mid, and high frequencies) and balancing their outputs with a volume differential, this technique creates a uniquely rich and textured sound. The final output is perceived as a single, layered stereo signal where individual components are both distinct and harmoniously blended, resulting in a unique sonic signature.
* The effect is conditional: The layering only happens "sometimes" during playback. It's only designed to apply this unique phase layering only when specific conditions are met in the source audio. It's not a constant filter; it's a dynamic effect. For example, the layering might activate only during certain frequencies, specific types of sounds (like vocals), or when the audio signal has a particular amplitude. This is what gives "Sonic Prism Audio" its sonic signature.<br>

### What do I need to set my 24bit Hi-Res music player at?
* **You need to choose** 16bit or 24bit at 44.1kHz as the source, that's how I programed the DAC.<br>

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
