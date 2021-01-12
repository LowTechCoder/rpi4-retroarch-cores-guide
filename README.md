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


