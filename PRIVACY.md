# Railroads: privacy

Railroads sends nothing to the author and makes no connection to the internet.

## What goes to other players

Railroads sends only what the game needs between players and the server: the
state of trains, and a horn sound file of your own to the server and the other
players when you set one.

## What stays on your computer

Railroads writes lines for a report of lag into `LogOutput.log` and
`rail-health.log`: the system, the frame times, where your character is and the
ping. On a server they also name the players and their ping. These files never
leave your computer by themselves. You can add `rail-health.log` to a bug report
on [blackforge.vladas.xyz](https://blackforge.vladas.xyz/feedback/bugs/new/Railroads)
yourself, the [privacy page of the site](https://blackforge.vladas.xyz/privacy)
covers what you send there. The setting `HealthLines` turns these lines off.
