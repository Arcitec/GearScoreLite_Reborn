# GearScoreLite: Reborn

Helps you quickly and easily judge a player's level of gear.

The GearScore algorithm gives you a good indication of the player's actual power level. Every item slot is intelligently weighted by how important and powerful each slot is; for example, a high level chest piece is "more powerful and provides more stats" than a high level belt, so the chest is "worth a higher score".

This intelligent weighting makes it much more useful than simply looking at the "average item level", since it's impossible to "cheat" the score by just wearing a few weak, high-level pieces in low-impact armor slots.

GearScoreLite Reborn is an improved version of the addon, with many important bug fixes and new features.

For World of Warcraft 3.3.5.

## What's New:

- Based on the final, official GearScoreLite version (3x04).
- Lots of bug fixes (see commit history if you want details).
- Added support for ElvUI, Shadowed and VuhDo unit frames.
- More readable GearScore font size in your own personal character window.
- No longer attempts to calculate GearScore for anyone while an Inspect window is open (either Blizzard's, or the popular Examiner addon). This fixes the bug where the Inspect window constantly changes contents and displays random talents and gear, due to GearScore triggering the "inspect" API for other people, which confuses the game.
- Removed the completely broken "enchant score" algorithm, which generated nonsensical results. It was the final feature added by the original author back in 2010, and it has never worked. Older community forks of this addon have also removed that broken algorithm, so this simply ensures that we're all using the same GearScore calculations. It was pointless anyway, since GearScore cannot inspect gems (which are more important), so why bother trying to inspect enchants? Not only was it broken, but it didn't even check if the enchant was good. If you actually care about their enchants and gems, you should do a normal inspect to ensure that they're using the correct gems and enchants for their role and talent spec!
- Added a hidden "Must Target" mode, where it won't attempt to calculate GearScore for anyone unless you're already targeting them. This means that you have to click the person to target them, and *then* you'll see their GearScore. It reduces clutter in the tooltips and decreases UI lag. This mode is off by default, meaning that everyone will be inspected on mouseover.

You can enable the secret "Must Target" mode by running the following command:

```
/run GS_Settings["MustTarget"] = true
```

Replace `true` with `false` if you want to disable this feature again.

Have fun!
