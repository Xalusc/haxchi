# Haxchi

This is the continuation of the POC Haxchi exploit by smea.  
It features compatibility with a lot of DS VC and can be easly installed and further configured.

## Installation

If you already have a installation of v1.7 or v1.8 then this wont bring anything new for you, it just makes it far simpler for new people.  
It now comes with its own installer and does not need iosuhax, wupclient or any additional scripts anymore, just your wiiu, a DS VC game and a way to run the homebrew launcher.  
If you happen to have a DS VC title [that is listed in this file](installer/src/gameList.h#L14-102) then go ahead and grab both haxchi .elf and .zip from the "releases" tab, make sure to NOT click on "source code" but on haxchi.elf and haxchi.zip.  
The .elf goes into sd:/wiiu/apps and the .zip should just be extracted to sd:/haxchi with all its contents inside. That content right now just consists of a simple replacement icon, logo and replacing the game title with "Haxchi", its example config.txt will boot homebrew launcher by default and a fw.img on your sd card when holding A. For a full list of all compatible buttons that you can use for the config.txt go [here](dsrom/option_select/main.c#L57-L75).  
The content of this haxchi folder can be changed to your liking - if you want to you can also add in an alternative bootSound.btsnd to replace the original startup sound which I did not do in this example haxchi folder.  
After setting up the content to your liking all you have to do is run the haxchi .elf in homebrew launcher, select the game you want to install it on and that is it! If you ever want to make changes to the content folder it installed to then just re-run the haxchi .elf and install it again, you dont have to reinstall the game beforehand, it'll just overwrite the previous haxchi installation with your new data.  
Please note, this will ONLY WORK WITH DS VC GAMES ON NAND, if you have a ds vc game on USB you want to use then please move it to your NAND first and ideally detach your usb device before using this installer .elf, if you dont remove your usb devices it may freeze up on exiting or not install properly.  
This also ONLY LOADS THE .ELF VERSION OF THE HOMBEBREW LAUNCHER which as of right now is v1.4 so make sure to keep that on your sd card or you will just get error -5 when starting your haxchi channel. Once you are in the homebrew launcher it is also perfectly compatible with loading .rpx files, you just cant use haxchi itself to load .rpx files.    

[These games right now are supported by the installer.](installer/src/gameList.h#L14-102)  

## Dependencies

To properly compile this project yourself you will need the latest libiosuhax from dimok789's github.  

## credit

smea, plutoo, yellows8, naehrwert, derrek, FIX94 and dimok
