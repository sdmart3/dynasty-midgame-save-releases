# Dynasty Midgame Save

**Quit a College Football 27 game whenever you like and pick it up later, right where you left off (PC).**

Life gets in the way of a close game. Dynasty Midgame Save lets you quit a game at any point and pick it up later, even days
later, right where you left off:

- **Every game is recorded.** At every snap Dynasty Midgame Save saves the quarter, the clock, both scores, who has the ball,
  the down and distance, the spot and the timeouts, plus the box score, injuries and fatigue.
- **Quit whenever you like.** Quit from the pause menu or close the game. The game is saved on the **Games** page as a
  suspended game.
- **Resume later.** Press **Resume** and start the same matchup again. The game begins right where you left off: same
  quarter, clock, score, down and spot, with the stats so far already in the game. No coin toss, no kickoff.
- **Your stats count.** The box score shows the whole game, and the season counts all of it. A player who got hurt in
  that game before you quit stays hurt.
- **See the saved stats.** Every saved game keeps its box score: passing, rushing, receiving, defense, kicking and
  punting, returns, snaps, team totals and injuries, one click away on its card.
- **Set up any situation.** A two-minute drill, a goal-line stand, a fourth-quarter comeback: type it in, and the next
  game you start (a dynasty game or Play Now) begins right there.
- **Drill a situation (Play Now, beta).** Put the same situation back again and again in the game you are playing:
  once, every snap, every few plays, or until a score or turnover. See **Drills**.
- **No defense (Play Now, beta).** The other team's players are moved off the field for each of your offensive plays, in
  a real game with a real crowd: for testing stadium, audio and presentation tweaks, or a drill without defenders. See
  **No defense**.

Dynasty Midgame Save has three parts, and the app installs all of them for you:

| Part | What it does |
|---|---|
| **Dynasty Midgame Save app** (`Dynasty Midgame Save.exe`) | The desktop app. You install Dynasty Midgame Save, resume games and set up situations here. |
| **Mod Manager plugin** | Starts Dynasty Midgame Save when you launch the game from the Mod Manager. |
| **Dynasty Midgame Save DLL** | Runs inside the game: records every snap and starts a resumed game where you left off. |

You don't need a `.fbmod`.

---

## What you need

- **College Football 27 on PC.**
- **The Mod Manager**, set up for College Football 27. Dynasty Midgame Save only runs when you start the game from the Mod
  Manager.

---

## Install

### With the app (recommended)

1. Close the game.
2. Unzip the Dynasty Midgame Save download anywhere you like (not into the Mod Manager or the game folder), then open
   `Dynasty Midgame Save.exe` in its `Dynasty Midgame Save` folder.
3. **Home** opens on **First-run setup**. Work through the steps:
   1. **Find the Mod Manager.** Dynasty Midgame Save looks for it on its own. If it guesses wrong or finds nothing, click
      **Choose the Mod Manager folder** and pick the folder that holds the Mod Manager program. If you pick the wrong
      folder, Dynasty Midgame Save tells you what you picked.
   2. **Install to the Mod Manager.** Click **Install Dynasty Midgame Save**. This copies the plugin and the DLL into the Mod
      Manager's `Plugins` folder. Nothing in the game folder changes. If the Mod Manager is open, close it and open it
      again so it loads the new plugin.
   3. **Launch the game from the Mod Manager**, the way you always do. This step ticks itself off once Dynasty Midgame Save
      reports in from the game (about 20 seconds after the game starts).
   4. **Play.** Recording is automatic: there is nothing to switch on.

The **Folders in use** card on Home shows each folder, with buttons to open, change or reset it.

### By hand

The download includes a `Manual install` folder with a `Plugins` folder inside. Copy that `Plugins` folder into your
Mod Manager folder, so that you end up with:

```
<Mod Manager folder>\Plugins\MidgameSavePlugin.dll
<Mod Manager folder>\Plugins\MidgameSave\          (midgamesave.dll, midgamesave.ini, plugin.cfg, README.txt)
```

If the Mod Manager already has a `Plugins` folder, merge into it. Don't replace it: other plugins live there too.

### If your Mod Manager is under Program Files

Windows only lets administrator programs write there. Home then shows **Dynasty Midgame Save needs permission to write to the
Mod Manager folder** with an **Allow Dynasty Midgame Save to write here** button: Windows asks you once, and that's it. Or move
the Mod Manager folder somewhere your account owns (for example `C:\Games`) and choose it again on Home.

The game itself runs as you, so it can't write there either. Dynasty Midgame Save notices and saves to
`%LOCALAPPDATA%\Dynasty Midgame Save\<a short code>\` instead; Home shows that folder with an **Open that folder** button, and
the app reads from it. If you'd rather keep everything in the Mod Manager folder, give your account write access to its
`Plugins` folder (Home shows the exact `icacls` command to copy into an administrator Command Prompt) or move the Mod Manager.

### Updating

When a newer app is ready to install, Home shows **Update ready** and an **Update Dynasty Midgame Save** button. Updating never
overwrites your settings: new settings are added to your `midgamesave.ini`, and a backup of everything that changes
goes to `%APPDATA%\MidgameSave\backups\` first. Close the game before you update, because the DLL can't be replaced
while the game is using it. The app also tells you when a newer release is out (see [Help](#help-and-bug-reports)).

---

## Suspend a game

You don't have to do anything. While Dynasty Midgame Save is installed and **Record games** is on (it is by default), every
snap is saved.

1. Play a game started from the Mod Manager. The top bar of the app shows **Recording**, and **Live** shows the
   scoreboard as Dynasty Midgame Save sees it.
2. Quit whenever you like: quit to the main menu from the pause menu, or close the game.
3. The app shows **Game suspended: Home 14, Away 7, Q2 5:00 saved**, and the game is on the **Games** page.

Notes:

- The game is saved as it was at the **last snap** before you quit. A play in progress when you quit is not part of
  it.
- **Super Sim:** the score, clock and situation are saved during a sim too (a few seconds after the sim stops or you
  pause). The stats catch up at the next snap you play, so after a Super Sim, play one snap before you quit.
- A game that reaches the final whistle is kept until you are back on your dynasty hub, then let go: its result is in
  your dynasty. If the game closes before you get back to the hub (a crash on the highlights screen or on Return to
  Hub, a freeze, or quitting to the desktop from the end screen), Games shows it as **Finished game that never reached
  your dynasty**, with **Finish this game** and **Dismiss**. See [A finished game that never reached your
  dynasty](#a-finished-game-that-never-reached-your-dynasty).
- Dynasty Midgame Save can't read the team names from the game yet, so the cards say **Home** and **Away**. Click **Name** on a
  card to call it, say, *Maryland vs Ohio State*.
- If the app was closed when you quit and you have not started another game since, Games shows **Found a recorded
  game** the next time you open it: **Keep** puts it in your library, **Discard** ignores it. Once another game starts,
  the game you quit goes to Games on its own (see [Does the app need to be open?](#does-the-app-need-to-be-open)).
- **Save this game now** on Live saves the game at any moment, without quitting.

### A finished game that never reached your dynasty

The dynasty takes a game's result when you are back on the hub after the final whistle. If the game closes before
that, the result may never reach your dynasty. Dynasty Midgame Save keeps such a game and shows it on **Games** marked
**Finished game that never reached your dynasty**:

- **Finish this game** opens the same Resume sheet as any saved game (Dry run is under Advanced, as always). The game
  starts again at the **last play call before the end**, with the stats and injuries up to then. You replay the final
  play or plays and the game ends normally, so the result reaches your dynasty. The replayed play can turn out
  differently from the first time.
- **Dismiss** puts it away (Show discarded keeps it for 30 days, with Undo).
- These cards are not counted in **Keep the last games**: they stay until you finish or dismiss them.
- A game that did reach the hub is never shown here. A game you quit before the final whistle is saved as before.

### Does the app need to be open?

No. Recording happens in the game: having Dynasty Midgame Save installed in the Mod Manager is enough. Open the app
whenever you like.

- Games you quit while the app was closed appear on the **Games** page the next time you open it, marked **Saved while
  the app was closed**. They are added for you (they are games you quit), and **Keep the last games** applies to them
  like any other.
- How it works: when you start the next game, Dynasty Midgame Save keeps the game before it (unless it reached the final
  whistle) in `Plugins\MidgameSave\pending\` in the Mod Manager folder, up to the 12 most recent. The app moves them into
  your library and clears that folder.
- The game you quit last, if no game has started since, shows as **Found a recorded game** instead.
- Arming a resume and starting a typed situation need the app.

---

## Resume a game

1. On **Games**, press **Resume** on the game.
2. The Resume sheet shows the saved situation, and under it what will happen: *When you start this game again, it
   begins right where you left off: same quarter, clock, score, down and spot, with the stats so far already in the
   game.* Choose:
   - **Carry stats**: puts your stats from before you quit back into the game, so the box score shows the whole game
     and the season counts all of it.
   - **Carry injuries**: a player hurt in this game before you quit stays hurt. A player who was already injured before
     kickoff is listed apart ("Already injured before kickoff") and left as he is.
   - **Advanced > Dry run**: goes through every check at the first snap but changes nothing in the game. The log on
     Live says what would have changed. Use it if you want to see what will happen first. While it is on, the button
     reads **Arm the dry run** and the sheet shows **Dry run: nothing will be written**.
   - **View saved stats** opens the box score saved with this game (see [Saved stats](#saved-stats)).
3. Press **Arm the resume** (or **Arm the dry run**). The game is now **Armed**, and Games shows **Resume in progress**
   with each step.
4. Start College Football 27 from the Mod Manager, and start **the same matchup, with home and away the same way
   round**.
5. The game begins right where you left off: the saved quarter, clock, score, down, distance, spot and timeouts, with
   the saved team on offense. There is no coin toss and no kickoff, and the box score already has everything from
   before you quit.
6. Play the game out. The card on Games says **Resumed** and what happened, and the season counts the whole
   game.

A few saved games can't start right at the saved moment: one saved at a kickoff or an extra point, or in overtime (and
any dry run). Then the game is put back where you left off at the first snap where the saved team has the ball: kick off
and play until then (a game saved in the second half waits until you sim or play into it). The sheet says so before you
arm it.

**Saved at a kickoff.** A kickoff has no down, so a game saved there can't start right at the saved moment. The Games
card and the Resume sheet say "Saved at a kickoff": a kickoff save in the 3rd or 4th quarter waits for the 2nd half
(sim or play into it), so the game starts at the coin toss and plays up to it; one in the 1st or 2nd quarter is put back
at the first scrimmage snap of that half where the saved team has the ball. To resume right away, save again at a
play-call screen (any 1st down after the kick).

If something does not look right, **Settings > Advanced** has two switches for troubleshooting, both on:
**Start right at the saved moment** (off: the game is put back at the first snap where the saved team has the ball,
as above) and **Stats in the game right away** (off: your stats from before you quit are added to the season when the
game ends instead, and the box score in the game shows only what you play after you resume).

Good to know:

- Dynasty Midgame Save applies **one resume per game launch**. If the game is already running and has used its resume, Dynasty Midgame
  Save asks you to quit the game and start it again.
- While a resume is armed, recording pauses, so the saved situation is not overwritten.
- **Cancel** (on Games or Live) disarms it and puts your recorded files back as they were. The saved game stays in
  your library.
- If the game refuses a resume (for example, you started the game in the second half of a game saved in the first),
  the card says why and the game is ready to try again.

---

## Saved stats

Every game saved with **Record stats** on keeps its box score. Press **Stats** on its card on **Games** (or **View
saved stats** in the Resume sheet) to see it. **Live** has the same view for the game you are playing now: **View
stats** on the Stats tile.

- The top of the sheet says when the stats are from (quarter, clock and score), when they were written, and how many
  players and injuries they hold. **Show** picks both teams, or just one.
- One tab per group: **Passing**, **Rushing**, **Receiving**, **Defense**, **Kicking & punting**, **Returns**,
  **Snaps** (downs played, pancakes, sacks allowed), **Team** (the two teams side by side) and **Injuries**. Click a
  column to sort by it; click it again to flip the order.
- **Home** and **Away** come from the score: Dynasty Midgame Save adds up each team's touchdowns, kicks and safeties and
  matches them to the scoreboard. When it cannot tell (a tied game, for example), the teams show by their game id.
- Positions show where they are certain. Defensive linemen show as **DL** and linebackers as **LB**.
- These are the stats from before you quit. When you resume with **Carry stats**, they go back into the game.
- After a Super Sim, the sheet says **Stats are as of the last snap you played**: the sim's plays are not in the box
  score until you play a snap.

The view only reads the saved file. Nothing in it changes your game or your season.

---

## Situations

The **Situations** page starts the next game you play at any situation, in a dynasty game or in Play Now. The game
begins right at the situation, with no coin toss and no kickoff, and the right team on offense.

A typed situation is used for one game; the game then records over it, so type it again (or open it from **Your
situations**) for the next game.

1. Pick a preset (**Two-minute drill**, **Goal line**, **Red zone**, **Fourth-quarter comeback**, **Overtime-like**,
   **Kneel-down practice**) or fill in the editor: quarter, clock, both scores, who has the ball, down, spot, yards to
   go and timeouts.
2. Leave a field blank (or choose **Leave**) and the game keeps its own value.
3. The **Preview** reads the situation back in plain words, for example *Q4 2:00, Home 21 - 24 Away, Home ball, 2nd & 7
   at own 35, timeouts 2/3*, and checks it: a clock longer than this game's quarters is refused, and so is overtime.
4. Press **Start this situation**, then start a game from the Mod Manager. With every field filled in, the game begins
   right at the situation; with a field left blank, it is set at the first snap where that team has the ball.

The spot is from the offense's point of view: *own 35* is the offense's own 35-yard line, *opp 8* is eight yards from
the end zone. **Save as...** keeps a situation by name; open it again from **Your situations**.

A typed situation never carries stats.

To repeat a situation in the game you are playing instead (Play Now only), see [Drills](#drills).

---

## Drills

> **Drill mode is a beta:** it has been tested in a few games; the possession flip, the timeouts fix and the hotkeys
> are off by default.

A drill puts a situation back into the game you are playing, again and again, so you can practise it: a two-minute
drill, a 3rd and 8, a goal-line stand. **Drills work in Play Now games against the CPU only.**

> **Never use drills in an online or rewards game: it can desync the consoles.** Dynasty Midgame Save cannot tell an
> online or rewards game from an offline one, so it asks you to confirm every time you start a drill.

1. On **Situations**, set up the situation as usual. A drill needs a quarter, who has the ball, a down and a spot.
2. Under the preview, pick how it repeats in **Repeat**:
   - **Once, in this game**: the next snap of the game you are playing is put at the situation. Press **Reset now** (on
     **Live**) or the Apply hotkey for another one.
   - **Every snap**: before every snap the game is put back at the situation.
   - **Every N plays**: after N plays from the situation it is put back (4 plays = a short series).
   - **Until a score or turnover**: play on until a score or a change of possession, then it is put back.
   - **Start of next game** is the usual typed situation (see [Situations](#situations)).
3. Press **Start the drill**, switch on **This is an offline Play Now game against the CPU**, and press **Start the
   drill** again. With a Play Now game on, it starts at the next snap; otherwise at the first snap of your next Play Now
   game.
4. **Live** shows the drill: how it repeats, the reps so far, the last result, when it was last put back and what it is
   waiting for. **Reset now** puts it back at the next snap; **Stop the drill** ends it (the game keeps going from where
   it is).

**Hotkeys.** On **Situations**, under **Repeat**, you can pick an **Apply now** key (put the situation back at the next
snap) and a **Stop drill** key. They are off until you pick one, and work with the game or the app in front. F-keys are
safest. If another program already uses the key, Live says so.

**Good to know.**
- A drill is set back at a snap where that team has the ball. After a score or a turnover the other team plays its
  possession first (or sim through it), then the drill comes back.
- The situation is put back before the play is called, so the play-call screen and the CPU see the drilled down, distance
  and spot. If that does not hold, it is put back at the snap instead.
- A drill stays in its quarter: when a rep runs out the quarter or the half, the drill stops. It also stops at the end of
  the game, when you start a new game (press **Reset now** to drill again), and when you stop it.
- A 3rd or 4th quarter drill started in the first half waits for the second half.
- **A drill never runs in a dynasty game**, and the game a drill runs in is never saved, resumed or added to a dynasty:
  your recording pauses for that whole game and starts again with the next one.
- A drill and a resume never run together: cancel an armed resume first, and stop the drill before you arm one.
- The box score, the line score and the time of possession keep every rep's plays.
- **Dry run** in the start sheet goes through every check at each snap but changes nothing; the log on Live says what
  would have changed.

### Known issues

- The first rep after the other team had the ball can show the old down, distance and spot on the play-call screen. The drill corrects it at the snap.
- **Until a score or turnover:** a drill reset after your own touchdown or an interception has not been seen in a real game yet (a field goal, a punt and the other team's score were tested).
- Drill games are never recorded, so there is nothing to resume. Drills work in Play Now games only, and in offline games only.

---

## No defense

> **Beta.** Plays end at a touchdown, out of bounds, a quarterback slide (X while scrambling), or a throw-away (R3 / throw it out of bounds). A runner you do not steer runs to a touchdown by himself. A quarterback who holds the ball in the pocket is never stopped. A running back's dive has not been confirmed. Offline Play Now only. Never use it in an online or rewards game.

At each of your offensive snaps, the other team's 11 players are moved off the field, the way the game's own **Offense
Only** practice does it, and put back after the play. Everything else is a normal Play Now game: the stadium, the
crowd, the scorebug, the commentary, the cameras and the replays. It is meant for testing stadium, audio and
presentation tweaks in a real game, and for running plays without defenders.

1. On **Situations**, under **Repeat**, tick **No defense (beta)**. It works with **Start of next game** (a whole game
   with no defense) and with every drill option.
2. Switch on **This is an offline Play Now game against the CPU** and press **Turn on No defense**.
3. Play your Play Now game. **Live** shows a **No defense** card: whether the defense was moved off at the last snap,
   how many plays so far, and why a snap was left alone. Its switch turns No defense on or off in the middle of a game;
   it takes effect from the next snap.

Turn Accelerated Clock off for No defense: with it on, the 15-second play clock can run out before you snap and the game gives delay-of-game flags.

How a play ends with nobody to tackle:

- Plays end at a touchdown, out of bounds, a quarterback slide (X while scrambling), or a throw-away (R3 / throw it out of bounds). A runner you do not steer runs to a touchdown by himself. A quarterback who holds the ball in the pocket is never stopped. A running back's dive has not been confirmed.

What keeps the defense:

- Kickoffs, extra points and 2-point tries, and every **4th down** (a punt or a field goal needs the other team; Dynasty
  Midgame Save cannot read which play you called).
- Every play of the CPU's possession: your defense plays as normal.
- A snap where the game's own possession is still changing hands, a game with a second player on the other team, and
  anything Dynasty Midgame Save cannot read: that snap is left alone.

Safety:

- **No defense never runs in a dynasty game**, and the game it runs in is never recorded, resumed or added to a dynasty
  (the stats of a game with no defense are not real). Your recording pauses for that game, even after you switch No
  defense off in it.
- No defense and a resume never run together: cancel an armed resume first, and switch No defense off before you arm
  one.
- The players are put back at the next play call (or the next snap), when you switch it off, and at the start of the
  next game.

### Known issues

- This is a beta: it has been played in one offline Play Now game so far (the defense moved off and put back on every
  play, no crash).
- Instant replays and audio with no defenders have not been checked yet.
- Players on the other team's sideline (the bench) can be seen; moved players are not seen on the field.
- A field goal or a punt on 1st to 3rd down is not detected: the other team is moved off for it too.
- The box score keeps every no-defense play (that is why the game is never recorded).

---


## Settings

| Setting | What it does |
|---|---|
| **Record games** | Saves the situation at every snap. On by default. |
| **Record stats** | Saves the box score, injuries and fatigue at every snap too (needed for Carry stats). On by default. |
| **Detailed log** | Writes every step to `midgamesave.log`. Leave it off unless something goes wrong. |
| **Carry stats by default** / **Carry injuries by default** | How the Resume sheet starts. |
| **Keep the last games** | How many saved games Dynasty Midgame Save keeps (20 by default). An armed game, and one resumed in the last 7 days, are always kept. |
| **Advanced** | **Start right at the saved moment** and **Stats in the game right away** (both on; switch one off only to troubleshoot, see [Resume a game](#resume-a-game)), dry run by default, injury weeks, patch safety and other troubleshooting options. The defaults suit almost everyone. |

Every switch takes effect within a second, even mid-game, except the ones marked **Next launch**.

**Start right at the saved moment** and **Stats in the game right away** follow the recommended setting while you
haven't changed them (they say **Default**), which may change in updates; once you change one, yours is kept (it says
**Your choice**, and **Use the default** next to it goes back to the recommended setting).

---

## Standing aside

If another tool in your Mod Manager already suspends and resumes games, Dynasty Midgame Save stays out of its way: it records
nothing and arms nothing, and Home says **Dynasty Midgame Save is standing aside**. Nothing breaks. To use Dynasty Midgame Save instead,
switch the resume settings off in the other tool, then restart the game from the Mod Manager.

---

## Known limits

- **Field direction.** A resumed game can go toward the other end zone than it did before you quit. Only the look of it
  changes: the score, the clock, the spot and the season are right.
- **The scoring summary.** The scoring plays from before you quit are listed with their score, type and quarter, but
  without the player who scored. The score, the box score and the season are right.
- **Team names.** Dynasty Midgame Save can't read the team names from the game yet: cards and the stats say **Home** and
  **Away** (name a game with **Name** on its card).
- **Fatigue.** Fatigue is saved with the box score, but a resumed game does not put it back: players start fresh.
- **Super Sim.** The stats catch up at the next snap you play, so after a sim, play one snap before you quit.
- **Positions in the stats.** Defensive linemen show as **DL** and linebackers as **LB**, because the exact spot (end or
  tackle, inside or outside) is not certain yet.
- **Drills** are a beta: Play Now only. The box score, line score and time of possession keep every rep;
  injuries and fatigue carry over from rep to rep; the timeouts on the scoreboard may lag a rep behind. Giving the ball
  back to the drill side after a score or a turnover (instead of playing the other team's possession) is built but off
  and not tested yet.
- **No defense** is a beta: offline Play Now only, never recorded. Plays end at a touchdown, out of bounds, a quarterback
  slide or a throw-away (a running back's dive has not been confirmed); 4th downs and kicks keep the defense.

---

## Troubleshooting

**Live says "Waiting for a game" while the game runs.** Make sure you started the game from the Mod Manager. Dynasty Midgame
Save loads about 20 seconds after the game starts. If you installed while the Mod Manager was open, close it and open
it again.

**A game I quit is not on Games.** Was Dynasty Midgame Save open when you quit? If not, open Games: the game shows as **Found a
recorded game**, or, if you have played another game since, as a card marked **Saved while the app was closed**. A game
quit before its first snap is not saved. A game that reached the final whistle is saved only if the game closed before
you were back on the dynasty hub: it shows as **Finished game that never reached your dynasty**.

**The resume did not happen.** Check that you started the same matchup with home and away the same way round. If the
game did not begin at the saved moment (for example a game saved at a kickoff), play until the saved side has the ball,
in the saved half. Live's **What Dynasty Midgame Save did** says what happened and what it is waiting for.

**The game says the resume was refused.** The card on Games says why. The most common reason is a game started past
the saved half. Resume it again and start a fresh game.

**Carry stats is greyed out.** The game was saved without stats (Record stats was off), or this game version does not
let Dynasty Midgame Save add stats yet. You can still resume the situation.

**`plugin.log` says "more than one CollegeFB27.exe" or "waiting up to 120 s".** The launcher relaunched the game and
two copies overlapped for a while. Dynasty Midgame Save waits up to `dup_wait_sec` seconds (default `120`, in
`plugin.cfg`) for one to go, then loads into the one that is left. If two are still running after that it picks the one
that is clearly the game (the only one with a visible titled window, else the child of the other, else the one with the
graphics modules loaded or far more memory) and loads there. If it cannot tell, it does not load and the message says
why; each candidate is listed in `plugin.log`, which is worth sending if you report it. `dup_wait_sec = 0` skips the
wait and `dup_pick = 0` turns the picking off, which is how 0.1.2 behaved. An old message like this shows on Live as
**Last launch** (muted, with its time) once the game is closed.

**Something else.** On **About**, use **Save diagnostics...** and **Report a problem** (below).

---

## Help and bug reports

- **Updates:** Dynasty Midgame Save checks for a new release at most once a day when it starts. It asks GitHub for the latest
  release and sends nothing about you or your PC. Switch it off on About; **Check now** works either way.
- **Save diagnostics...** (About, or the foot of Home) makes one zip with the Dynasty Midgame Save logs, its status and settings,
  and the last recorded situation. Your Windows user name is taken out of every path. It never includes your saves,
  your mods or anything from the game folder. You see exactly what is inside before you save it.
- **Report a problem** opens a new issue on GitHub with your versions filled in. Attach the diagnostics zip.

---

## Where things are

| Where | What |
|---|---|
| `<Mod Manager>\Plugins\MidgameSave\` | The DLL, `midgamesave.ini` (settings), `plugin.cfg`, the logs, and the files the game writes: `resume-last.ini` (the situation) and `resume-stats.ini` (the stats) |
| `<Mod Manager>\Plugins\MidgameSave\pending\` | Games you quit while the app was closed, and finished games that have not reached your dynasty hub yet, waiting for the app to add them to Games (it empties this folder) |
| `%APPDATA%\MidgameSave\games\` | Your saved games, one folder each |
| `%APPDATA%\MidgameSave\situations\` | Your saved situations |
| `%APPDATA%\MidgameSave\backups\` | What Install and Uninstall backed up |

---

## Uninstall

On Home, under **Installation**, click **Uninstall**. This removes the plugin and the DLL from the Mod Manager. Games still
waiting in the `pending` folder go into your library first. Your settings and the last recorded files go to a dated
folder in `%APPDATA%\MidgameSave\backups\`, and your saved games stay in the app. Close the game first. To remove everything, also delete the `Dynasty Midgame Save` folder you unzipped and
`%APPDATA%\MidgameSave`.
