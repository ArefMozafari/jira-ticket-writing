---
name: jira-ticket-writing
description: Writes or rewrites a Jira ticket (title, description, acceptance criteria) in one shared short, non-technical Persian shape that QA, PMs and developers can all read. Use when creating a Jira ticket or bug, rewriting a vague one, writing or checking acceptance criteria (معیار پذیرش), or syncing a ticket with what was actually done.
---

# Jira Ticket Writing

One shared shape for every ticket, so a reader can decide in seconds what is wrong, how to see it,
and when it counts as done. The reader is a tester, a reporter or a lead, and many are not
technical. Write for them, not for the code.

Ticket text is Persian unless the team's tickets are already in another language; match them.

## Title

- One sentence stating the symptom or the outcome, in the words a user would use.
- When rewriting an existing ticket, keep the original title's key nouns and add the specifics
  around them. People search for a ticket by the words they first saw. When in doubt, keep the
  title and sharpen only the description.
- No file names, class names, or internal terms.

## Description

Four parts, in this order. Each carries only what the "is this ready?" decision needs.

1. **مشکل** (the problem): two or three lines. What the user sees going wrong. For a feature or a
   task, say what is missing and why it matters instead.
2. **مراحل بازتولید** (steps to reproduce): a numbered `1.` list, the fewest steps that reach the
   problem. Skip this part for a feature with nothing to reproduce.
3. **معیار پذیرش** (acceptance criteria): see below.
4. **نکته** (note): only when the steps have a trap, such as a needed account state or a device. Include
   it only when the reporter's text or the ticket's facts state the trap; never invent one. Skip it
   otherwise.

The merge or pull request link goes last, once the work has one, as a markdown link:
`مرج ریکوئست: [title](url)`.

## Acceptance criteria

The checklist a tester runs to decide "done". Each line is one thing they can look at and pass or
fail.

- Three to five bullets. More than five means the ticket is two tickets.
- One observable behavior per bullet, stated as trigger then result:
  «وقتی … ، … نمایش داده می‌شود».
- Say what appears on screen, not how it is built. No class, file, endpoint or cause.
- Cover the main path, one edge case, and one "must not break" case (the nearby behavior that
  worked before and still has to).
- No vague verbs («درست کار کند», «بهتر شود»). If a tester cannot tell pass from fail, rewrite it.
- No cause analysis or solution design. That belongs in the merge request description.

## Example

Title: `دکمه ورود بعد از وارد کردن کد تأیید فعال نمی‌شود`

```
مشکل
بعد از وارد کردن کد تأیید ۶ رقمی، دکمه «ورود» غیرفعال می‌ماند و کاربر نمی‌تواند وارد شود.

مراحل بازتولید
1. صفحه ورود را باز کنید و شماره موبایل را وارد کنید.
2. کد تأیید ۶ رقمی را وارد کنید.
3. وضعیت دکمه «ورود» را ببینید.

معیار پذیرش
- وقتی هر ۶ رقم کد وارد شد، دکمه «ورود» فعال می‌شود.
- وقتی یکی از رقم‌ها پاک شد، دکمه دوباره غیرفعال می‌شود.
- ورود با کد درست مثل قبل انجام می‌شود و کاربر به صفحه اصلی می‌رسد.

مرج ریکوئست: [رفع غیرفعال ماندن دکمه ورود](https://example.com/merge_requests/1)
```

## When closing a unit of work

Compare the ticket with what was actually done. If the title or description is vague or no longer
matches, update the description first, and the title only within the keep-the-key-nouns rule above.
This sync is optional; skip it when the ticket already reads right.

## Jira markdown traps

- Write links as `[text](url)`. The wiki form `[text|url]` is stored as literal text.
- Write numbered lists as `1.` lines. Lines starting with `#` come back as separate one-item lists.

## Checklist before saving

- [ ] Title states the symptom in user words, key nouns kept.
- [ ] Description is under about ten lines, with no code names.
- [ ] Every acceptance criterion can be passed or failed by looking at the screen.
- [ ] Three to five criteria, including an edge case and a must-not-break case.
- [ ] Links are `[text](url)` and steps are `1.` lines.
