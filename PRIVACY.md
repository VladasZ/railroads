# Railroads: privacy of the feedback post

This page is about the feedback post of the Valheim mod Railroads. It says
what the post sends, where it goes, how long it stays and what you can do
about it. Nothing else in Railroads sends anything out of your game.

## Who gets the data

VladasZ, the author of Railroads. Reach me on the
[Railroads Discord server](https://discord.gg/6s9VY2hzBm).

## What goes, and when

A player writes a report at a feedback post and presses Send. A report holds:

- the text of the report and the contact the sender typed,
- the character name of the sender and the name of the world,
- the game logs of every player on the server who accepted the conditions
  at a feedback post, the sender included,
- the logs of the server.

The logs of a player are these files: `LogOutput.log` and `LogOutput.prev.log`
of BepInEx, `Player.log` and `Player-prev.log` of Unity, `rail-health.log`,
the Railroads config, the list of files in `BepInEx/config` and the configs
of performance mods. The files with `prev` in the name are from the run of
the game before, which may be another server or a single player world.
`rail-health.log` holds the hardware of the computer, the frame times, the
ping to the server and where the character stood in the game world.

Before a log leaves a game or the server, these are taken out of it: Steam
ids, Steam names, PlayFab ids, IP addresses with their ports and the user
name in file paths. Character names stay. The log of the server also names
the characters of players who did not accept the conditions, as it shows who
did what on the server.

Nothing leaves any game before the sender saw the list of what goes and
pressed Accept. A player who did not accept the conditions sends no logs.

## Why

Only to find and fix bugs in Railroads.

## On what grounds

Your logs go only with your consent, which you give at a feedback post with
Accept. You take it back there with Take back, and from then on your logs
stay on your computer. Your consent is kept in a file on your computer,
`BepInEx/railroads-feedback-consent.txt`, and counts on every server.

The character names in the log of the server are kept on the ground of a
legitimate interest: a bug between 2 players cannot be read without them.
You can object to it on the Discord server.

A server admin can turn the feedback post off for the whole server with the
setting `Feedback` in the section `Server` of `vladasz.railroads.cfg`.

## Where it goes and how long it stays

1. The server of the world. It keeps a copy until the Railroads backend has
   the report, for at most 1 day, then deletes it.
2. The Railroads backend at `blackforge.vladas.xyz`, reached through
   Cloudflare. It keeps the report and the IP address of the game server,
   which counts the daily limit of reports, for 30 days.
3. [Sentry](https://sentry.io), which stores the report in its region in
   Frankfurt, Germany, for 30 to 90 days.

## Your rights

You can ask to see a report with your logs, to have it deleted, or to have
it corrected. Every player whose logs went with a report sees its code in
the game. Write the code to me on the Discord server, and I answer within a
month. You can also complain to the data protection authority of your
country.

## Changes

A change of what goes or where it goes gets a new version of the conditions
in the game, and every player is asked again. The history of this file is
on GitHub.
