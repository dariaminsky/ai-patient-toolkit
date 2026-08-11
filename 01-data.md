# 01 — Your Data

If you read only one chapter of this guide, read this one.

Everything else — finding the right doctor, reaching researchers, evaluating options — depends on having your data in a form you can re-read, share, and reason about. Without it, every AI chat starts from zero, and every consultation wastes its first ten minutes.

Your records are probably scattered. The diagnosis sits with one hospital, scans with another, and labs with a third. A genetic test may be years old. Some consultations exist only in memory. Several countries or languages make the gaps worse. Every consultation and AI session starts with partial context.

A plain-text working folder gives you a current summary, a source index, and a version history. Keep the original records separate and unchanged.

## Why not just chat with an AI and let it remember?

Everyone asks this first.

Long chats can drift. The model builds a summary of you. That summary can slowly move away from your records.

A [2026 preprint](https://arxiv.org/abs/2605.12978) tested one kind of agent memory on ARC-AGI tasks. In one result, GPT-5.4 failed 54% of problems it had solved before memory consolidation. This covers one experimental setup. Treat it as a warning about automated rewriting.

Keep two separate stores:

- **raw records** — every report, every result, preserved untouched;
- **your summary** — the current-state file you maintain, in dated versions.

Keep the summary under your control. Keep the raw records as ground truth. Start fresh chats when the old one gets long. Add your current verified profile each time. Plain text also lets you switch models in minutes — you keep the substrate, you rent the model.

## Urgent care

Use this folder for organization and appointment prep. If a symptom may be urgent, contact local emergency services or your urgent-care line. Do not wait for an AI answer.

## Gather everything

Start with an inventory. List each document, scan, report, lab result, consultation note, and genetic test. Keep the originals in protected private storage.

Choose what the assistant may read. Approve the exact files first. Copy one document into the working folder when the task needs it. A local app can still send its contents to the AI provider for inference.

- Portal won't let you download? **Photograph the screen.**
- Paper documents? **Photograph each page.**
- Photos stuck on your phone? **Use AirDrop, Quick Share, a cable, or an encrypted drive.** Email creates another cloud copy.
- Doctor emails? **Save them as PDF** on your computer. If email is your only route, check who stores the message and for how long.
- Your own observations (symptoms, side effects, what helped)? **One text file, dated entries, added when you can.**

Leave identity documents — insurance cards, ID scans, policy papers — wherever you keep your passport.

You're building a working health summary. It gives an AI a better starting point. Your original records stay in charge.

## The `.md` format, in one minute

`.md` (Markdown) is plain text with simple structure — `#` for headings, `-` for lists. Any text editor opens it. Many assistants can read it. You can compare it version-to-version. A current-state file looks like this:

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
├── 00-current-state.md         # current profile; direct identifiers removed; still sensitive
├── source-index.md             # source IDs and protected locations of original records
├── care-team.md                # your doctors and clinics — kept separate, stays local
├── 01-diagnosis/               # verified transcriptions; approved working copies only
├── 02-treatment/               # what was done, when, outcome; doctor messages and notes
├── 03-genetics/                # clinically confirmed summaries; raw exports stay elsewhere
├── 04-decisions/               # one file per major decision
├── 05-side-effects/            # one file per side effect, with timeline
├── 06-research/                # papers read, researchers contacted
├── agents/                     # standing instructions for your AI assistant
└── 99-archive/                 # old profile versions (full-date names)
```

Keep raw originals outside the AI workspace by default. Record each protected location in `source-index.md`. Bring in one approved working copy when the current task needs it.

Start with `README.md`, `00-current-state.md`, and `source-index.md`. Add the rest as you go (full template in the [appendix](appendix/templates.md)). Share only the files needed for the current task.

**Transcribe the important parts yourself.** Dumping PDFs on a model and asking for a summary will eventually drop or misread a number — confidently. You type the key facts; the raw scan stays as ground truth. (If an AI assistant transcribes for you, verify every number against the original.)

## Mark every source

Use one source grade for every important fact:

- `[report]` — signed or final clinical report;
- `[lab]` — laboratory result;
- `[message]` — email, portal message, or chat;
- `[verbal]` — spoken information recalled by you;
- `[self-report]` — symptom or observation recorded by you.

Add the filename and page: `[lab | CBC-2026-03-15.pdf | p. 2]`. For verbal facts, add the speaker and date. Write `date unknown` when needed.

Treat OCR as a draft. Copy the value, unit, reference range, and decimal separator exactly. Keep `1,2` as `1,2` until a human confirms the format. If two records conflict, keep both. Mark the conflict. Never choose a winner silently.

## Genetic raw data

If you've done 23andMe, Ancestry, or similar, download your raw data while you have access. Store it in a protected location outside the AI workspace and git. Add a neutral reference to `source-index.md`. Genetic raw data identifies you very well.

A consumer result is a lead. Confirm it in a clinical laboratory before using it for care. Discuss pathogenic or likely pathogenic findings with a clinical genetics professional. Record the exact variant, laboratory, classification, and date.

Keep variants of uncertain significance (VUS) too. They can be reclassified. Record them for reference. Do not use a VUS to guide treatment. Add family history: relative, illness, and age where known.

## Versions

When your situation changes, save a dated copy (`00-current-state-v1-2026-04-15.md`) in `99-archive/`. Then update the current file. The series shows your trajectory.

Git is optional. Use it only after you understand it and say yes. Keep the repository local. Add no remote. Exclude raw records, images, PDFs, care-team details, source locations, and raw genetic exports.

Keep an encrypted backup on a second device or service you chose. Version history tracks changes; the backup protects against loss. Test that you can restore one file. Keep this folder off public GitHub.

## Privacy

- **Local storage is one layer.** The folder stays on your computer. The text or image you ask a cloud model to read can still go to its provider.
- **Approve every transfer.** Pick the exact files. Review any web query before it leaves the app.
- **Check the current policy.** Read retention, training, and deletion terms for your provider and plan. Turn off training where the setting exists.
- **Remove direct identifiers.** Strip names, full birth dates, record numbers, and hospital names when they are irrelevant. This lowers risk. Rare diagnoses, genetics, dates, and locations can still identify the case.
- **Treat the profile as sensitive.** Share it with a specific person or service for a specific task.
- **Keep credentials, IDs, and insurance numbers outside these files.**

Paid plans can still retain logs. Read the current retention policy.

## Records in several languages and countries

If your records span several languages, keep every original. Add a short translation above it. Mark the language and who translated it.

Treat AI translation as a draft. Verify doses, units, dates, anatomy, and every negation with a clinician or qualified medical translator before care decisions.

## Avoid

- Don't pile everything into one giant unstructured file.
- Don't keep medical data in shared workspaces (shared Drive, shared Notion).
- Don't let the cloud hold your only copy.
- Start with an incomplete, verified profile. Add to it over time.
- Never paste records or personal medical details into a public GitHub issue.
- If you use git, keep it local and without a remote.

## This week

- **Today, 15 minutes:** copy the starter folder and make a source index. Add one approved report. Draft 20 lines and verify them.
- **This week, 1–2 hours:** inventory the remaining records. Leave the originals in protected storage.
- **Next week, 1–2 hours:** transcribe the most important reports — diagnostics first, genetics next.
- **Ongoing:** something changed → new version. Something decided → a note in `04-decisions/`.

After a month, you should have a dated profile and a source index to use in appointments and AI sessions.

---

_More posts and ideas are in drafts now. I publish my thoughts in [Information Body](https://informationbody.substack.com) — subscribe if you'd like to be updated._
