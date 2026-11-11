# Reference template and delivery checklist

This folder is the reference implementation for work packages delivered to this
repository. Copy its layout for new packages.

## Required layout

Each work package lives at `contributions/<contributor>/<package>/` on a contributor
branch named `contrib/<contributor>`. The Owner of a package is the contributor
directory name (the segment directly under `contributions/`).

Within a package:

- `README.md`
- `USAGE.md`
- `CHANGELOG.md` (optional)
- `automation/run_checks.py` (mandatory)
- `quality/export.json` (QA export, mandatory)

## Acceptance checklist

A package is evaluated against ALL of the following rules. The readiness status is
derived only from these rules.

Content checks (file contents are inspected):

1. `README.md` must exist and be non-empty, and must contain English text only.
2. `USAGE.md` must exist and be non-empty, and must contain English text only.
3. `CHANGELOG.md` is optional. When present and non-empty it must contain English
   text only. An absent or empty `CHANGELOG.md` is acceptable.

Structural checks (only file existence is checked; the content of these files is not
inspected):

4. `automation/run_checks.py` must exist at exactly that relative path.
5. `quality/export.json` must exist at exactly that relative path.

Quality gate:

6. The package must have no open blocking findings of its own. The tracker column
   `Blocking Findings` is defined in the Delivery Metrics Glossary in the team
   workspace. `quality/export.json` stores raw statistics keyed without display
   labels, so resolve the column through the glossary.

A package is `Complete` only when checks 1-6 all pass. Otherwise it is `In Progress`.
