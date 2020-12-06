# jailm8-windows
A multipurpose jailbreak tool for windows

# introduction
You've probably heard of [jailm8](https://github.com/SarKaa/jailm8), the bootable linux os that was optimised for checkra1n, and a few other features.

I saw that a lot of people used my tool to run project sandcastle without a linux computer. I felt sorry for these people, as there were no native tools for psc for windows.

I saw this with a lot of other tools as well. Tools that could have been compiled in a few minutes with cygwin.

# What is it?
So I had made [jailm8](https://github.com/SarKaa/jailm8), with all its extra features, but I was disappointed by the lack of tools available for windows. I saw that people had to resort to compiling tools themselves with cygwin, which is a horrible experience for some tools (project sandcastle I'm looking at you)

On my [discord support server](https://discord.gg/VDUFB3gpeQ), I was talking about how jailm8 (the iso) would become obsolete when checkra1n for windows is released. Then a friend asked me if I could make a simple tool that would make it easy to set up the same extra features I had in jailm8, but for windows.

Naturally, I looked around, no one had specific tools compiled for windows, everyone expected people to compile them themselves.

I got to work, compiling various different jailbreak tools, and making a small windows app that could run these files. 

# tools included
I have pre-compiled the following programs, and they will be downloaded automatically when needed.

Project sandcastle android

Project sandcastle linux

libimobiledevice programs (precompiled .net version):

irecovery

iproxy

idevicename

ideviceinfo

(not all libimobiledevice utilites are included in the app itself, but can be used with the "diy" command, see below)

# Can I use other libimobiledevice tools 
YES!

You can use the diy command to move the libimobiledevice folder to the working directory (where jailm8.exe is). You can then cd into this directory with command prompt or powershell, and run the exe's. For documentation on the guides, check the [libimobiledevice website](https://github.com/libimobiledevice-win32/imobiledevice-net)

# If its not open-source, whats this repo for?
This repo contains (most of) the precompiled binaries for the tools included above. Jailm8.exe will download these files if you choose an option that requires them.

It will only download the required files, so you won't get unnecessary files being downloaded

If you have errors with a message saying windows couldn't run this program, delete the resources folder, and re-run jailm8.exe


# sources
Project sandcastle binaries from [here](https://github.com/corellium/projectsandcastle/tree/master/loader) compiled by me

[libimobiledevice](https://github.com/libimobiledevice-win32/imobiledevice-net), precompiled
