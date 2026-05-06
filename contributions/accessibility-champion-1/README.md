# ♿ Accessibility Champion

You make sure the site can be used by the widest possible audience. Alt
text, plain language, contrast, focus states. **What you change actually
ships.**

Multiple champions in the team — pair-review when you can. Two reviewers
catch more than one.

## What lives in this folder — pick whichever calls to you

- `audit.md` — your running list of issues found and fixes proposed
- `alt-text.md` — alt text for the team's images
- `plain-language-rewrites.md` — passages you've simplified
- `keyboard-nav-walkthrough.md` — what tabbing through the site reveals
- `screen-reader-walkthrough.md` — what NVDA/VoiceOver would announce
- `final-review.md` — your sign-off near the end of the hour

**Claim a lane with your teammates first** — audit, alt text + plain
language, keyboard/screen-reader walkthrough, final review.

## Coordinate with

- **Other Accessibility Champion(s)** — pair on the trickier issues
- **Copywriters** — for jargon, reading level
- **Visual Designers** — for alt text, contrast
- **Software Developers** — for colour contrast, focus states, semantic HTML

## First 2 minutes

1. Sign in to **copilot.microsoft.com** with your role-card account.
2. Ask:
   > *"Teach me, in 5 bullet points, what 'accessibility' means for a small marketing microsite. What are the most common issues a quick team is likely to miss?"*
3. Use it as your checklist. Drop it in `audit.md` and start ticking.
4. Commit.

## Prompts that work

- *"Generate alt text for an image of [describe it]. 1–2 sentences. Don't start with 'image of'."*
- *"What's the reading age of this paragraph? Suggest a plain-language version."*
- *"Check this colour combination for WCAG AA contrast: foreground `#1a1a2e`, background `#fdfcfb`."*
- *"Find me three pieces of jargon a 16-year-old wouldn't understand in this passage, and rewrite each."*

Pair, don't gate. When you find an issue, propose the fix.
