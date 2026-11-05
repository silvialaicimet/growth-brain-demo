# growth-brain-demo

A demo of a function brain as a plugin: the shared agents, skills and context of a Growth team, for a fictional challenger energy retailer. It shows the structure. Every file in `context/` is a placeholder and contains no real data.

New here? Say: **help me get started**, or **I'm new, set me up**, and the onboarding coach takes over.

## Install

**Claude Code**

```
/plugin marketplace add silvialaicimet/growth-brain-demo
/plugin install growth-brain-demo@growth-brain-demo
```

**Claude desktop app (Code tab)**

Open the Code tab, open the plugins screen, choose "Add marketplace", enter `silvialaicimet/growth-brain-demo`, then install `growth-brain-demo`. Plugins do not load in claude.ai in the browser.

Then run `/growth-brain-demo:setup` once. It reads `.claude/folders.json` if you have one, creates only the missing folders and never overwrites a file.

## What is inside

| Part | Contents |
|---|---|
| Agents | `campaign-analyzer`, `channel-optimizer`, `content-generator`: the default flow, in that order |
| Skills | `growth-onboarding` (the coach), `growth-budget`, `legal-check`, `aeo-content` |
| Command | `/growth-brain-demo:setup` |
| Context | Placeholders: project brief, brand brain, budget structure, way of working |

Agents write their outputs to your own `workflows/` and `drafts/` folders, never into the plugin.

## Owners

| What | Owner |
|---|---|
| Brand brain | TODO |
| Legal check rules | TODO |
| Everything else | Plugin owner (TODO) |

## Hooks

None. Nothing in this plugin runs automatically.

## Suggest a change

Write one line: what happened, what should happen, one example. Open an issue or pull request on this repo.

## Never in this plugin

Customer data, email addresses, passwords and keys, salaries and people costs, hiring material, drafts that are not approved.
