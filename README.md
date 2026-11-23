# jira-ticket-writing

An agent skill that gives every Jira ticket the same shape: a symptom title, a short
non-technical description, and three to five pass/fail acceptance criteria that a tester can
check on screen. The skill is in `skills/jira-ticket-writing/SKILL.md`.

## Install (Claude Code)

```
/plugin marketplace add <owner>/jira-ticket-writing
/plugin install jira-ticket-writing@jira-ticket-writing
```

Replace `<owner>/jira-ticket-writing` with the GitHub path where this repository is hosted.

## Use

The skill loads when you create, rewrite or review a Jira ticket, or write acceptance criteria.
Ask for it by name with `/jira-ticket-writing`.
