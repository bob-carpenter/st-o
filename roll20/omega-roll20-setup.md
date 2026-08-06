# Installing the Roll20 Sheet

1. Open your game's **Settings → Game Settings**.
2. Under **Character Sheet Template**, choose **Custom**.
3. Paste `omega-roll20.html` into the **HTML Layout** tab.
4. Paste `omega-roll20.css` into the **CSS Styling** tab.
5. Save. Open any character; the sheet is there.

You must be the game creator, and custom sheets require a Pro subscription on Roll20. If you don't have Pro, the fallback is to use the community **Blades in the Dark** sheet and rename things in your head — the dice mechanic is identical.

---

## How rolling works

Every roll button asks you for the **dice pool** from a dropdown rather than computing it. This is deliberate:

- It handles the 0-dice case correctly (`{2d6}kl1`, keep lowest), which computed pools break on.
- It absorbs push dice, assists, setups, and situational bonuses without any extra UI.
- Your rating is printed in the roll output so the table can see what you started from.

So: read your rating off the sheet, add whatever applies, pick that number. One extra click, no edge cases.

**Reading results.** The chat shows the kept die. Hover it to see all dice rolled — that's how you spot two 6s for a crit. Roll20's grouped-roll display doesn't flag crits automatically.

**Resist button.** Rolls your attribute and reminds you the stress cost is 6 minus your highest die. If your table uses the flat-cost method instead (1/2/3 by position), ignore the button and just mark stress.

---

## Attribute ratings are automatic

The sheet worker recomputes Insight, Prowess, and Resolve whenever you change an action dot. Rating = number of actions in that group with at least one dot, per the rules. Those fields are read-only on purpose.

---

## The ship

The ship block lives at the bottom of the same sheet. Make a character named `U.S.S. Enterprise`, fill in tier and the four systems, ignore everything above it. Same for a shuttle — Tier 0, use the Hull dropdown as its single harm track.

Roll20 only supports one custom sheet per game, so this is simpler than it looks.

---

## Things deliberately left out

- **Clocks.** Use Roll20's rollable tables or just draw them on the map layer. A sheet field for clocks is worse than a shared image.
- **Ability text.** The abilities box is a plain textarea. Paste in the two or three the player picked. A dropdown of seventy abilities is more work to maintain than it saves.
- **Stress/XP as checkboxes.** Number fields are fewer clicks and less markup. If your players want boxes to tick, say so and I'll swap them in.
