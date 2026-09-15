# ocsid-repo-skill

Install source for the `ocsid` repository-skill library (chemistry / molecular /
pharmaceutical / biomedical).

This repository intentionally contains **only** the skill content tree that
`ocsid repo-skills install` fetches. The CLI clones this repo and
sparse-checks-out `skills/repositories`:

```text
skills/repositories/
├── repo-skills/                  # repository-skill roots (SKILL.md + references/)
│   ├── repository-index.jsonl    # central repository index
│   └── <skill-id>/
└── repo-skills-router/           # area -> family -> repository router
    └── references/index/
        ├── taxonomy.json
        ├── repositories.jsonl
        ├── assignments.jsonl
        └── build-metadata.json
```

It does not carry the `cli/` runtime, installers, docs, or examples — those live
in `YitiAnz127/AREX-ocsid`.

## Usage

```sh
ocsid repo-skills install
```

The CLI reads the official repository from its bundled configuration; this
repository is the default source for the chemistry subset.

## Derivation

Derived from the AREX-Skill chemistry/biochemistry collection. It contains the
integrated `skills/repositories` subtree (109 repository-skill roots / 127
area-family memberships / 2 areas / 10 families). Generated and kept in sync by
`scripts/rebuild_router.py` in `AREX-ocsid`.
