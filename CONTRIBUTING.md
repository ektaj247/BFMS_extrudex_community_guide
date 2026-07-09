# Contributing

This documentation remains accurate only if the operators of the machine maintain it. All improvements are welcome, from typographical corrections to the replacement of documented settings.

## 1. Content restriction

**No Creative3DP materials may be contributed under any circumstances.** This includes STL files, wiring diagrams, bills of materials, assembly video content, and close paraphrases of the official guide. Pull requests containing such material will be closed without merge. See [NOTICE.md](NOTICE.md). All contributions must consist of the contributor's own words, photographs, and measurements.

## 2. Contribution categories

- **Setting revisions.** A proposed change to a documented temperature, speed, ratio, or procedure must be supported by evidence: the corresponding Experiment Log entry, diameter measurements, and where practical a photograph or test-print result. Unsupported observations belong in an issue, not a settings change.
- **Troubleshooting additions.** A symptom encountered, its confirmed root cause, and the corrective action that resolved it, in the format of [Troubleshooting, section 6.10](docs/06-troubleshooting.md).
- **Clarity revisions.** Confusion experienced by a new user is treated as a documentation defect; correcting the passage that caused it is a valued contribution.
- **Safety additions.** Highest priority; reviewed and merged first.

## 3. Editorial standard

- Write for a reader operating the machine for the first time.
- Present recommendations as the **current best-known method**, subject to revision — "current practice is X" rather than "X is required." Safety rules are the exception and are stated as requirements.
- When revising a recommendation, state the rationale in the pull request description so the repository history documents *why* practice changed.
- Preserve the separation of concerns: settings reside in [Materials and Temperature Settings](docs/03-materials-and-temperatures.md); supporting evidence resides in the [Experiment Log](docs/07-experiment-log.md); the two must cross-reference.

## 4. Process

1. **Minor corrections** (typography, wording): submit a pull request directly.
2. **Setting or procedure changes:** submit a pull request updating the relevant document **and** adding the supporting Experiment Log entry.
3. **Questions, ideas, unverified observations:** open an issue.
4. Limit each pull request to a single topic to expedite review.

## 5. Licensing of contributions

By contributing, you confirm that your contribution is your own original work and agree that it is licensed under the repository's [CC BY-SA 4.0](LICENSE) license.
