# 💻 Software Developer

You don't write code directly into the site. You write **proposals** here —
the Factory Agent reads them and reshapes the SHELL (HTML structure, CSS
palette, layout, snippets). You're directing AI, not fighting it.

Multiple developers in the team — you all contribute to the SHELL together.
Pick the angle that calls to you and commit.

## What lives in this folder — pick whichever calls to you

- `palette.md` — colour + typography proposals (hex codes, type pairing).
  The agent maps these to CSS variables in `styles.css`.
- `layout-ideas.md` — hero proportions, grid, page composition
- `page-structure.md` — section order, what each section should do
- `section-ideas.md` — a brand-new section the page is missing
- `component-snippets/` — small HTML/CSS/JS bits the agent can lift in
- `refactor-requests.md` — *"the hero feels cramped, suggest the agent
  widens it"*
- `polish-pass.md` — small CSS improvements you'd ship if you had more time
- `wildcards.md` — bold ideas (animated stat counter, scroll fade-in,
  micro-interaction). Demoable in 60 seconds wins.

**Claim a lane with your teammates first** so you don't all converge on the
same thing — palette, layout, components, polish, wildcards. The team
covers more ground that way.

## What this turns into on the live site

| You commit … | The agent does … |
| --- | --- |
| `palette.md` with hex codes | updates CSS variables at the top of `site/styles.css` |
| `layout-ideas.md` describing hero proportions | rewrites `<section>` markup to match (mobile-first) |
| `section-ideas.md` proposing a new section | adds a new `<section>` in the GROW ROOM at the bottom of `<main>` |
| A snippet in `component-snippets/` | lifts the snippet into the page where it fits |
| `refactor-requests.md` | applies the requested change to the markup or CSS |

The Project Coordinator owns FLOW (section order); your proposals shape
the SHELL. If you and the PC disagree on flow, the agent follows the PC's
plan and adapts the shell to fit.

## Coordinate with

- **Other Software Developers** — agree lanes early so you're not duplicating
- **Visual Designers** — palette and imagery shape the shell
- **Project Coordinator** — flow + section order
- **Accessibility Champion(s)** — focus states, contrast, motion preferences

## First 2 minutes

1. Sign in to GitHub with your role-card account. Open the repo. Find your
   folder.
2. Open **github.com/copilot** in another tab.
3. Pick a lane (palette / layout / components / polish / wildcards).
4. Run a prompt. Drop the result as a new file in your folder. Commit.

## Prompts that work

- *"Suggest a 4-colour palette for a charity microsite for first-gen UK uni students. Warm, trustworthy, hopeful. Hex codes plus reasoning."*
- *"Critique this hero layout for mobile: [paste]."*
- *"Suggest a typography pairing for a warm, editorial-feeling charity site. Display font + body font."*
- *"Write a CSS-only fade-up animation for a hero block on page load, respecting prefers-reduced-motion."*

You're the AI's editor, not its typist. Iterate until the proposal is
sharp, then commit.
