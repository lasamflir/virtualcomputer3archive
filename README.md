# virtualcomputer3archive

These are all of the files associated with the final iteration of the Virtual Computer Project, a series of fantasy computers programmed in Assembly, called Advanced Virtual Computer 3. This was made in SmileBASIC for the New 3DS.

This was by far my biggest software project. I really enjoyed developing and using it, but now that the Nintendo Network is shutting down, it will be harder than ever to share with others and I must move on. I am uploading it to GitHub so that anyone with a 3DS and PetitModem can download it and anyone on GitHub can inspect it.

I am not done with fantasy computers. If I can work out the necessary GUI programming for it, there will be a new virtual computer for the PC or the web, whichever's easiest to develop for.

While the Nintendo Network is still available (until April 8th 2024), you can save yourself the hassle of using PetitModem and download this project with the code **T5CEW3J4**.

# How to download these files.

Use version 1.4.1 of PetitModem (http://rei.to/petitmodem.html) to put the files on your 3DS. You will need to modify the PetitModem 3DS client to only save files as TXT, since it otherwise defaults to DAT for files without extensions. Comment out everything after ELSE on line 916, and comment out lines 918 and 919.

# How to use AVC3

At minimum you need two files. These are the ones named "AVC3" and "LIB" with many hyphens in front (to place them at the top of SB's menu system). These are the virtual computer itself and the library of subroutines that is loaded in at every launch. While AVC3 can be modified to run without this, it is heavily referenced by nearly all of my programs.

Launch AVC3 and you will see several options. To run software already in slot 1, press down. I can answer any questions you have about the menu system, but I don't have the time to properly document it right now. Do try the debug mode though, it's very pretty. :)

Programs are written in AVC3 assembly, and are assembled every time they are run. There is no machine code or "ROM" format. I don't have time to write detailed descriptions of each program, but their names should tell you what they do. Some programs load data from the clipboard. Some programs explain their controls. If you're really stuck, you can try looking at the source code. I will upload documentation for AVC3 assembly at some point.

# What is this project?

At the end of high school, I decided I really wanted to learn how computers work at a low level. This led to developing my own fantasy computer and assembly language. Over the many iterations (VC1-8, AVC1-3), I have learned to be a better Assembly programmer and fantasy computer designer through each iteration having weaknesses I addressed in the next. This is comparable to CHIP-8, except it's a fantasy *computer* and not a fantasy *games console*. I also really enjoy writing emulators, interpreters and compilers, so this is my ideal form of hobby programming. Several programs from previous iterations in the series are included, as well as several emulators and interpreters for them. There is even a self-emulator, though it is functionally absolutely pointless. :)

The architecture is quite powerful. Instructions that reference registers can also reference memory and the stack, making for very dense Assembly code. It's a 16-bit word architecture with 64 kilowords (128KB) of addresses, all of which are memory. The displays are 32x24 character grids that can reference anywhere in memory and available inputs are touch and buttons. The circle pad and c-stick are reserved for debug mode. The architecture is optimised for making programs with text input and output, with a virtual keyboard provided by the library code.

# Why did you make it in SmileBASIC?

I like programming platforms that already have an inherent 8-bit look to them, and are constrained in some way. Before SB, I would mainly program for my calculator in Casio BASIC. I also like the portability of a programming language I could use on my 3DS. SB also has several features that make it desirable for this sort of project, like having multiple program slots and running on "modern" hardware that reach about 25-45 KHz in most programs.
