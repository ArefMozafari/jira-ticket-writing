# jira-ticket-writing

An [Agent Skills](https://agentskills.io) skill that gives every Jira ticket the same shape: a
symptom title, a short non-technical description, and three to five pass/fail acceptance criteria
that a tester can check on screen. The skill is in `skills/jira-ticket-writing/SKILL.md`.

## Install

| Agent | Command |
| --- | --- |
| Claude Code | `claude plugin marketplace add ArefMozafari/jira-ticket-writing`<br>`claude plugin install jira-ticket-writing@jira-ticket-writing` |
| Gemini CLI | `gemini extensions install https://github.com/ArefMozafari/jira-ticket-writing` |
| GitHub Copilot CLI | `copilot plugin marketplace add ArefMozafari/jira-ticket-writing`<br>`copilot plugin install jira-ticket-writing@jira-ticket-writing` |
| Cursor | `agent plugin marketplace add https://github.com/ArefMozafari/jira-ticket-writing`<br>then `/plugins` in `agent` and install `jira-ticket-writing` |
| Codex, Cursor, Windsurf, Cline and more | `npx skills add ArefMozafari/jira-ticket-writing` |
| GitHub CLI, for Copilot and other agents | `gh skill install ArefMozafari/jira-ticket-writing` |

Inside a Claude Code session the same two steps are the slash commands
`/plugin marketplace add ArefMozafari/jira-ticket-writing` and
`/plugin install jira-ticket-writing@jira-ticket-writing`. Restart the session afterwards so the
skill loads.

### Manual install

Copy the `skills/jira-ticket-writing` folder into your agent's skills directory:

| Agent | Directory |
| --- | --- |
| Claude Code | `~/.claude/skills/` |
| Codex, Gemini CLI, GitHub Copilot, Cursor, Windsurf, OpenCode, Goose, Amp | `~/.agents/skills/` |
| Cline | `~/.cline/skills/` |

## Use

The skill loads when you create, rewrite or review a Jira ticket, or write acceptance criteria.
Ask for it by name with `/jira-ticket-writing`.
