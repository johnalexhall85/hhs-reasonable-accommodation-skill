# HHS Reasonable Accommodation Assistant

An AI skill that helps U.S. Department of Health and Human Services (HHS) employees and their representatives prepare thorough, well-organized reasonable accommodation (RA) documentation under **HHS Policy 126-1**, the **Rehabilitation Act**, and the **ADA Amendments Act**.

It uses the open [Agent Skills](https://agentskills.io) format, so it works in Claude and in other tools that support skills.

**[⬇ Download the skill (.zip)](https://github.com/johnalexhall85/hhs-reasonable-accommodation-skill/releases/latest/download/hhs-reasonable-accommodation.zip)**

---

## What it does

The assistant walks you through four phases, at your own pace:

1. **Basic intake (private):** the position, essential functions, and functional limitations.
2. **Brainstorm (private):** translates symptoms into workplace-relevant functional language and suggests possible accommodations for the employee to review and confirm.
3. **Case history (private):** prior requests, agency conduct, deadlines, and open 45-day EEO windows.
4. **Document drafting:** using only what the employee has confirmed.

It can draft:

- A compliance tracker (accommodation history, policy issues, 45-day EEO windows)
- A functional limitations and nexus document for the interactive process meeting
- A response to a Reasonable Accommodation Coordinator (RAC) information request
- A formal accommodation request letter to attach to **HHS-995**
- Provider letters structured to match **HHS-994** items (a) through (e), drafted in full so the provider only needs to review, revise, and sign
- Plain-language cover notes explaining the framing to providers
- Professional correspondence to the RAC or agency

It works for employees acting on their own behalf, for representatives, and for an employee and representative sharing one chat.

## Install

### Claude (web, desktop, mobile)

1. Make sure code execution is on: **Settings > Capabilities** (Free, Pro, Max). On Team or Enterprise plans, an admin enables it under **Organization settings > Plugins & skills**.
2. [Download the zip](https://github.com/johnalexhall85/hhs-reasonable-accommodation-skill/releases/latest/download/hhs-reasonable-accommodation.zip). Don't unzip it.
3. In Claude, go to **Customize > Skills**, click **+**, then **+ Create skill > Upload a skill**, and choose the zip.
4. Make sure the skill is toggled on.

### Claude Code

```
/plugin marketplace add johnalexhall85/hhs-reasonable-accommodation-skill
/plugin install hhs-reasonable-accommodation@hhs-ra-assistant
```

### Other tools that support Agent Skills (Codex, Gemini CLI, Copilot, Cursor, and others)

```
npx skills add johnalexhall85/hhs-reasonable-accommodation-skill
```

### ChatGPT

Skills in ChatGPT are available on Business, Enterprise, Healthcare, and Edu workspaces where an admin has turned them on. Go to **Skills > Create > Upload from your computer** and choose the zip.

### Tools without skill support

Create a custom assistant (Custom GPT, Gem, or project), paste the contents of `skills/hhs-reasonable-accommodation/SKILL.md` (without the header block between the `---` lines) as its instructions, and upload the files in `references/` as knowledge files.

## Use it

Start a new chat and say something like:

> Use the HHS reasonable accommodation skill. I need help with an accommodation request.

The assistant will ask whether you are the employee or a representative and whether anyone else will be typing in the chat, then guide you from there.

## Important

- **Not legal advice.** This tool provides legal information and drafting support. It is not a lawyer. Consult qualified EEO counsel on complaint jurisdiction, deadlines, or litigation strategy.
- **Mind your privacy.** Use placeholders for names, case numbers, and identifiers until a document is ready to submit. If you use an AI tool on a government system or account, follow your agency's acceptable-use and AI policies, and assume what you enter may be visible to the agency.
- **Check every deadline yourself.** The 45-day EEO contact window is a jurisdictional bar. The assistant flags triggering events, but you are responsible for confirming dates.
- **Templates are examples.** Dates, names, and scenarios in the bundled templates are illustrative only.
- **Review before submitting.** Every draft should be reviewed by the employee, and provider letters must reflect the provider's own clinical judgment.

## What's inside

```
skills/hhs-reasonable-accommodation/
├── SKILL.md        # Assistant instructions
├── references/     # Templates, questionnaires, HHS policy and form text
└── assets/         # Original HHS forms (PDF) and template documents
```

## License

MIT for the skill content. The official HHS forms and HHS Policy 126-1 are U.S. Government works.
