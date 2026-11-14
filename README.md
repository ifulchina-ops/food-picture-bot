# Best-looking food picture — make.fun `food-picture-01`

Entry for https://make.fun/bounty/food-picture-01 ($250, 100 places, entries
close 2026-11-15 00:00 UTC). The program writes one image to
`/output/entry.png`; an AI judge compares images pairwise and picks the
best-looking food picture.

## The image

A chocolate fondant, cracked open so its molten centre spills across dark
slate, with gold leaf, fresh raspberries, a quenelle of vanilla ice cream
and a raspberry-coulis swirl — steam rising in warm, dramatic light. The
most appetising frame I could put in one shot: glossy flowing chocolate,
bright red berries against the dark plate, and steam that makes it feel
served seconds ago.

The image was generated in-session (three candidates were made and
compared; a steaming tonkotsu ramen bowl with a jammy-yolk egg was the
runner-up and a seared salmon fillet with asparagus third), then resized to
1024x683 and saved as an optimized PNG so it fits the competition's limits.

- `art.png`: 1024x683 RGB PNG, 848,140 bytes (limit: 1 MiB, 1024x1024)
- SHA-256: `7e7922ea6b6c644d5e31e41923fbd3dfb62ce0f30b3c1de8190fefc0a9d31848`

## How it runs

`main.py` copies `art.png` byte-for-byte to `/output/entry.png` and verifies
the copy (present, non-empty, identical SHA-256). Before copying it checks
the artwork against the competition limits — at most 1 MiB and 1024x1024 —
reading the PNG dimensions from the IHDR header with the standard library
only, so a bad bundle fails fast instead of submitting an invalid image.
No network, no randomness: two runs produce identical bytes. Outside the
grader, set `MAKEFUN_OUTPUT_DIR` to redirect the output.

## Files

- `main.py` — the entry program
- `art.png` — the image
- `README.md` — this file
- `LICENSE` — MIT
