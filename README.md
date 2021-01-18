# jailm8-windows
A multipurpose jailbreak tool for windows

# introduction
You've probably heard of [jailm8](https://github.com/SarKaa/jailm8), the bootable linux os that was optimised for checkra1n, and a few other features.

I saw that a lot of people used my tool to run project sandcastle without a linux computer. I felt sorry for these people, as there were no native tools for psc for windows.

I saw this with a lot of other tools as well. Tools that could have been compiled in a few minutes with cygwin or MingW.

# What is it?
So I had made [jailm8](https://github.com/SarKaa/jailm8), with all its extra features, but I was disappointed by the lack of tools available for windows. I saw that people had to resort to compiling tools themselves with cygwin, which is a horrible experience for some tools (project sandcastle I'm looking at you)

On my [discord support server](https://discord.gg/VDUFB3gpeQ), I was talking about how jailm8 (the iso) would become obsolete when checkra1n for windows is released. Then a friend asked me if I could make a simple tool that would make it easy to set up the same extra features I had in jailm8, but for windows.

Naturally, I looked around, no one had specific tools compiled for windows, everyone expected people to compile them themselves.

I got to work, compiling various different jailbreak tools, and making a small windows app that could run these files. 

In short, its a minimal frontend, that sets everything up for you, for various tools for windows.

# tools included
I have pre-compiled the following programs, and they will be downloaded automatically when needed.

• Project sandcastle android

• Project sandcastle linux

libimobiledevice programs (precompiled .net version):

  • idevicepair

  • iproxy

  • idevicename

  • ideviceinfo

  • Idevice_id

  • idevicedebug

  • ideviceprovision

  • idevicedate
  
  • irecovery

 (not all libimobiledevice utilites are included in the app itself, but can be used with the "diy" command, see below)

# Can I use other libimobiledevice tools 
YES!

You can use the diy command to move the libimobiledevice folder to the working directory (where jailm8.exe is). You can then cd into this directory with command prompt or powershell, and run the exe's. For documentation on the guides, check the [libimobiledevice website](https://github.com/libimobiledevice-win32/imobiledevice-net)

# Commands:
You can put either the number or command into the jailm8 interface
| Number in menu  | command | info |
| --- | --- | ---|
| 1.  | android  | boot android through project sandcastle (once checkra1n is relased for windows, this will be merged with the next option) |
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
| 12. | irecovery | irecovery utility |
| 13. | support | Join my discord server for more support, or if you just wanna talk about jb |
| 14. | exit | guess |
| 15. | menu | Shows app menu |
| 16. | help | shows help text |
| 17. | color | shows available colour schemes for jailm8 |
| 18. | update | updates downloaded resources from this repo |
| 19. | clean | deletes downloaded resources |
|  | version | prints current jailm8 version, latest jailm8 version and connected device's ios version if connected |
|  | restart | restart's jailm8, this isn't that important a command so I didn't add a menu entry for this |
|  | stats | prints a list of useful stats from the app itself, like how many resources have been saved |
|  | amds64 | Lets you trigger the Apple Mobile Device Support installer manually |
|  | startup | lets you set a command to be run automatically when starting jailm8 |

# If its not open-source, whats this repo for?
This repo contains (most of) the precompiled binaries for the tools included above. Jailm8.exe will download these files if you choose an option that requires them.

It will only download the required files, so you won't get unnecessary files being downloaded

If you have errors with a message saying windows couldn't run this program, use the clean command, and try again

The resources folder also contains some saved data (colour schemes), so you will need to re-run the color command after cleaning the resources.

This repo also hosts some of the files used for the update checker, these are not affected by the clean command.

Not all the files are kept in the source code part, some files are too big.

For the links to every resource, check the links.txt file

# Whats it written in?
Actually, most of the functions are batch functions, but the overall app is held together by c. This keeps the app nice and small, but also lets jailm8 integrate all the tools into the app much quicker. Its compiled with mingw. Most of the time, it will act like batch, but the C parts handle startup and exit. I highly suggest using the exit option (14 on menu) instead of simply pressing the cross, just to allow the app to close properly.

# How does the auto-update checker work
Jailm8 will automatically check for updates (when it displays the ASCII jailm8 text), and if there is an update available, it will ask if you want to update.

If you select yes, it will close jailm8 and open a command prompt window where the old jailm8.exe will be deleted, and a new one will be downloaded. It should automatically start jailm8 again, unless something interferes with it.

# How is it so small?
Its kept small by keeping all resources to be downloaded, so nothing is kept in the app itself, apart from links. The app itself doesn't have a gui, so theres no excess code needed. It is also kept small by using an optimum combination of C and Batch code, keeping the need for extra compilable code short. 

# sources
Project sandcastle binaries from [here](https://github.com/corellium/projectsandcastle/tree/master/loader) compiled by me

[libimobiledevice](https://github.com/libimobiledevice-win32/imobiledevice-net), precompiled

Apple Mobile Device Support 64 extracted from the iTunes setup EXE (from apple, not from the microsoft store)
