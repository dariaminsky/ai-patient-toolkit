# 02 — Privacy and safety

Read this before an assistant opens a medical file.

## Get consent first

The person whose records these are controls access.

Before reading a raw file, the assistant must say:

- which file it needs;
- what it will extract;
- which provider will process the content;
- whether another tool, connector, or web search will receive anything;
- what will be written back to the folder.

Wait for a clear yes. Ask again before changing providers, adding a connector, running a web search, or creating a schedule.

A caregiver needs the patient's permission. Record that permission in the private folder. Keep it out of prompts and public tools.

## Know where the content goes

Cloud assistants process content on provider systems. The original file may stay on your computer. Selected text, images, prompts, and outputs can still leave it.

Check the exact product and plan. Look for:

- model-training controls;
- retention and deletion periods;
- possible human review;
- processing region;
- connector and plugin access;
- rules for health data.

Policies change. Save the link and the date you checked it.

Call a workflow local only when the model runs locally and network access is off.

## Share less

Start with one file. Add another only when the task needs it.

Remove direct identifiers where they add no clinical value:

- full name;
- full date of birth;
- address, email, and phone;
- medical-record, insurance, and account numbers;
- faces, signatures, barcodes, and QR codes;
- clinic and staff names when they are irrelevant.

Review every redaction yourself. AI misses identifiers.

Removing names lowers the risk. Rare diagnoses, genetic variants, exact dates, and locations can still identify a person. Treat every health profile as sensitive.

Keep raw documents out of web searches, connectors, public issues, and public repositories. Use the smallest search query that can answer the question. Show the query before sending it.

## Store it safely

Plain text has no built-in encryption.

- Turn on full-disk encryption.
- Use a strong device login and automatic screen lock.
- Keep the folder out of shared accounts.
- Check cloud-sync settings before adding medical files.
- Keep an encrypted backup.
- Test that the backup can be restored.

Keep the encrypted backup separate from version history. A drive can fail. A folder can be deleted. Git history can be changed.

Git is optional. Ask before initializing it. Keep a health repository local and add no remote. Run `git remote -v` and show that it is empty. Exclude raw records, genetic exports, identity files, `care-team.md`, and `source-index.md`.

`.gitignore` only prevents some new mistakes. A file already committed can remain in history. Never push a health folder to GitHub, GitLab, or another remote.

Use dated local copies when git feels like extra work.

## Build from sources

Give every clinical fact a source ID and date.

Use clear source types:

- formal report;
- lab result;
- prescription or medication list;
- clinician message;
- patient note;
- memory, still unverified.

Mark AI transcription as `UNVERIFIED` until a person checks it against the original. Copy numbers with their units, reference ranges, date, page, and source ID.

Keep raw records unchanged and available for checking.

Verification requires the original cited source. Open it. Check that it exists, supports the claim, and applies to the population being discussed.

## Keep the medical boundary clear

AI can organize records, extract text, compare versions, map sources, and prepare questions.

Qualified clinicians interpret the medical meaning. The patient and clinical team make treatment decisions.

The assistant must never:

- diagnose;
- choose or change treatment;
- estimate a person's chance of benefit or harm;
- decide that a symptom is safe;
- turn a preliminary paper into a recommendation;
- present a generated citation as a source.

When someone asks, "What should I do?", prepare questions for the treating clinician. State which facts and sources shaped each question.

## Urgent care

Urgent symptoms need a clinician or local emergency service now.

Close the research or filing workflow. Tell the person to contact their treating team, local urgent-care service, or local emergency number. The assistant should not continue with triage.

If the person is unsure how urgent it is, direct them to a qualified human service.

## Research watches

A research watch finds leads. It will miss papers, trials, corrections, and local options.

Each reported item must include:

- a source that was opened;
- DOI, registry ID, or official URL;
- publication date and date checked;
- peer-review status;
- population and sample size;
- main result in plain language;
- limits and conflicts of interest;
- one question for a clinician.

Label preprints and conference abstracts clearly. Check for corrections, retractions, and trial-status changes.

The clinician decides whether a finding matters for this case. The assistant may only explain why it was flagged for review.

Show the search terms before scheduling a watch. Get fresh consent when the terms or external services change.

## Before the first file

- [ ] The person chose the provider and plan.
- [ ] The data path was explained.
- [ ] Consent was recorded locally.
- [ ] Only the needed folder is shared.
- [ ] Device encryption is on.
- [ ] An encrypted backup exists.
- [ ] No git remote exists.
- [ ] The first source is ready for manual verification.

---

_Continue with the copy in [`starter/`](starter/)._
