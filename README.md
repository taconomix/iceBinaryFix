# iceBinaryFix
Modified bin file for AUR package ice-ssb-git

2 bugs found/resolved

Issue 1: Option for Brave Browser still appears readonly with Brave installed.
Fix: Changed "_BRAVE_BIN" path to "/usr/bin/brave" from "/usr/bin/brave-browser"

Issue 2: When only one compatible browser is installed, the isolate button will always read "Firefox is always isolated" and be readonly
Fix: Couldn't find the cause of this, everything looked like it should work in the section where the set_sensitive and set_active properties were set. I moved Firefox from the default to the second position, setting Brave as the default, and that appeared to resolve the issue. 

I tested the above fix with each compatible browser as the only one available, and everything seemed to work correctly. GNOME Web and Firefox both displayed the proper "always isolated" messages when they were the only browsers, all others gave the "Isolate the SSB" message and were clickable. It also works with any combination of available browsers. 
