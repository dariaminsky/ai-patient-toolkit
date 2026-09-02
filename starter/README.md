# Your health folder

These are your working files.

If you are reading this inside the toolkit repository, copy the folder to a private place first and rename the copy. Do not fill these templates inside the public repository.

Read `ai-patient-toolkit/02-privacy-and-safety.md` first.

## Start

1. Turn on device encryption.
2. Make an encrypted backup.
3. Check the chosen AI provider's training and retention controls.
4. Decide which single file the assistant may read first.
5. Get consent from the person whose records these are.
6. Add the protected location of the first record to `source-index.md`.
7. Fill `00-current-state.md` from formal records.
8. Mark anything written from memory as `UNVERIFIED`.

Put the originals in `original-records/` next to these files. Let the assistant read two or three at a time, after you approve them. Nothing in there gets edited.

## Growing the folder

These files are the flat starting set. Numbered subfolders — diagnosis, treatment, genetics, decisions, side effects, research, archive — get added as records accumulate. The full structure is in `ai-patient-toolkit/appendix/templates.md`.

## Files

- `original-records/` — your originals, as they came. Never edited.
- `00-current-state.md` — verified snapshot of the case.
- `source-index.md` — source IDs, protected locations, and approved working copies.
- `care-team.md` — names and contact details. Keep local.
- `decision-note.md` — one question, its evidence, and the clinician's decision. Copy this file for each new decision.
- `side-effect-log.md` — observations and advice received. Copy it per side effect when one log gets crowded.
- `agents/research-watch.md` — source-first research instructions.
- `agents/appointment-prep.md` — a short appointment agenda.
- `.gitignore` — a basic guard against committing raw files.

## Git

Dated copies are enough.

If you choose git, keep it local. Add no remote. Check with:

```sh
git remote -v
```

The command should print nothing.

The `.gitignore` reduces mistakes with untracked files. Remove sensitive files before the first commit. Keep a separate encrypted backup.

## Before each AI session

- Share the smallest useful file set.
- Review direct identifiers.
- State the exact task.
- Require source IDs for every extracted fact.
- Verify the output against the originals.
- Ask a clinician about medical meaning.

Urgent symptoms go to a clinician or local emergency service. Close the AI workflow.
