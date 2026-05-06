# Meridian Tool Lint Scope Walkthrough

The fixture is intentionally compact, so the review starts with the cases that pull farthest apart.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | file span | 158 | ship |
| stress | terminal width | 124 | watch |
| edge | argument risk | 172 | ship |
| recovery | report density | 227 | ship |
| stale | file span | 223 | ship |

Start with `recovery` and `stress`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

`recovery` is the optimistic case; use it to make sure the scoring path still rewards strong signal.
