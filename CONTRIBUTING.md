# Contributing

This repository is public.

## No personal medical data

Never put personal medical data in an issue, pull request, discussion, commit, screenshot, or attachment.

This includes your data and anyone else's:

- names, dates of birth, addresses, and contact details;
- record, insurance, account, and prescription numbers;
- reports, scans, lab results, and portal screenshots;
- exact genetic results tied to a person;
- appointment dates, clinic names, and clinician names;
- AI transcripts that contain case details;
- filenames or image metadata that identify someone.

Redaction can fail. A rare diagnosis, date, and location may be enough to identify a person.

Assume that copies, notifications, caches, and repository history will remain.

If a report needs personal data, do not file it here. Ask for a private route without adding case details. If no private route exists, keep the data off GitHub.

## Send a safe report

Use synthetic details.

Good issue:

> The lab template drops units when a value wraps onto a second line. Synthetic example: Marker Q = 14 units/L.

Unsafe issue:

> Here is my report. What does this result mean for my treatment?

For a correction:

1. Name the file and section.
2. State the problem in one sentence.
3. Link a primary or official source.
4. Add the date you checked it.
5. Suggest a short replacement.

## Medical claims

Keep contributions inside the guide's scope: organization, provenance, privacy, and appointment preparation.

Do not add diagnosis, treatment advice, personal benefit estimates, or emergency triage.

Research claims need an opened source. Prefer regulators, clinical guidelines, trial registries, peer-reviewed primary studies, and official product documentation. Label preprints and conference abstracts.

Use original sources. Open each one and confirm that it supports the claim.

## Pull requests

Keep the change small. Explain what changed and why. List every source used.

Run a privacy check before submitting:

- [ ] All examples are synthetic.
- [ ] No screenshots contain personal data.
- [ ] No file metadata contains personal data.
- [ ] Links open and support the text.
- [ ] Product and pricing facts include a checked date.
- [ ] The change gives no treatment advice.

## License

Contributions use the license assigned to their destination in [`LICENSE.md`](LICENSE.md). By submitting a contribution, you agree to license it on those terms.
