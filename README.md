# Claude Skills — Chris Tech

Custom [Claude](https://claude.com) skills used across Chris Tech / Zetu Business Solutions projects. Each skill is a `SKILL.md` file (Claude's instruction format) plus a packaged `.skill` file for one-click install.

## What's a `.skill` file?

A `.skill` file is a zip archive containing the skill's `SKILL.md`. GitHub can't preview zip contents inline, so it looks blank in the file viewer — that's expected. To read a skill's actual instructions, open the plain-text `SKILL.md` inside its matching folder (linked below). To install a skill into Claude, download the `.skill` file and load/save it in Claude.

## Skills

### [`google-ui-design`](./google-ui-design/SKILL.md) · [download](./google-ui-design.skill)

Chris Tech's default UI/UX design standard for every website, web app, SaaS platform, dashboard, marketplace, POS system, admin panel, portal, and landing page. Applies automatically to frontend work unless a different direction is requested.

Inspired by Google Material Design and modern Google products — clarity, whitespace, restrained color, strong typography, consistent components, accessibility — without copying Google's branding, logo, or exact layouts.

Covers:
- Design priority order (usability → accessibility → hierarchy → responsiveness → performance → consistency → polish → animation)
- Design tokens, color system, typography, spacing/container system
- Header, navigation, hero/landing sections, search, cards, buttons, forms & inputs
- Icons, avatars, badges, alerts, toasts, loading/empty/error/404 states
- Modals, drawers, dropdowns, tooltips, tables
- Dashboards, admin systems, auth flows, payment UI, e-commerce, POS
- Project-type adaptation (SaaS, marketplace, POS, school system, business site, docs/support)
- Security-aware UI, responsive breakpoints, dark mode, accessibility, animation
- Next.js / React / Tailwind conventions and a reusable component system
- A mandatory design-review checklist and final quality bar before any UI is considered done

### [`emoji-policy`](./emoji-policy/SKILL.md) · [download](./emoji-policy.skill)

Strict no-emoji policy (0% default density) for all UI and written content across projects. Applies to navigation, buttons, cards, headings, form labels, alerts, dashboards, empty/error/loading states, marketing copy, docs, emails, and system messages — use a proper icon library (Lucide, Material Symbols) instead of emoji icons.

Emojis are only used when the user explicitly requests them, supplies specific emojis to preserve, the product needs emoji-based chat/messaging, or an emoji already exists in user-generated content.

## Installing a skill

1. Download the relevant `.skill` file from this repo (or from a chat where Claude generated it).
2. In Claude, open the file — a **Save skill** option appears.
3. Once saved, Claude consults the skill automatically whenever its description matches the task (no need to reference it by name).

## Updating a skill

Edit the `SKILL.md` in the skill's folder, then repackage it into a `.skill` file (Claude's `skill-creator` skill handles this — ask Claude to "update and repackage the `<name>` skill"). Commit both the updated `SKILL.md` and the regenerated `.skill` file.

## Repo structure

```
claude-skill/
├── google-ui-design/
│   └── SKILL.md
├── google-ui-design.skill
├── emoji-policy/
│   └── SKILL.md
├── emoji-policy.skill
└── README.md
```

## Maintainer

[Chris Tech](https://www.christeck.co.ke) — [@learninghub44](https://github.com/learninghub44)
