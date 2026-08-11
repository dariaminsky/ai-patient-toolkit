# AI Patient Toolkit

This repository contains a folder structure, templates, and AI-assistant instructions for organizing medical records.

I built this during my own treatment. I use the same folder structure for my records. Version 0.2 publishes the reusable parts.

Included: file-organization instructions, a source-checked health-profile template, decision and side-effect logs, appointment-prep instructions, and a research-lead workflow.

Use AI to organize records, map sources, and prepare questions. Diagnosis and emergency assessment require qualified clinicians. Discuss treatment choices with your medical team. For an emergency, contact the local emergency service.

Cloud assistants process relevant file content on their providers' systems, including files opened from a local folder. Medical profiles remain sensitive after names are removed. Read [Privacy and processing](#privacy-and-processing) before adding records.

## Quick start

1. On this page, press the green **Code** button, then **Download ZIP**. Unzip it and rename the folder `ai-patient-toolkit`.
2. Create a folder called `health-workspace`. Put `ai-patient-toolkit` inside it.
3. Copy the `ai-patient-toolkit/starter` folder into `health-workspace`. Rename the copy `my-health-records`.
4. Read the [privacy and safety guide](02-privacy-and-safety.md) and the [starter instructions](starter/README.md). Check device encryption, backups, provider settings, and consent.
5. Open `health-workspace` as a local folder in [Claude Code](https://claude.com/claude-code) or [Codex](https://openai.com/codex).
6. Paste this prompt:

   > Read `ai-patient-toolkit/AGENTS.md`, `ai-patient-toolkit/02-privacy-and-safety.md`, and `my-health-records/README.md`. Help me set up `my-health-records`. Explain the data flow before reading a medical file. Ask for consent for each file batch. Show me the file plan first. Keep the originals unchanged. Ask me to verify every extracted date, unit, value, and source.

7. Review the plan. Approve one step at a time. Add one approved medical file. Keep the original where it is. Check every extracted fact against it.

When a new report arrives, copy it into the folder. Ask the assistant to update the profile as a new version. Review the changes.

## Contents of v0.2

- [Assistant setup instructions](AGENTS.md)
- [Mindset](00-mindset.md)
- [Data and versioning guide](01-data.md)
- [Privacy and safety guide](02-privacy-and-safety.md)
- Starter files:
  - [Overview](starter/README.md)
  - [Current-state profile](starter/00-current-state.md)
  - [Source index](starter/source-index.md)
  - [Care team](starter/care-team.md)
  - [Decision note](starter/decision-note.md)
  - [Side-effect log](starter/side-effect-log.md)
  - [Research watch](starter/agents/research-watch.md)
  - [Appointment prep](starter/agents/appointment-prep.md)
- Synthetic example:
  - [Example overview](example/README.md)
  - [Example current-state profile](example/00-current-state.md)
- [Prompt templates](appendix/templates.md)
- [Resources](appendix/resources.md)

## Files and versions

The main file is `00-current-state.md`. It records the current diagnosis, treatment, results, sources, and open questions.

Save each meaningful update as a new version. A later review may need the state from a specific date. Git can record the changes. Keep a separate encrypted backup too.

The files use Markdown (`.md`): plain text with headings and lists. Text editors and AI tools can read it. You can compare versions and move the files between tools.

## Reusable agent files

Agent files are saved instructions for a repeated task.

The research-watch file asks the assistant to look for papers and trial updates. It can miss sources or read them badly. Open the primary source. Take treatment-relevant findings to a clinician. Check the source even when two models agree.

The appointment-prep file asks the assistant to draft a short question list from the current profile. Review every question before the visit.

Run these files manually in v0.2. Scheduling depends on the tool.

Research monitoring is optional. Skip it if it adds work you do not want.

## Privacy and processing

Choosing a local folder controls where the files are stored. A cloud assistant still sends relevant file content to its provider for processing.

Removing names lowers the risk. A medical profile can still identify someone through a rare diagnosis, genetics, or dates.

- Check the provider's retention and training policies.
- Remove names, birth dates, record numbers, and hospital names before web searches.
- Keep IDs, insurance numbers, and credentials out of the health folder.
- Keep the health folder separate from this toolkit repository. Never push it to GitHub.
- Read the full [privacy and safety guide](02-privacy-and-safety.md) before adding a large record set.

## About this project

I write about the background in [Information Body](https://informationbody.substack.com).

## Contributing

Corrections and additions are welcome. Open an issue or a pull request. Researchers can open an issue to correct a citation or its framing.

## License

Guide text and examples: [CC BY 4.0](LICENSES/CC-BY-4.0.txt). Starter files and scripts: [MIT](LICENSES/MIT.txt). See [LICENSE.md](LICENSE.md).
