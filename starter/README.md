# Starter folder

Copy this folder to a private place on your computer. Rename the copy. Work there.

Do not fill these templates inside the public toolkit repository.

Read [`02-privacy-and-safety.md`](../02-privacy-and-safety.md) first.

## Start

1. Turn on device encryption.
2. Make an encrypted backup.
3. Check the chosen AI provider's training and retention controls.
4. Decide which single file the assistant may read first.
5. Get consent from the person whose records these are.
6. Add the protected location of the first record to `source-index.md`.
7. Fill `00-current-state.md` from formal records.
8. Mark anything written from memory as `UNVERIFIED`.

Keep raw records outside this working folder at first. Add one document at a time when you need it.

## Files

- `00-current-state.md` — verified snapshot of the case.
- `source-index.md` — source IDs, protected locations, and approved working copies.
- `care-team.md` — names and contact details. Keep local.
- `decision-note.md` — one question, its evidence, and the clinician's decision.
- `side-effect-log.md` — observations and advice received.
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
