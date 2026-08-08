---
name: emoji-policy
description: Strict no-emoji policy for all UI and written content across projects. Consult this whenever building or editing any interface (React/Next.js/HTML components, buttons, nav, cards, dashboards, forms, alerts, empty/loading/error states) or writing any copy (marketing text, docs, help articles, product descriptions, emails, system/notification messages). Default emoji density is 0% — use proper icon libraries (Lucide, Material Symbols) instead of emoji icons, and keep written content professional and emoji-free unless the user explicitly requests emojis or supplies specific ones. Always consult even if the user doesn't mention emojis, since the default is to never add them.
---

# Emoji Policy — Strict

Default emoji density: **0%**. Do not use emojis in UI or content unless the user explicitly requests them or supplies a specific emoji to preserve. The default interface and copy must be professional, clean, and minimal, and must remain fully usable and visually complete without any emojis.

## Never use emojis for

- Navigation icons, items
- Button icons
- Card icons
- Feature icons
- Section decorations
- Headings, page titles
- Form labels
- Alerts, notifications
- Dashboard statistics
- Product categories
- Marketing decorations
- Empty states
- Error messages
- Success messages
- Placeholder content
- Loading states

Use a proper UI icon library instead: Lucide, Material Symbols, or another consistent professional icon library already used by the project.

## Never auto-add emojis to content

- Website copy
- Marketing text
- Blog content
- Documentation
- Help-center articles
- Product descriptions
- Dashboard text
- Notifications
- Emails
- System messages

Keep written content professional and natural — no decorative emoji sprinkled in for tone.

## Icons vs. emojis

Never substitute an emoji for a professional UI icon.

Bad: `🚀 Launch`, `💰 Payments`, `📊 Analytics`, `⚙️ Settings`

Correct: use the icon library's Launch/Payments/Analytics/Settings icon components alongside the text label — no emoji glyph.

## Exceptions — emojis allowed only when

1. The user explicitly asks for emojis.
2. The user provides specific emojis and asks that they be preserved.
3. The project specifically requires emoji-based communication, e.g. a chat/messaging feature where users send emojis to each other.
4. An emoji is part of user-generated content and must be displayed as supplied (never strip user content).

Even inside these exceptions, do not add further emojis beyond what was requested or supplied.

## When uncertain

Do not use the emoji. Communicate hierarchy and emphasis with typography, spacing, color, borders, icons, and layout instead.
