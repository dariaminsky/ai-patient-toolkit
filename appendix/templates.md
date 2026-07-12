# Templates

_Copy-paste-ready material. The most-bookmarked part of the guide, probably._

## File structure template — your digital health twin

```
your-health/
├── README.md                      # high-level summary; "if I disappear, this is what to read first"
├── 00-current-state.md            # what is true right now (new version each time it changes; old ones go to 99-archive/); no names — safe to paste anywhere
├── care-team.md                   # your doctors and clinics — separate on purpose, stays local
├── 01-diagnosis/
│   ├── report-YYYYMMDD.md         # transcribed key info, link to scan
│   ├── imaging-YYYYMMDD.md
│   ├── labs-YYYYMMDD.md           # one file per lab panel
│   └── original-records/          # raw scans (PDF, screenshots) untouched
├── 02-treatment/
│   ├── timeline.md                # what was done, when, by whom, outcome
│   ├── meds.md
│   ├── doctor-notes/              # messages, emails, verbal instructions — marked as message-grade
│   └── original-records/
├── 03-genetics/
│   ├── 23andme-raw.txt
│   ├── your-variant.md            # your exact variant, as ClinVar writes it
│   └── family-history.md
├── 04-decisions/
│   ├── YYYY-MM-decision-X.md      # one file per major decision: options, evidence, reasoning, what happened
│   └── ...
├── 05-side-effects/
│   ├── one-file-per-side-effect.md
│   └── ...
├── 06-research/
│   ├── papers-read.md
│   ├── researchers-contacted.md
│   └── trials-checked.md
├── agents/                        # standing instructions for your assistant (research-watch.md, appointment-prep.md)
└── 99-archive/                    # old profile versions: 00-current-state-v1-YYYY-MM-DD.md
```

Every numbered folder can hold its own `original-records/` for untouched raw files, next to their transcriptions.

The point is not the structure. The point is: **everything in one place**, **plain text**, **version-controllable**, **readable by any LLM in one upload**.

## Prompt template — first analysis of a new clinical document

```
I am [age], [sex/gender]. I have [diagnosis]. My genetic profile includes [variants]. 

I am attaching [type of document, e.g., a diagnosis report, biopsy result, or lab panel from YYYY-MM-DD].

Please:

1. Summarize the key findings in plain language.
2. Flag any results that look unusual or unexpected given my diagnosis.
3. Identify questions I should ask my [specialist / surgeon / treating doctor] at my next consultation.
4. Note any specific terms or values I should research further.

Do not give treatment recommendations. I am the patient. I am not asking for a doctor's opinion — I am asking for help understanding my own data.

If you are not certain about anything, say so. Hallucinations are not acceptable here.
```

## Prompt template — finding the right researcher

```
I have [diagnosis] with [specific subtype / genetic context]. 

I am looking for researchers / clinicians who specialize in this specific intersection — not generalists. I am willing to travel.

Please identify the top 5-10 researchers worldwide currently publishing on [specific area], with:

- Their name and current institution
- A one-line summary of their most relevant recent work (last 3 years)
- A specific paper or trial of theirs that I should read
- How to contact them (institutional email, lab page)
- Whether they accept consultations from patients (if known)

Cross-reference with PubMed / Google Scholar if possible. Be specific about what you do not know.
```

## Email template — reaching out to a researcher

```
Dear Dr. [Lastname],

I am a patient with [diagnosis + specific context]. I have read your paper "[exact title]" (Journal, Year) and found [specific finding] particularly relevant to my situation because [one specific reason that shows you actually read it].

I have a specific question: [sharply articulated, 1-3 sentences, answerable].

I understand you are busy and may not be able to respond. If you cannot, I would be grateful for a pointer to a colleague or a forthcoming publication that might address this.

Thank you for your work.

[Your name]
[Optional: one-line credential or context, e.g., "I am happy to share my full record under any privacy arrangement you prefer."]
```

## Doctor consultation prep — bring this to every appointment

```
For appointment on YYYY-MM-DD with Dr. [Name]:

Top 3 questions:
1. 
2. 
3. 

Updates since last appointment:
- 

Data to discuss:
- [specific scan / lab / event]

Concerns:
- [physical / emotional / decision-making]

What I am hoping to leave the appointment with:
- 
```

## Skeptical filter — vetting a supplement / intervention claim

```
Someone has recommended [intervention] for [condition]. The claim is that it [specific claimed mechanism / benefit].

Please:

1. Identify the strongest primary-source evidence for this claim. Cite specific studies with year, journal, sample size, study type.
2. Identify the strongest counter-evidence or null results.
3. Note any conflicts of interest in the strongest pro-evidence studies.
4. State the realistic likelihood this intervention is beneficial / neutral / harmful for someone in my specific situation ([condition + relevant context]).
5. If the evidence is sparse, say so clearly. Do not fill the gap with confident speculation.

I am not asking whether to take it. I am asking what the evidence actually says.
```

## Cross-reference workflow

```
1. Ask the question of Model A.
2. Ask the same question of Model B (different vendor — e.g., if A was Claude, B is Gemini).
3. If answers agree → ask Model C as confirmation.
4. If answers disagree → ask each model to critique the other's response, then re-evaluate.
5. For anything that would affect treatment, ALSO ask a human specialist before acting.
```

## What is NOT in the templates

- Treatment-specific prompts. Those depend too much on the specific condition + protocol; they will be covered in future updates.
- Insurance-navigation templates. Country-specific; out of scope.
- Death / advance-directive planning. Important; separate guide.
