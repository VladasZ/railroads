# Railroads: privacy of the feedback post

This page is about the feedback post of the Valheim mod Railroads. It says
what the post sends, where it goes, how long it stays and what you can do
about it. Apart from the feedback post, Railroads sends only what the game
itself needs between players and the server: the state of trains, and a
horn sound file of your own to the server and the other players when you set
one. Those are not sent to the author.

## Who gets the data

VladasZ, the author of Railroads. Reach me on the
[Railroads Discord server](https://discord.gg/6s9VY2hzBm) or at
blackforge.game@gmail.com. Reports are read by hand, no AI tool reads them.

## What goes, and when

A player writes a report at a feedback post and presses Send.

A sender who has not accepted the conditions on this server sends only the
text and the contact they typed, and the version of Railroads. The contact can
be empty. No logs, no character name and no world name go with such a report,
and no logs of other players. It still passes through the server of the world
and reaches the backend from the address of that server, see below.

A sender who accepted sends:

- the text of the report and the contact the sender typed, as they typed them,
- the character name of the sender and the name of the world,
- the game logs of every player on the server who accepted the conditions
  at a feedback post on this server, the sender included,
- the logs of a dedicated server, unless the sender took that tick off.

The owner of a server chooses with the setting `FeedbackServerLogs` whether
its log goes whole or with only the lines of Railroads and all errors.

The logs of a player are these files: `LogOutput.log` and `LogOutput.prev.log`
of BepInEx, `Player.log` and `Player-prev.log` of Unity, `rail-health.log`,
the Railroads config, the list of files in `BepInEx/config`, the configs of
performance mods, and a small file with the date and the version of the yes.
The files with `prev` in the name are from the run of the game before, which
may be another server or a single player world.

Each player chooses with 3 ticks at a feedback post whether the logs of the
last run go, whether `Player.log` goes, and whether all other log lines go or
only errors and the lines of Railroads. All 3 are on until a player takes them
off.

These logs can hold facts about the computer: the system, the processor, the
memory, the graphics card and its settings, the screen and a VR headset. They
hold the mods a player runs, the times of events, where the character was, the
ping and how the player connects. Railroads writes such lines every minute
into `LogOutput.log` and `rail-health.log`, which keeps the last 3 runs. These
files stay on your computer until a report takes them. The setting
`HealthLines` turns these lines off.

Before a log leaves a game or the server, these are taken out of it: Steam
ids, Steam names, PlayFab ids, IP addresses with their ports, e-mail
addresses, the name of the computer, the save folder and the user name in file
paths. The filter
works by patterns and can miss what it does not know.

The server then replaces the names of characters with no yes with a label,
like `player 3`, in every file and note of the report. The label stays the same
through 1 report. Character names of players who accepted stay. A name the
server and the logs do not show as a character name can stay, for example in
a log of the run before from another server.

Nothing leaves any game before the sender saw the list of what goes and
pressed Accept. A player who did not accept the conditions on this server
sends no logs. Your game tells you itself each time your logs start to go, with
the code of the report.

## Why

Only to find and fix bugs in Railroads.

## On what grounds

Your logs go only with your consent, which you give at a feedback post with
Accept. It counts for your account and for that server only. Another account
on the same computer and another server ask again. You take it back at a
feedback post with Take back, and from then on your logs stay on your
computer, also when they were already on their way. Your consent is kept in a
file on your computer, `BepInEx/railroads-feedback-consent.txt`. Each report
holds the date and the version of the consent of each player whose logs went
with it.

A server admin can turn the feedback post off for the whole server with the
setting `Feedback` in the section `Server` of `vladasz.railroads.cfg`.

## Where it goes and how long it stays

1. The server of the world. Its owner can read the copy while it is there. It
   keeps a copy until the Railroads backend has the report, for at most 1 day,
   then deletes it.
2. The Railroads backend at `blackforge.vladas.xyz`, reached through
   Cloudflare, which sees the IP address of the game server. The backend does
   not store that address. It keeps the report and a hash of the address for
   30 days, to count the daily limit of reports. The key of the hash is random
   and is not stored, so the address cannot be read back from it.
3. [Sentry](https://sentry.io), which stores the report in its region in
   Frankfurt, Germany, for 30 to 90 days.

## Your rights

You can ask to see a report with your logs, to have it deleted, or to have
it corrected. Every player whose logs went with a report sees its code in
the game, once the backend has the report. Write the code to me on the Discord server or to
blackforge.game@gmail.com, and I answer within a month. You can also complain
to the data protection authority of your country.

## Changes

A change of what goes or where it goes gets a new version of the conditions
in the game, and every player is asked again. The history of this file is
on GitHub.
