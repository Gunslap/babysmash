BabySmash
=========

## This Fork
I created this fork to update the .NET Framework version used to .NET 7 (using the [.NET Upgrade Assistant](https://learn.microsoft.com/en-us/dotnet/core/porting/upgrade-assistant-overview?WT.mc_id=dotnet-35129-website)), which should make it easier to port to other OSes in the future (ie: Linux).
It compiles and runs fine, but I had to comment out some of the auto-updating functions that aren't available in .Net 7 and it still uses a few windows specific calls (ie: SpeechSynthesizer).

I forked [David Rieman's fork](https://github.com/DavidRieman/babysmash), has he had already made a few nice improvements and updated the Framework to .NET 4.8.

## Overview
The BabySmash game for small kids.  

As babies or children smash on the keyboard, colored shapes, letters and numbers appear on the screen and are voiced to help breed familiarization.

Baby Smash will lock out the Windows Key, as well as Ctrl-Esc and Alt-Tab so your baby won't likely exit the application, rotate your monitor display, and so on. Pressing ALT-F4 will exit the application and Shift-Ctrl-Alt-O brings up the options dialog.

Originally developed by Scott Hanselman, based on AlphaBaby. The version here contains some enhancements, but the original version is also available: http://www.hanselman.com/babysmash/

## Enhancements
This version of BabySmash includes at least the following enhancements over the original:
* Keypad typing now register as numbers typed, just like the number row.
* Bug fixes, including cleaner shutdown.
* Improved sound handling.
* Ovals are added to the roster of shapes (including Circle, Heart, Hexagon, Rectangle, Square, Star, Trapezoid, Triangle), letters, and numbers.

## AutoHotkey
Used in conjunction with a tool like AutoHotkey, you can essentially create a "baby lock hotkey" so you can baby-proof your PC inputs at a moment's notice, with this immersive application instead of just the boring Windows Lock Screen.  To set up:
* Download and install, if you don't already have it. Available for free at: http://www.autohotkey.com/
* Run AutoHotkey; for the first time, it will prompt if you want to edit the script. You do.
* If the script is not open, right-click the AutoHotkey taskbar icon (an 'H' icon) and select 'Edit This Script'.
* Choose a hotkey. Avoid relying on the Windows key, as it will be held while BabySmash starts and may be buggy when you exit BabySmash due to the way the key is intercepted. I like to use Control+Shift+Z.
* Code the hotkey. If you're using Control+Shift+Z, you can add "^+z::Run D:\GIT\babysmash\bin\Release\BabySmash.exe" right after the line "#z::Run www.autohotkey.com" (without quotes); Obviously your path to BabySmash.exe will vary depending on where you installed or built the code.
* Save the file and close your text editor.
* Right-click the AutoHotkey taskbar, and select 'Reload This Script'.
* Try out your new hotkey to make sure it works.  If not, go back to 'Edit This Script' and try again.

For more advanced customization, see also: http://ahkscript.org/docs/Tutorial.htm
