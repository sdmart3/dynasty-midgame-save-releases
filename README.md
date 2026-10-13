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
  game you start begins right there.

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
      reports in from the game (about 30 seconds after the game starts).
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
- A game that reaches the final whistle is not saved: there is nothing to resume.
- Dynasty Midgame Save can't read the team names from the game yet, so the cards say **Home** and **Away**. Click **Name** on a
  card to call it, say, *Maryland vs Ohio State*.
- If the app was closed when you quit and you have not started another game since, Games shows **Found a recorded
  game** the next time you open it: **Keep** puts it in your library, **Discard** ignores it. Once another game starts,
  the game you quit goes to Games on its own (see [Does the app need to be open?](#does-the-app-need-to-be-open)).
- **Save this game now** on Live saves the game at any moment, without quitting.

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

The **Situations** page starts the next game you play at any situation.

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
- **Super Sim.** The stats catch up at the next snap you play, so after a sim, play one snap before you quit.
- **The last play before you quit.** If you quit at the play-call screen, the game resumes after your last play, but
  that play's stats may be missing from the carried box score.
- **Positions in the stats.** Defensive linemen show as **DL** and linebackers as **LB**, because the exact spot (end or
  tackle, inside or outside) is not certain yet.

---

## Troubleshooting

**Live says "Waiting for a game" while the game runs.** Make sure you started the game from the Mod Manager. Dynasty Midgame
Save loads about 30 seconds after the game starts. If you installed while the Mod Manager was open, close it and open
it again.

**A game I quit is not on Games.** Was Dynasty Midgame Save open when you quit? If not, open Games: the game shows as **Found a
recorded game**, or, if you have played another game since, as a card marked **Saved while the app was closed**. A game
that reached the final whistle is not saved, and neither is one quit before its first snap.

**The resume did not happen.** Check that you started the same matchup with home and away the same way round. If the
game did not begin at the saved moment (for example a game saved at a kickoff), play until the saved side has the ball,
in the saved half. Live's **What Dynasty Midgame Save did** says what happened and what it is waiting for.

**The game says the resume was refused.** The card on Games says why. The most common reason is a game started past
the saved half. Resume it again and start a fresh game.

**Carry stats is greyed out.** The game was saved without stats (Record stats was off), or this game version does not
let Dynasty Midgame Save add stats yet. You can still resume the situation.

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
| `<Mod Manager>\Plugins\MidgameSave\pending\` | Games you quit while the app was closed, waiting for the app to add them to Games (it empties this folder) |
| `%APPDATA%\MidgameSave\games\` | Your saved games, one folder each |
| `%APPDATA%\MidgameSave\situations\` | Your saved situations |
| `%APPDATA%\MidgameSave\backups\` | What Install and Uninstall backed up |

---

## Uninstall

On Home, under **Installation**, click **Uninstall**. This removes the plugin and the DLL from the Mod Manager. Games still
waiting in the `pending` folder go into your library first. Your settings and the last recorded files go to a dated
folder in `%APPDATA%\MidgameSave\backups\`, and your saved games stay in the app. Close the game first. To remove everything, also delete the `Dynasty Midgame Save` folder you unzipped and
`%APPDATA%\MidgameSave`.
