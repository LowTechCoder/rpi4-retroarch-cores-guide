# Raspberry Pi 4 RetroArch Cores Guide


## Playstation
### Graphical Improvements
This is an optional change in RetroArch that could introduce some problems in some games, but for the games I play this is totally worth the tradeoff. Turning these on will improve the resolution and speed up the core.

> Run a game > In that games menu > Options > Enhanced Resolution (Slow) > [on]

This next one may not be needed with the added power of the Raspberry Pi 4, but keep it in mind if your game seems slow.  The biggest problem I run into this one is the save points in Tomb Raider are invisible if you turn this on.  Luckily RetroArch has save states you can use instead.

> Run a game > In that games menu > Options > Enhanced Resolution (Speed Hack) > [on]
### Games not working
If your game isn't working, theres a good chance you will need to search around the internets to find what's called a BIOS file.  
Retropie has good documentation on which cores needs which BIOS files:  
https://retropie.org.uk/docs/Playstation-1/. 
Heres the ones I found that worked the best for me.  I just added them all, and the emulator should choose the best.  
scph5500 - 3.0 NTSC-J
scph5501 - 3.0 NTSC-U/C
scph5502 - 3.0 PAL

If you place those BIOS files on a thumbdrive, here is the command to copy those to the correct directory. Replace RA-DATA with your thumbdrive and if you have different named BIOS files than I used,replace 'scph550*' with the name of the BIOS file.
```
cp /media/pi/RA-DATA/scph550* /home/pi/snap/retroarch/427/.config/retroarch/system/
```

## Nintendo - Game Boy Advance (VBA Next)

This core you may encounter some audio issues if the Run ahead mode is on or too high. So turn it off or turn the Number of Frames to Run-Ahead down to 1.

> Settings > Latency > Run-Ahead to Reduce Latency > [on]

> Settings > Latency > Number of Frames to Run-Ahead > [1]

> Settings > Latency > Use Second Instance for Run-Ahead > [off]

> [Game Running] > Overrides > Save Core Overrides

## ScummVM importing issues

If ScummVM gives you issues on the import like Curse of Monkey Island did for me, you may can try this.

Since RetroArch ignores some files while using the Manual Scan, with the Raspberry Pi File Manager, find the directory where the game file is. For me it was an AUTORUN.INF file. Remember where that path is.

> Import Content > Manual Scan > Content Directory > [the path you found above]

> ... System Name > [ScummVM]

> ... Default Core > [ScummVM]

> ... File Extensions > [this didn't work for me, so leave this empty]

Scanning Recursively cluttered up my ScummVM Playlist with about 100 files, so lets turn this off.

> ... Scan Recursively > [no]

Select 'Start Scan'

Now that should have added your game along with a few other unwanted files to the ScummVM playlist.  Lets clean that list up by selecting each of those files you don't need and select 'Remove'

Ok, you can be done at this point, but I like to take it further and Rename that AUTORUN file in my ScummVM playlist.

> ScummVM > [Game] > Rename [Curse of Monkey Island]

Save those settings.

> Main Menu > Configuration File > Save Current Configuration

More ScummVM information:

https://docs.libretro.com/library/scummvm/

## ScummVM Run-Ahead

Turn Run-Ahead off for ScummVM games. I don't see any issues with having it on except the warning message that pops up every time a ScummVM game is run.

> [Game Running] > Latency > Run-Ahead to Reduce Latency > [off]

> [Game Running] > Overrides > Save Core Overrides


