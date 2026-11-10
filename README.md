# Grandma-proof · Dona Maria

**An agent skill that makes your AI build screens a 70-year-old grandmother can use, and stop pestering you while it works.**

🇧🇷 [Leia em português](README.pt-BR.md)

![license MIT](https://img.shields.io/badge/license-MIT-green) ![languages](https://img.shields.io/badge/languages-English%20%7C%20Portugu%C3%AAs-blue) ![works with](https://img.shields.io/badge/works%20with-Claude%20Code%20%7C%20Codex%20%7C%20Cursor%20%7C%20Gemini%20CLI-black)

AI agents build interfaces for people like themselves: fluent, patient and technical. Real users are not. This skill gives the agent one person to keep in mind, Grandma Rose (Dona Maria in the Portuguese version), plus seven rules it must follow.

## The seven rules

**What the agent builds**

| # | Rule | In one line |
|---|---|---|
| 1 | Simplicity | One screen, one job. Fewer buttons, less text, but never so little that people get lost. |
| 2 | Grandma | Everyday words, big targets, always a way back, errors that do not scare. |
| 3 | Alignment | Buttons and boxes in a group share size, line and proportion. No caption glued to a button; explanations live in the hover hint. |
| 4 | No AI look | No purple gradients, no invented proof, and no "GPT landing page" with a giant centered headline and one italic word. |

**How the agent works**

| # | Rule | In one line |
|---|---|---|
| 5 | Speak plainly | Replies without jargon. Using a technical word does not make the user a programmer. |
| 6 | Subagents | Split the work and run parts in parallel, with a reviewer that did not write the code. |
| 7 | Decide by debate | Small doubt? Two debater agents argue, a judge agent picks, the work goes on. The human is asked only when it matters. |

Every delivery ends with the **Grandma test**: ten checks run on the real screen, from "can you tell what this is for in 5 seconds?" to "does it work on a 360 px phone?".

## Install

Pick your language. The two skills are the same rules, written natively in each language.

| Skill | Language | Folder |
|---|---|---|
| `grandma-proof` | English | [`skills/grandma-proof`](skills/grandma-proof) |
| `dona-maria` | Português (Brasil) | [`skills/dona-maria`](skills/dona-maria) |

### Claude Code

macOS, Linux or Git Bash:

```bash
git clone https://github.com/ricarossetto/dona-maria-skill
mkdir -p ~/.claude/skills && cp -r dona-maria-skill/skills/grandma-proof ~/.claude/skills/
```

Windows PowerShell:

```powershell
git clone https://github.com/ricarossetto/dona-maria-skill
Copy-Item -Recurse dona-maria-skill\skills\grandma-proof "$HOME\.claude\skills\"
```

For a single project, copy it into `.claude/skills/` inside that project instead.

### Codex, Cursor, Gemini CLI and other agents

Copy the same folder into the skills folder your agent reads, usually `~/.agents/skills/` or `.agents/skills/` inside the project.

No skills support? Paste the content of `SKILL.md` into your `AGENTS.md` or rules file.

### Without git

Download the zip for your language from the [latest release](https://github.com/ricarossetto/dona-maria-skill/releases/latest) and unzip it into your skills folder.

## Use

Ask for any screen and the agent picks the skill up by itself. You can also call it by name:

```
/grandma-proof build the sign-up form
/grandma-proof review this dashboard
```

To keep it on for every task, add one line to your `CLAUDE.md` or `AGENTS.md`:

```
Always follow the grandma-proof skill when building interfaces and when replying to me.
```

## What is inside

```
skills/grandma-proof/
├── SKILL.md                 the seven rules and the Grandma test
└── references/
    ├── ai-tells.md          the list of AI-look signs to remove
    └── debate.md            ready-made briefs for the two debaters and the judge
```

The main file stays short so it loads cheaply. The two reference files are read only when needed.

## Honest limits

- **Subagents cost more.** Rule 6 makes the agent run several helpers at once. That is faster and usually better, and it uses more of your plan. One-step tasks are done directly.
- **The agent still asks sometimes.** Rule 7 keeps a short list of cases where it must ask: actions that cannot be undone, spending money, and things only you know.
- **Hover hints do not exist on phones.** That is why the rule is that a button's own label must be enough; the hint is a bonus.
- **It will not redesign your brand.** Existing visual identity is kept. The skill removes autopilot choices, not bold ones.

## Credits

Written with the skill format from Anthropic's [skills](https://github.com/anthropics/skills) repository. The anti-AI-look rule owes a lot to the work of the design community, especially [unslop](https://github.com/heydamir/unslop) by Damir Sokolovsky. All text here is original.

## License

[MIT](LICENSE). Use it, change it, share it.
