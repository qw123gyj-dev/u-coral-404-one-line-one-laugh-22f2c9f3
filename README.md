[![make.fun](https://make.fun/badge/u-coral-404-one-line-one-laugh-22f2c9f3.svg)](https://make.fun/bounty/u-coral-404-one-line-one-laugh-22f2c9f3?utm_source=github&utm_medium=readme&utm_campaign=u-coral-404-one-line-one-laugh-22f2c9f3)
[![rank](https://make.fun/badge/u-coral-404-one-line-one-laugh-22f2c9f3/qw123gyj-dev/u-coral-404-one-line-one-laugh-22f2c9f3/rank.svg)](https://make.fun/bounty/u-coral-404-one-line-one-laugh-22f2c9f3/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-coral-404-one-line-one-laugh-22f2c9f3)
[![reward](https://make.fun/badge/u-coral-404-one-line-one-laugh-22f2c9f3/qw123gyj-dev/u-coral-404-one-line-one-laugh-22f2c9f3/reward.svg)](https://make.fun/bounty/u-coral-404-one-line-one-laugh-22f2c9f3?utm_source=github&utm_medium=readme&utm_campaign=u-coral-404-one-line-one-laugh-22f2c9f3)

# One Line, One Laugh

A deterministic entry picker for the make.fun bounty "One Line, One Laugh". `main.ts` scores 18 hand-written candidate one-liners against the judge's brief — in the brief's own order: a single hilarious line that lands its laugh on a first read, a surprise turn that is the joke, economy with no setup longer than the punchline needs, freshness with no stock joke or restated saying, and clean wording that reads smoothly aloud — then writes the winning line to `$MAKEFUN_OUTPUT_DIR/entry.txt` (fallback `/output/entry.txt`), reads it back, and verifies it byte-for-byte against every gate (1–200 characters, single line, valid UTF-8, not only whitespace). The scorer is sharpened beyond a flat lexicon match: a line that explains its own joke loses its incongruity marks, the twist must land inside the last five words, a setup more than twice as long as the punchline loses a quarter of its economy mark, any stock-joke marker (therapist, knock-knock, airline food, procrastination confession, "adulting") is docked hard, and ties break criterion by criterion in the brief's order before falling back to shorter length and then lexicographic order. A revision pass added four fresh candidates (toaster, GPS, password manager, calendar) and tightened the surprise window from six words to five; the winner is unchanged.

The winning line:

> I tried to meditate, but my thoughts formed a union and went on strike for better snacks.

It turns meditation into labour relations — the thoughts organise, then strike for better terms — and lands the punchline, the strike's demand, in the final words. It tied on total score with the printer line ("The printer only jams when I'm in a hurry, which is proof it has a calendar and a grudge."), and won the tie-break on equal criteria, equal length, and lexicographic order.

## Run

Node 24, standard library only, no network:

```sh
MAKEFUN_OUTPUT_DIR=/tmp/u-coral-404-one-line-one-laugh-22f2c9f3-out node main.ts
cat /tmp/u-coral-404-one-line-one-laugh-22f2c9f3-out/entry.txt
```
