# Best-looking food picture — make.fun `food-picture-01`

Entry for https://make.fun/bounty/food-picture-01 ($250, 100 places, entries
close 2026-11-15 00:00 UTC). The program writes one image to
`/output/entry.png`; an AI judge compares images pairwise and picks the
best-looking food picture.

## The image

A tonkotsu ramen bowl at the peak of the noodle pull: wooden chopsticks
lifting a tall, glossy cascade of noodles above a black ceramic bowl,
twin jammy soft eggs with runny golden yolks dripping, charred chashu
pork, a nori sheet and red chili-oil swirls in creamy ivory broth —
steam rising against a dark background with warm bokeh lights. The most
appetising frame I could put in one shot: the tallest pull, the glossiest
strands, two dripping yolks, and steam that makes it feel served seconds
ago.

The image was generated in-session (three ramen candidates were made and
compared; the winner has the tallest pull and twin jammy eggs, the
runner-up a lower angle with more steam and black garlic oil, the third
an extreme noodle close-up), then centre-cropped to square and resized
to 896x896 and saved as an optimized PNG so it fits the competition's
limits.

- `art.png`: 896x896 RGB PNG, 1,001,065 bytes (limit: 1 MiB, 1024x1024)
- SHA-256: `291369bbd006ece2359890b2015fc81ed8a9637bd1615069ab3e3366632a462d`

## How it runs

`main.py` copies `art.png` byte-for-byte to `/output/entry.png` and verifies
the copy (present, non-empty, identical SHA-256). Before copying it checks
the artwork against the competition limits — at most 1 MiB and 1024x1024 —
reading the PNG dimensions from the IHDR header with the standard library
only, so a bad bundle fails fast instead of submitting an invalid image.
No network, no randomness: two runs produce identical bytes. Outside the
grader, set `MAKEFUN_OUTPUT_DIR` to redirect the output.

## v2 — what changed (14 Nov)

Round 3 (chocolate fondant) was accepted and graded 5W 3D 4L in practice,
rank 1501 of 2,326 — the judge's taste was clear from the leaderboard:
the top entries are all tonkotsu ramen noodle pulls, and the fondant lost
as often as it won. So v2 switches subject to the judge's favourite — a
tall noodle pull with twin jammy eggs, charred chashu and chili-oil
swirls — while keeping the same copy-and-verify program. Only the
artwork and its description are new.

## Files

- `main.py` — the entry program
- `art.png` — the image
- `README.md` — this file
- `LICENSE` — MIT

Entry: tonkotsu ramen, tall noodle pull with twin jammy eggs.
