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

• Project sandcastle android

• Project sandcastle linux

libimobiledevice programs (precompiled .net version):

  • irecovery

  • iproxy

  • idevicename

  • ideviceinfo

 (not all libimobiledevice utilites are included in the app itself, but can be used with the "diy" command, see below)

# Can I use other libimobiledevice tools 
YES!

You can use the diy command to move the libimobiledevice folder to the working directory (where jailm8.exe is). You can then cd into this directory with command prompt or powershell, and run the exe's. For documentation on the guides, check the [libimobiledevice website](https://github.com/libimobiledevice-win32/imobiledevice-net)

# Commands:
You can put either the number or command into the jailm8 interface
| Number in menu  | command | info |
| --- | --- | ---|
| 1.  | android  | boot android through project sandcastle |
| 2. | linux  | boot linux through project sandcastle |
| 3. | iproxy | forward your devices local ssh server to a port on your computer |
| 4. | name | check which devices are connected, outputs connected devices names |
| 5. | id | see device udid |
| 6. | info | outputs a long list of details regarding your device. It can also dump these details to a text file |
| 7. | pair | idevicepair utility |
| 8. | provision | ideviceprovision utility |
| 9. | date | see device date |
| 10. | debug | idevicedebug utility |
| 11. | diy | download libimobiledevice to working directory |
| 12. | clean | deletes downloaded resources |
| 13. | support | Join my discord server for more support, or if you just wanna talk about jb |
| 14. | exit | guess |
| 15. | menu | Shows app menu |
| 16. | help | shows help text |
| 17. | color | shows available colour schemes for jailm8 |
| 18. | update | updates downloaded resources from this repo |
| 19. | version | prints current jailm8 version, latest jailm8 version and connected device's ios version if connected |
|  | restart | restart's jailm8, this isn't that important a command so I didn't add a menu entry for this |

# If its not open-source, whats this repo for?
This repo contains (most of) the precompiled binaries for the tools included above. Jailm8.exe will download these files if you choose an option that requires them.

It will only download the required files, so you won't get unnecessary files being downloaded

If you have errors with a message saying windows couldn't run this program, use the clean command, and try again

The resources folder also contains some saved data (colour schemes), so you will need to re-run the color command after cleaning the resources.

# Whats it written in?
Actually, most of the functions are batch functions, but the overall app is held together by .NET. This is the reason the app looks a lot like batch scripts, but that allows for running the different commands within the app. Unfortunately, this makes running jailm8 off a usb (ironic) significantly slower, as windows has to suffer odd write speeds and stuff. This was originally gonna be written in c and compiled with cygwin, but then I was enlightened about the powers of bash to run commands within the app, so .NET and batch it was.

# sources
Project sandcastle binaries from [here](https://github.com/corellium/projectsandcastle/tree/master/loader) compiled by me

[libimobiledevice](https://github.com/libimobiledevice-win32/imobiledevice-net), precompiled
