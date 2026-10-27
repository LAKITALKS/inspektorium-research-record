# Inspektorium research record

This repository is the read-only research record behind
[Inspektorium](https://github.com/LAKITALKS/Inspektorium) up to release 0.2.0. It holds study
records, case packs, run records, publication logs and the historical source that produced them.
Maintained code and documentation live in the main repository.

## Provenance

- Source: [`LAKITALKS/Inspektorium@d086973`](https://github.com/LAKITALKS/Inspektorium/tree/d086973936d893e204dce426d23b35328d2a6c2c),
  the `main` commit after release v0.2.0 and its closeout (2026-10-26).
- `agent-arena/`, `publication/`, `LICENSE` and `NOTICE` are byte-identical to that commit, at the
  same paths. Paths in the 2026-10-26 import index therefore resolve here.
- `historical-docs/` holds the top-level documents of that commit and `docs/ONE_INSTRUMENT.md`. Their
  relative links were written for the main repository.
- `MANIFEST.sha256` lists the SHA-256 of every other file. It was checked against the Git blobs of
  `d086973` before publication: 4,229 files, 0 mismatches.
- One snapshot commit, tagged `record-2026-10-27`, then archived (read-only).

Verify a copy with:

```sh
shasum -a 256 -c MANIFEST.sha256
```

## Former working title

Until release 0.2.0, the audit runtime of Inspektorium was developed under the working title
"Agent Arena". The folder `agent-arena/`, the Python package `agent_arena` and the distribution
`agent-arena` carry that name. They are earlier identities of the same instrument, not a separate
product. From Inspektorium 0.3.0, the runtime is the subpackage `inspektorium.audit`; the main
repository's `docs/research/history.md` explains the transition.

## Contents

| Path | Content |
| --- | --- |
| `agent-arena/analysis/` | Study records: plans, freezes, raw records, analyses and validation evidence |
| `agent-arena/cases/`, `tasks/`, `runs/`, `reports/` | Case packs, task library, run records and generated reports |
| `agent-arena/research/` | Research workspace, early datasets and historical launchers |
| `agent-arena/historical-sources/` | Snapshots of the modules that produced important evidence |
| `agent-arena/agents/`, `docs/`, `*.md` | Agent configurations, contracts, closeouts and phase documents |
| `agent-arena/src/`, `tests/`, `examples/`, `scripts/` | Runtime source, its full test suite, examples and tools as of `agent-arena` 1.0.2, including modules that Inspektorium 0.3.0 no longer ships |
| `publication/` | Publication and verification records of 2026-10-26, including the import index |
| `historical-docs/` | Claims, methodology, research plan and results, roadmap, scope and checklists of Inspektorium 0.2.0 |

## Use

The historical evidence binds module paths and bytes of the versions that produced it.
Inspektorium 0.3.0 does not verify it. Use the release that matches the evidence:

| Version | Where |
| --- | --- |
| `agent-arena` 1.0.1 | Release [`agent-arena-v1.0.1`](https://github.com/LAKITALKS/Inspektorium/releases/tag/agent-arena-v1.0.1) |
| `agent-arena` 1.0.2 with `inspektorium` 0.2.0 | Release [`v0.2.0`](https://github.com/LAKITALKS/Inspektorium/releases/tag/v0.2.0) |

Install the downloaded wheels into a fresh virtual environment, for example
`python -m pip install inspektorium-0.2.0-py3-none-any.whl agent_arena-1.0.2-py3-none-any.whl`.

The historical test suite can also run from a clone of this record. From the repository root, in a
fresh virtual environment with Python 3.11 or newer:

```sh
python -m pip install -e './agent-arena[dev,providers]'
cd agent-arena
python -m pytest tests
```

Measured before publication on 2026-10-27 with Python 3.12.14 on macOS arm64 and the
commands above: 2,560 passed, 0 failed.

No authorization or budget in this record is active. The public authorization files are marked
`INERT_PUBLIC_ARCHIVE`. The launchers in `agent-arena/research/legacy-launchers/` can call model
providers and are not authorized by any release.

## License

The author's own code and documentation are licensed under the Apache License 2.0 (`LICENSE`),
as in the source commit. `NOTICE` lists the material that keeps its own rights: quoted third-party
texts, cited source excerpts, dependencies and rendering tools. Earlier release artifacts
(v0.1.0, v0.1.1, agent-arena-v1.0.1) remain under the license they were published with.

Author: Lazaros Varvatis.
