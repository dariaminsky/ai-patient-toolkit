# 01 — Your Data

If you read only one chapter of this guide, read this one.

Everything else — finding the right doctor, reaching researchers, evaluating options — depends on having your data in a form you can re-read, share, and reason about. Without it, every AI chat starts from zero, and every consultation wastes its first ten minutes.

Your records are probably scattered: one hospital's diagnosis report, another's scans, labs from a third, a genetic test from years ago, consultations that exist only in memory — often across countries, languages, and healthcare systems that don't talk to each other. In that state your data can't be re-read by anything, can't be shared as one coherent picture, and can't be queried. The fix is not a database. It's a folder of plain text files that any AI can read directly.

## Why not just chat with an AI and let it remember?

The question everyone asks first, so here's the answer.

Long chats degrade. Over a long conversation the model builds its own summary of you, and that summary quietly drifts from your real records — while sounding more confident, not less. "Memory" features have the same flaw, and it's now documented: in [a 2026 study](https://arxiv.org/abs/2605.12978), an AI that solved a set of problems perfectly went on to fail 54% of those same problems after "consolidating" its experience into memory. The rewriting step itself is the failure mode.

So keep two separate stores, and never let anything collapse them:

- **raw records** — every report, every result, preserved untouched;
- **your summary** — the current-state file you maintain, in dated versions.

Nothing auto-rewrites the summary, and the summary never replaces the raw records. In practice: start fresh chats instead of continuing forever, paste your current file at the start, never rely on a vendor's memory feature for anything that affects treatment. Plain text also means you can switch models in minutes when the landscape changes — you keep the substrate, you rent the model.

## Gather everything

Before any structure: gather. Every document, scan, report, lab result, consultation note, genetic test. Chaos in one folder beats order across six portals — a folder can be handed to an AI with "read everything."

- Portal won't let you download? **Photograph the screen.**
- Paper documents? **Photograph each page.**
- Photos stuck on your phone? **Email them to yourself** (or AirDrop), then drag into the folder — your assistant can talk you through it.
- Doctor emails? **Forward them to one dedicated address** or save as PDF.
- Your own observations (symptoms, side effects, what helped)? **One text file, dated entries, added when you can.**

One exception to "everything": identity documents — insurance cards, ID scans, policy papers. They are not medical state; keep them wherever you keep your passport, not in this folder.

You're building what I call a *digital health twin* — a picture of your medical reality complete enough that any AI gives you specific, grounded answers about *your* case instead of generic ones.

## The `.md` format, in one minute

`.md` (Markdown) is plain text with simple structure — `#` for headings, `-` for lists. Any text editor opens it; any AI reads it instantly; it can be compared version-to-version; it will still open in thirty years. A current-state file looks like this:

```
# My current state

## Diagnosis

- [Your diagnosis, worded exactly as the official report words it]
- [Stage / severity / extent at diagnosis, if that applies]
- [Genetic findings, if any — the exact variant name]

## Active treatment

- [What, dose or schedule, current status]

## Current markers

| Date | CRP | ... |
| --- | --- | --- |
| 2026-03-15 | 1.2 | ... |
```

Mine is about a thousand lines after months of treatment. Yours starts at twenty — and twenty lines are already enough for the answers to stop being generic.

## One folder, simple structure

```
your-health/
├── README.md                   # what's in this folder
├── 00-current-state.md         # what's true RIGHT NOW — your health profile (no names: pasteable anywhere)
├── care-team.md                # your doctors and clinics — kept separate, stays local
├── 01-diagnosis/               # reports, imaging, lab results (labs-YYYYMMDD.md)
├── 02-treatment/               # what was done, when, outcome; doctor messages and notes
├── 03-genetics/                # raw genetic data, variant reports
├── 04-decisions/               # one file per major decision
├── 05-side-effects/            # one file per side effect, with timeline
├── 06-research/                # papers read, researchers contacted
├── agents/                     # standing instructions for your AI assistant
└── 99-archive/                 # old profile versions (full-date names)
```

Each numbered folder keeps its own `original-records/` subfolder for the untouched raw files, next to their plain-text transcriptions.

Start with just `README.md` and `00-current-state.md`; add the rest as you go (full template in the [appendix](appendix/templates.md)). PDFs and photos live in the sub-folders next to their plain-text transcriptions — but the part you and the AI re-read is the `.md`.

**Transcribe the important parts yourself.** Dumping PDFs on a model and asking for a summary will eventually drop or misread a number — confidently. You type the key facts; the raw scan stays as ground truth. (If an AI assistant transcribes for you, verify every number against the original.)

## Genetic raw data

If you've done 23andMe, Ancestry or similar — **download your raw data now** and save it in `03-genetics/`. Services re-analyze old samples as databases improve (that's how I got the email that became my first warning), get bought, or shut down. Document any pathogenic variant exactly as ClinVar writes it — the specific variant matters for treatment. Document variants of unknown significance too; they get reclassified. And write down family history: which relatives, which illnesses, what age. Nobody will re-collect that for you.

## Versions

When your situation changes meaningfully, don't edit history — save the old file with a version number and the full date (`00-current-state-v1-2026-04-15.md`) into the archive, and start the new version. After a year the series *is* your story, and a new doctor (or a new AI) can read the trajectory, not just the snapshot. If a coding assistant set up your folder with git, git's own diary of changes is enough and the archive copies become optional; either way the rule is the same: **nothing is ever overwritten.** And one rule in plain words: this folder must never go on the internet.

## Privacy

- **Paid accounts when possible** — free tiers are more likely to use your conversations for training. Check your provider's data policy, and opt out of training wherever the setting exists.
- **Major providers, not random health apps.** Clear policies, stable infrastructure.
- **Local first.** The folder lives on your computer; share copies per conversation rather than storing your files with the provider, and check what the provider retains. Keep your own backup.
- **Strip identifiers** from anything you paste into an ordinary chatbot: no names, birth dates, record numbers, hospitals. The model reasons just as well without them. This is why the profile keeps no names and your care team lives in a separate `care-team.md` — the profile stays safe to paste as-is.
- **Never** put credentials, IDs, or insurance numbers in these files — that's not medical state.

(Even paid providers typically keep conversation logs for some period for abuse monitoring — that's normal and different from training. Read the retention policy if the distinction matters to you.)

## Records in several languages and countries

If your medical life spans healthcare systems, languages, and continents, this method is where it pays off most: the folder becomes the only place where your whole story exists in one piece — portable across every border and every doctor. Keep originals in the source language; on top of each, add a short summary in whatever language you use with your doctors and your AI (English is a good default when records span several languages). AIs translate short medical documents well between major languages, and the original stays underneath as ground truth.

## What NOT to do

- Don't pile everything into one giant unstructured file.
- Don't keep medical data in shared workspaces (shared Drive, shared Notion).
- Don't let the cloud hold your only copy.
- Don't wait for perfect transcription before using AI — imperfect data now beats perfect data in three months.
- If you use git: the repository stays **private**. Never push medical records to a public repo.

## This week

- **Today, 15 minutes:** make the folder, write 20 lines of `00-current-state.md` from memory.
- **This week, 1–2 hours:** gather everything into it. Unorganized is fine.
- **Next week, 1–2 hours:** transcribe the most important reports — diagnostics first, genetics next.
- **Ongoing:** something changed → new version. Something decided → a note in `04-decisions/`.

A month in, you'll have a different kind of conversation with every doctor, every AI, and every researcher you ever talk to about your care.

---

_More posts and ideas are in drafts now. I publish my thoughts in [Information Body](https://informationbody.substack.com) — subscribe if you'd like to be updated._
