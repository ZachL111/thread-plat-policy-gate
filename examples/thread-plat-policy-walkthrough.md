# Thread Plat Policy Gate Walkthrough

This walk-through keeps the domain vocabulary close to the data instead of burying it in prose.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | rollout width | 163 | ship |
| stress | quota pressure | 188 | ship |
| edge | route drift | 213 | ship |
| recovery | secret scope | 242 | ship |
| stale | rollout width | 214 | ship |

Start with `recovery` and `baseline`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

`recovery` is the optimistic case; use it to make sure the scoring path still rewards strong signal.
