# Review Journal

The repository goal stays the same: package a Python local lab for lint analysis with transition tables, invalid-transition tests, and documented operating limits. This note explains the added review angle.

The local checks classify each case as `ship`, `watch`, or `hold`. That gives the project a small review vocabulary that matches its cli tools focus without claiming live deployment or external usage.

## Cases

- `baseline`: `file span`, score 158, lane `ship`
- `stress`: `terminal width`, score 124, lane `watch`
- `edge`: `argument risk`, score 172, lane `ship`
- `recovery`: `report density`, score 227, lane `ship`
- `stale`: `file span`, score 223, lane `ship`

## Note

This file is intentionally plain so the fixture remains the source of truth.
