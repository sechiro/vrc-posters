# vrc-posters

Poster images served via GitHub Pages for the VRChat poster display demo (vrc-dynamic-image-compression).

- `posters/`: PNG without alpha channel, 1448x2048 (portrait) recommended.
- GitHub Pages URL: `https://sechiro.github.io/vrc-posters/posters/<file>.png`

## slides/

Lecture slides for the LightWeightTalkroom (ことのはアーク) cafe slide screen.

- `slides/slide_NN.png`: fixed two-digit sequence starting at `slide_01.png`.
- 2048x1152 (16:9), PNG **without alpha channel** (RGB). Both edges are multiples of 4, so BC1 / ASTC 4x4 need no edge padding.
- URL: `https://sechiro.github.io/vrc-posters/slides/slide_NN.png`
- GitHub Pages serves with `Cache-Control: max-age=600`; a replaced file is picked up by new downloads within ~10 minutes.

### Decks

The world declares three deck folders: `slides/`, `slides_b/`, `slides_c/` (same layout each).
Each folder has a `count.txt` holding the number of slides (one integer). The world reads it at
join and when the presenter presses 再読込; pages beyond the count are never requested.
Swap a deck's content by replacing the PNGs and `count.txt`, then push.
