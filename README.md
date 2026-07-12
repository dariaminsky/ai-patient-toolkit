# AI Patient Toolkit

_A simple way to organize your medical records so AI can truly help you — and your doctors._

**What this is.** When you're facing a serious diagnosis, you drown in paper: reports, scans, lab results, half-remembered conversations. And every AI chat starts from zero, so it gives you generic answers. This toolkit fixes both. You gather everything into one folder on your computer, and an AI assistant turns it into a clear, always-current picture of your case — one that you own, that any AI can read, and that no company controls. And if your medical life spans several countries, languages, and healthcare systems that don't talk to each other, this is where the method pays off most: your folder becomes the one place where your whole story exists in one piece — and it travels with you.

You don't need to be technical. If you can use a chatbot, you can do all of this.

## How it works

1. **Create a folder** on your computer. Put every medical file you have into it — PDFs, photos of documents, scans, lab results. Chaos is fine; sorting comes later, and not by you.
2. **Open a coding assistant** — [Claude Code](https://claude.com/claude-code) or [Codex](https://openai.com/codex). Don't let the word "coding" put you off: you talk to it in plain language, in *your* language, like the chatbot you already know — it can just also see and organize the files on your own computer. Download the **desktop app** — a normal application you install like any other; ignore anything on those pages that mentions "terminal" or "npm". Two honest notes before you start: both need a paid plan (about $20/€20 a month — the free tiers don't include this), and the setup takes about 15 minutes once.
3. **Give it the link to this repository** — the address of this page, copied from the top of your browser. If the app asks, choose **local** and select the folder you made in step 1. Then say: *"Please read AGENTS.md from this repository and set up my health folder."* It will sort your files, build your first **health profile** — one clear text file that holds your whole situation — and set everything up for you. (If the assistant says it can't open the link: on this page, press the green **Code** button → **Download ZIP**, unzip it next to your health folder, and say *"read AGENTS.md in the ai-patient-toolkit folder"*.)
4. **When something new happens** — a new lab result, a new symptom, a new report — open the tool, tell it what's new (or drop the file into the folder), and ask it to **create a new version of your health profile**.

That's the whole routine. Stuck at any step? Open the ordinary free chatbot you already know (claude.ai or chatgpt.com), describe what's on your screen, and ask it to walk you through — it's very good at this. The chapters below explain each part gently, and the [templates](appendix/templates.md) are ready to copy.

## Why versions?

Your medical situation is a story, not a snapshot. Treatments change, results come and go, and one day you or a new doctor will need to know *what was true in March, before things changed*. So the profile is never overwritten — each update is saved as a new version, and every old one stays. Nothing is ever lost, you can always look back, and because every old version is kept, your history can't be rewritten — only added to.

## Why plain text (.md)?

The files are plain text in Markdown (`.md`) — ordinary text with simple headings and lists:

- any AI can read it instantly, with your whole case in view;
- it opens on any computer, today and in thirty years;
- no app or company can lock it in — it's just text, and it's yours;
- it travels: one small file carries your full picture to any new doctor, any new tool.

This is close in spirit to what Andrej Karpathy calls an "LLM wiki" — personal knowledge kept in plain text that any model can read — and to the [Open Knowledge Format](https://github.com/GoogleCloudPlatform/knowledge-catalog), Google Cloud's open format for keeping knowledge in plain files, managed the careful way software is managed. Your records stay compatible with tools that don't exist yet.

## The little helpers (agents)

The same assistant can set up **agents** for you — standing instructions it runs whenever you ask and, where the tool supports it, on a schedule. The most useful one watches new research papers and clinical trials for *your specific conditions* and tells you only about things that could actually matter for you — with sources you can click and check. Another can prepare a clear, ranked list of questions before each doctor's appointment. You write them once and reuse them for as long as you need.

## Your privacy

- Everything lives in a folder **on your computer** — not in an app, not in someone's cloud.
- Be clear-eyed about one thing: when your assistant reads your files, their content goes to the AI provider you chose — that's how these tools work. So choose the provider deliberately, and check how it handles your data: policies differ by provider and plan, and they change. If there's a "use my data for training" setting, turn it off; a paid plan is usually the safer place for medical data than a free one. The guide shows where to look.
- Anything that goes *further* than your own assistant — web searches, other services — gets identifiers stripped first: no names, no birth dates, no record numbers, no hospital names. The model reasons just as well without them.
- Nothing about you goes into this repository, and nothing personal is in it.

## What's inside

| Section | What's in it | Status |
|---|---|---|
| [AGENTS.md](AGENTS.md) | Instructions your AI assistant follows to set everything up for you. | **Available** |
| [00-mindset.md](00-mindset.md) | Why this exists, and the mindset of an active patient. | **Available** |
| [01-data.md](01-data.md) | The heart of the method: the folder, the health profile, versions, privacy. | **Available** |
| [appendix/templates.md](appendix/templates.md) | Ready to copy: folder structure, prompt templates. | **Available** |
| [appendix/resources.md](appendix/resources.md) | Tools, learning material, registries. | **Available** |
| More chapters | In drafts now. | Coming |

This is a **living guide** — it grows as the tools change and as readers ask questions. I publish my thoughts in the companion newsletter, [Information Body](https://informationbody.substack.com) — subscribe if you'd like to be updated.

## A few honest words

I made this for myself, while going through treatment — the story is in [Information Body](https://informationbody.substack.com). I'm not a doctor, and this guide will never tell you what to do about your illness. It exists so that you walk into every appointment with the full picture in hand, and so your doctors get a better-informed patient. Your decisions belong to you and your medical team.

## Contributing

Corrections and additions are welcome — open an issue or a pull request. If you're a researcher whose work is referenced and you'd like the framing adjusted, open an issue.

## License

Text: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Templates and scripts: [MIT](https://opensource.org/licenses/MIT). See [LICENSE.md](LICENSE.md).
