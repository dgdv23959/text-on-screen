# Text on Screen

A romance quote generator for text-on-screen posts. Shuffle through 1,000 original,
gender-neutral lines, step back to the one before, and copy any line to the clipboard.

**Live site:** https://dgdv23959.github.io/text-on-screen/

## How it works

`index.html` is the entire site — one self-contained file with all 1,000 quotes inlined.
No build step, no dependencies, no server. Open the file locally or host it anywhere static.

- **Shuffle** deals from a shuffled deck, so no line repeats until all 1,000 have been seen.
- **Go back** walks the history; shuffling after going back re-walks what you already saw
  before dealing anything new.
- **Copy** puts the bare line on the clipboard.
- Keyboard: `space` shuffle, `←` back, `C` copy.

The background carries a faint colour wash that follows the emotional register of the
line on screen — warm for in-relationship, plum for longing, cool for breakup.

## The quote bank

1,000 lines across 10 categories (Modern Ache, Choose Over Chemistry, Small Proof,
Green Flag Reframe, Hard Truth, Classic Translated, Overheard, Addressed Letter,
LA Geography, Repair) and 3 emotional states (334 longing / 333 in-relationship /
333 breakup). Every line is original — no attribution needed.

## Editing the quotes

The quotes live in one `const BANK = [...]` array near the bottom of `index.html`.
Each entry is `[state, text]` where state is `0` in-relationship, `1` longing, `2` breakup.
