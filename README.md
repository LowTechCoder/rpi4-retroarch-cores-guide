# rpi4-retroarch-cores-guide


## Playstation graphical improvements
This is an optional change in RetroArch that could introduce some problems in some games, but for the games I play this is totally worth the tradeoff. Turning these on will improve the resolution and speed up the core.

> Run a game > In that games menu > Options > Enhanced Resolution (Slow) > [on]

This next one may not be needed with the added power of the Raspberry Pi 4, but keep it in mind if your game seems slow.  The biggest problem I run into this one is the save points in Tomb Raider are invisible if you turn this on.  Luckily RetroArch has save states you can use instead.

> Run a game > In that games menu > Options > Enhanced Resolution (Speed Hack) > [on]


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

## ScummVM Run-Ahead

Turn Run-Ahead off for ScummVM games. I don't see any issues with having it on except the warning message that pops up every time a ScummVM game is run.

