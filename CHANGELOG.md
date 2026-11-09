# Changelog

## 0.2.4

### New
- **Works with Dynasty Extensions' Spring Practice.** Dynasty Extensions 0.2.0 adds Spring Practice (beta): three
  practice weeks in the preseason, each with a drill game of five set situations that starts with a two-minute drill
  before the half. When both are installed, Dynasty Extensions hands the start of each drill game to Dynasty Midgame
  Save, which sets it up the same way it starts a saved game (no coin toss, no kickoff). The week-4 spring game is a
  normal game and is not handed over. With older Midgame Save versions the drill games play as normal games, so the
  two tools never fight over the game. Dynasty Extensions does not need Midgame Save: without it, Dynasty Extensions
  starts the drill games itself.
- The drill games are never recorded: they are not offered as saved games, and your own saved games and settings are
  left exactly as they were. If you have armed one of your saved games to resume (or a drill), Midgame Save says no to
  the hand-off and that drill game plays as a normal game. The Live page says when a drill game is running.

Nothing else changes. Normal games, Play Now, Situations, Drill and No defense work exactly as in 0.2.3.

## 0.2.3

### Fixed
- **Overtime now starts properly in a resumed or typed-in game.** If a game you resumed (or started from a situation on
  the Situations page) was tied at the end of the 4th quarter, overtime had no coin toss and the ball stayed where
  regulation ended. The setting that skips the opening coin toss stayed on for the whole game. It is now turned off at
  the first snap, so overtime gets its own coin toss and the ball at the opponent's 25.
- **A game saved right after a score now resumes at a touchback.** If you quit after a touchdown, field goal or safety
  and before the kickoff, the game used to start the other team on the yard line of the play that had just scored. Now
  the receiving team starts at its own 25, 1st and 10. After a safety, the team that scored receives the free kick.
  Saves taken in the middle of a drive are not changed, and neither are saves after a long sim. The log says when a
  save was turned into a touchback and why.
- **A Mod Manager under Program Files no longer leaves the app on "Not running".** Windows lets only administrator
  programs write to Program Files. The Mod Manager can install Dynasty Midgame Save there, but the game runs as you, so
  it could not write its log, its status or your saved games, and the app showed "Ready / Not running" forever. Now the
  game checks whether it can write to its own folder. If it can't, it saves to
  `%LOCALAPPDATA%\Dynasty Midgame Save\<a short code>\` instead, and the app reads both places. Home explains it in
  plain words, has an **Open that folder** button, and shows the one command that gives your account write access (to
  run yourself in an administrator Command Prompt), or you can move the Mod Manager out of Program Files. Repair and
  Update say the same thing. Nothing about the game changes if the folder is writable.
- **Two Mod Manager folders no longer leave the app on "Ready".** If you keep more than one Mod Manager folder (for
  example v1.1.0.6 and v1.1.0.7), the app now follows the one your game started from, and warns you when Dynasty Midgame
  Save is installed in more than one. The warning on Home and Live has buttons to use the folder your game started from
  or to open the other one, so you can remove the extra copy.
- **Works with the Oct 29 update.** The game's patch-check rows now include the Oct 29 build, so Dynasty Midgame Save hooks in as before.
- **Resumed games never pick up stats from a different game.** Saved stats now belong to the game they were taken in:
  a stats snapshot from another game is never saved, armed, loaded or carried into a resume.
- **Starts a little sooner.** Dynasty Midgame Save now loads about 20 seconds after the game starts (it was 30), so a quick
  Play Now start no longer misses the resume.

### New
- **Touchback buttons on Situations.** "Home ball" and "Away ball" fill in the ball, 1st down, the own 25 and 10 to go
  for either side. The quarter, clock and score you typed stay as they are.

## 0.2.2

### Fixed
- **Games and Resume now say when a save was taken at a kickoff.** A game saved at a kickoff has no down yet, so it
  cannot start right at the saved moment: it waits for the first scrimmage snap of the half it was saved in, and a game
  saved at a kickoff in the 3rd or 4th quarter waits for the 2nd half (so every relaunch starts at the coin toss). The
  Games card and the Resume sheet now say so ("Saved at a kickoff: waits for the 2nd half"), and the Resume sheet says
  how to resume right away: save again at a play-call screen (any 1st down after the kick).

### Changed
- Wording only. Nothing about how a resume works has changed, and the game DLL is the same apart from its version number.

## 0.2.1

**No defense (BETA).** No defense is a beta: it has been played in one offline Play Now game so far. It is off unless you
switch it on.

### New
- **No defense (beta, Play Now only).** On **Situations**, under **Repeat**, tick **No defense**: at each of your
  offensive snaps the other team's players are moved off the field (the way the game's Offense Only practice does it)
  and put back after the play. The stadium, the crowd, the scorebug, the commentary and the replays stay a normal Play
  Now game, so you can test stadium, audio and presentation tweaks in a real game. It works on its own (a whole game with
  no defense, Repeat set to **Start of next game**) and with every drill option. **Live** shows a **No defense** card
  with a switch to turn it on or off in the middle of a game.
- **How a play ends.** Plays end at a touchdown, out of bounds, a quarterback slide (X while scrambling), or a throw-away (R3 / throw it out of bounds). A runner you do not steer runs to a touchdown by himself. A quarterback who holds the ball in the pocket is never stopped. A running back's dive has not been confirmed.
- Turn Accelerated Clock off for No defense: with it on, the 15-second play clock can run out before you snap and the game gives delay-of-game flags.
- **Safe by design.** Kickoffs, tries and 4th downs keep the defense, and so does the CPU's whole possession. It never
  runs in a dynasty game; the game it runs in is never recorded, resumed or added to a dynasty; it and a resume never
  run together; you confirm an offline Play Now game against the CPU. Never use it in an online or rewards game.

### Known issues
- Instant replays and audio with no defenders have not been checked yet.
- Players on the other team's sideline (the bench) can be seen; moved players are not seen on the field.
- A field goal or a punt on 1st to 3rd down is not detected: the other team is moved off for it too.

## 0.2.0

**Drill mode (beta).** Drill mode is a beta: it has been tested in a few games; the possession flip, the timeouts fix and the hotkeys are off by default.

### New
- **Drill mode (beta, Play Now only).** On **Situations**, **Repeat** turns a typed situation into a drill in the game you are
  playing: **Once, in this game**, **Every snap**, **Every N plays** or **Until a score or turnover**. The situation is put
  back before the play is called, so the play-call screen and the CPU see the drilled down, distance and spot (at the snap
  instead if that does not hold). **Live** shows the drill (reps, the last result, what it waits for) with **Reset now** and
  **Stop the drill**, and two optional hotkeys (**Apply now**, **Stop drill**) work with the game or the app in front.
- **Safe by design.** A drill never runs in a dynasty game, the game a drill runs in is never saved, resumed or added to a
  dynasty (your recording pauses for that game), and a drill and a resume never run together. You confirm an offline Play
  Now game against the CPU every time: never use drills in an online or rewards game, it can desync the consoles.
- Off by default: giving the ball back to the drill side after a score or a turnover (the possession flip), the
  scoreboard timeouts fix and the hotkeys.

### Known issues
- The first rep after the other team had the ball can show the old down, distance and spot on the play-call screen. The drill corrects it at the snap.
- **Until a score or turnover:** a drill reset after your own touchdown or an interception has not been seen in a real game yet (a field goal, a punt and the other team's score were tested).
- Drill games are never recorded, so there is nothing to resume. Drills work in Play Now games only, and in offline games only.

## 0.1.3

- **Play Now:** typed situations now start without a coin toss or kickoff, like dynasty games, with the right team on
  offense.
- **Fixed: Dynasty Midgame Save no longer gives up when the game starts as two processes at once.** EA's launcher can
  start the game, let it exit some seconds in and start the real one later, so for a moment two `CollegeFB27.exe`
  processes overlap, and Dynasty Midgame Save refused ("could not hook the game: more than one CollegeFB27.exe is
  running (2)"). It now waits for the overlap to clear (up to `dup_wait_sec` in `plugin.cfg`, 120 seconds by default,
  logged in `plugin.log`), then loads into the process that is left. If two are still running after that, it works out
  which one is the real game from evidence (the only visible titled window, else the child of the other, else the one
  with the graphics modules loaded or far more memory, and never one that uses far less memory than the other) and loads
  only when that points at exactly one; otherwise it refuses and says why ("could not tell which of 2 CollegeFB27.exe
  processes is the game: ..."). `plugin.log` lists every candidate. `dup_pick = 0` turns the picking off.
- **An old "could not hook the game" is no longer shown as current.** When the game is not running, a failure left from
  an earlier launch shows on Live muted as "Last launch", with the time it was written.

## 0.1.2

### New
- **A finished game is safe until it reaches your dynasty.** After the final whistle, Dynasty Midgame Save keeps the
  game until you are back on your dynasty hub, then lets it go. If the game closes before that (a crash on the
  highlights screen or on Return to Hub, a freeze, or quitting to the desktop from the end screen), the game shows on
  **Games** as **Finished game that never reached your dynasty**. **Finish this game** starts it again at the last play
  call before the end, with the stats and injuries up to then: you replay the final play or plays and the game ends
  normally (the replayed play can turn out differently). **Dismiss** puts it away. These cards are not counted in
  **Keep the last games**.

## 0.1.1

### Fixes
- **Quit at the play-call screen and keep your last play.** The stats from the play you just ran are now saved as soon
  as the play-call screen comes up, so a game you quit (or crash out of) there resumes with that play in the box score,
  counted once.
- **The right team has the ball.** A game saved at the play-call screen right after a kickoff, a punt or a turnover could
  give the ball back to the team that just lost it. It now saves the team that has the ball.
- **Stats keep saving after an unfinished resume.** If you quit a resumed game before the final whistle, the next games
  you played saved no stats, so resuming one of them came back without its stats and the score by quarter on the end
  screen was wrong. Fixed: every game saves its stats again.

## 0.1.0

The first release.

### Suspend and resume games
- **Every game is recorded.** At every snap Dynasty Midgame Save saves the situation: quarter, clock, score, who has the ball,
  down, distance, spot and timeouts. It also saves the box score, injuries and fatigue.
- **Quit whenever you like.** Quit from the pause menu, or close the game. The game lands on the **Games** page as a
  suspended game, with the score, the clock, the down and distance and the stats so far.
- **Resume later, even days later.** Press **Resume**, then start the same matchup from the Mod Manager. The game
  begins right where you left off: same quarter, clock, score, down and spot, with the stats so far already in the
  game. No coin toss, no kickoff.
- **Carry stats and injuries.** Your stats from before you quit go back into the game, so the box score shows the whole
  game and the season counts all of it. A player who was hurt in that game before you quit stays hurt.
- A game saved at a kickoff, an extra point or in overtime is put back where you left off at the first snap where the
  saved team has the ball. The Resume sheet says so before you arm it.
- **Resume in progress.** While a game is armed, Games and Live show each step in plain words: armed, game started,
  back where you left off, your stats back in the game.
- **Save this game now** on Live saves the current game at any moment.
- **Saved stats.** Press **Stats** on a saved game to see its box score: passing, rushing, receiving, defense,
  kicking and punting, returns, snaps, team totals and injuries, sortable, for both teams or one. Live shows the same
  view for the game you are playing.
- A game that reaches its final whistle is never saved as suspended.
- **Found a recorded game.** A game recorded while Dynasty Midgame Save was closed is offered on Games: keep it or discard it.
- **The app does not need to be open.** Recording happens in the game. When you start another game, the one you quit
  before it is kept for the app, and Games shows it the next time you open the app (**Saved while the app was closed**).
- **Name your games and add notes.** Team names are not read from the game yet, so cards show Home and Away. Give a
  game a name like "Maryland vs Ohio State" and it shows on the card.


### Situations
- **Set up any situation** and start it at the next game: quarter, clock, both scores, the ball, down, spot,
  distance and timeouts. Leave a field blank and the game keeps its own value.
- **Six presets**: Two-minute drill, Goal line, Red zone, Fourth-quarter comeback, Overtime-like and Kneel-down
  practice.
- A live preview reads the situation back in plain words and checks it before you start it.
- Save situations by name and start them again with one click.

### The app
- **Home** walks you through setup in four steps and shows what Dynasty Midgame Save is doing now.
- **Live** shows the game as Dynasty Midgame Save sees it: the scoreboard, what is recorded, and the log.
- **Settings**: record games, record stats, the Resume sheet's defaults, how many games to keep, the theme, and
  advanced options. Under **Advanced**, two switches for troubleshooting, both on: **Start right at the saved moment**
  and **Stats in the game right away**. Switches you haven't changed follow the recommended setting, which may change
  in updates; once you change one, yours is kept.
- **Dry run**: go through every check at the first snap without changing anything in the game. The Resume sheet's
  button reads **Arm the dry run** while it is on, and the card says which kind of run it was.
- **Standing aside.** When another tool already suspends and resumes games in your setup, Dynasty Midgame Save stays out of
  its way and says so on Home.
- Install, update, repair and uninstall from Home. Your settings are never overwritten, and a backup is made first.
- An update check (at most once a day, can be switched off), **Save diagnostics** and **Report a problem** on About.
- Dark and light themes.
