# meridian-tool-lint-scope

`meridian-tool-lint-scope` keeps a focused Python implementation around cli tools. The project goal is to package a Python local lab for lint analysis with transition tables, invalid-transition tests, and documented operating limits.

## Project Rationale

The project exists to keep a narrow engineering decision visible and testable. For this repo, that decision is how file span and argument risk should influence a review result.

## Meridian Tool Lint Scope Review Notes

Start with `report density` and `terminal width`. Those cases create the widest score spread in this repo, so they are the best quick check when the model changes.

## Feature Set

- `fixtures/domain_review.csv` adds cases for file span and terminal width.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/meridian-tool-lint-walkthrough.md` walks through the case spread.
- The Python code includes a review path for `report density` and `terminal width`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Architecture

The fixture data drives the tests. The code stays thin, while `metadata/domain-review.json` and `config/review-profile.json` explain what each case is meant to protect.

The Python implementation avoids hidden state so fixture changes are easy to reason about.

## Usage

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Test Command

The check exercises the source code and the review fixture. `recovery` is the high score at 227; `stress` is the low score at 124.

## Next Improvements

The repository is intentionally scoped to local checks. I would expand it by adding adversarial fixtures before adding features.
