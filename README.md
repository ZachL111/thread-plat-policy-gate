# thread-plat-policy-gate

`thread-plat-policy-gate` keeps a focused Java implementation around platform engineering. The project goal is to package a Java local lab for policy analysis with bounded scenario files, conflict explanations, and documented operating limits.

## Use Case

The point is to make a small domain rule concrete enough that a reader can change it and immediately see what broke.

## Thread Plat Policy Gate Review Notes

For a quick review, compare `secret scope` with `rollout width` before reading the middle cases.

## Highlights

- `fixtures/domain_review.csv` adds cases for rollout width and quota pressure.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/thread-plat-policy-walkthrough.md` walks through the case spread.
- The Java code includes a review path for `secret scope` and `rollout width`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Code Layout

The implementation keeps the scoring rule plain: reward signal and confidence, preserve slack, penalize drag, then classify the result into a review lane.

The Java code keeps the review rule close to the tests.

## Run The Check

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Regression Path

That command is also the regression path. It verifies the domain cases and catches mismatches between the CSV, metadata, and code.

## Future Work

The repository is intentionally scoped to local checks. I would expand it by adding adversarial fixtures before adding features.
