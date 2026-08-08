---
name: google-ui-design
description: Build modern, clean, highly usable web interfaces inspired by Google's Material Design philosophy — clarity, whitespace, strong typography, restrained color, accessibility. Use whenever building or restyling a web UI, dashboard, landing page, admin panel, form, or any React/Next.js/HTML frontend, especially when the user asks for a "clean", "modern", "professional", "Google-like", or "premium" look, or doesn't specify a design direction at all. Also consult when reviewing or polishing an existing UI for visual quality. Not for cloning actual Google products — the goal is an original interface that follows the same design principles.
---

# Google-Inspired UI/UX Design

Build interfaces that feel clean, professional, calm, spacious, trustworthy, fast, accessible, and consistent. This is not about cloning Google's products — it's about applying the same design discipline (clarity, simplicity, whitespace, strong typography, restrained color, subtle interaction) to an original interface with its own branding.

Avoid unnecessary decoration: no excessive gradients, glassmorphism, giant shadows, decorative blobs, or visually noisy backgrounds unless specifically requested. Usability beats visual effects every time.

## Workflow

1. Build the page/component.
2. Before calling it done, run through the **Final Review Checklist** at the bottom of this file.
3. Iterate — don't stop after the first functional pass.

## Layout

- Desktop max content width: ~1200–1400px, centered, generous spacing.
- Mobile: design intentionally, don't just shrink desktop. Comfortable padding, stacked cards, tappable buttons, no unintended horizontal scroll.
- Spacing scale (use consistently): 4, 8, 12, 16, 24, 32, 48, 64, 80px.
- Test at: 360/375/390/412px (mobile), 768px (tablet), 1024/1280/1440px (desktop).

## Typography

- Clean sans-serif: Google Sans (if licensed), Inter, Geist, or system-ui. No decorative fonts.
- Hierarchy: large/strong page title → medium-large section heading → ~16px body → smaller muted (but readable) supporting text.
- Keep the number of distinct font sizes small; hierarchy should come from scale + weight, not decoration.

## Color

Restrained palette. Reference values (adapt to existing brand colors if the project has them):

```
Primary:       #1A73E8
Primary Hover: #1765CC
Text:          #202124
Secondary:     #5F6368
Border:        #DADCE0
Surface:       #F8F9FA
Background:    #FFFFFF
```

Use color mainly for actions, links, status, and navigation state — not decoration.

## Components

**Header** — logo, nav, help/sign-in; light background, minimal border, clear active state, simple icons. Avoid mega menus and heavy shadows. Mobile: logo + menu drawer.

**Search** (prominent for docs/products/records apps) — generous padding, rounded corners, search icon, clear placeholder, strong focus state, keyboard accessible. Subtle border, not a heavy shadow.

```
┌─────────────────────────────────────────────┐
│  [search icon]  Search for help or type a…  │
└─────────────────────────────────────────────┘
```

**Cards** — white surface, thin border, moderate radius, minimal/no shadow, comfortable padding, clear title + description, optional icon/link. Use borders and whitespace for hierarchy, not heavy elevation.

**Buttons** — primary (brand bg, white text), secondary (light bg, border, dark text), text button (no container, brand-colored text). Always implement hover, focus, disabled, and loading states. Don't oversize.

**Forms** — explicit label + input + helper text + inline error for every field. Never rely on placeholder-as-label. Visible focus states, helpful validation, loading/success states, full keyboard nav.

```
Email address
┌──────────────────────────────┐
│ name@example.com             │
└──────────────────────────────┘
We'll use this email to contact you.
```

**Icons** — one consistent library (Lucide or Material Symbols), simple/outlined, sized and used semantically — not decoratively on every line.

**Navigation** — must always answer "where am I" and "where can I go next": active states, breadcrumbs where useful, clear titles, logical/consistent grouping.

**Tables** — light borders, comfortable row height, clear headers, hover state, pagination/search-filter when needed. On mobile, convert to cards rather than shrinking columns.

**Modals/Dialogs** — use sparingly, only for things that don't deserve their own page. Clear title, close button, Escape support, focus management, mobile-friendly sizing.

**Alerts/Notifications** — restrained, four types (info/success/warning/error), toast for short-lived feedback, no giant banners unless truly warranted.

**Loading states** — never leave the user guessing. Prefer skeleton loaders for content-heavy pages; spinners/disabled-button/progress indicators elsewhere.

**Empty states** — always explain what's missing and offer the next action. Never just "No data".

```
No projects yet
Create your first project to get started.
[Create project]
```

**Error states** — always cover: what happened, why it might have happened, what to do next (e.g. a retry action). Avoid raw technical errors unless the audience is technical.

```
We couldn't load your projects.
Check your internet connection and try again.
[Try again]
```

## Animation

Short, subtle transitions only (hover, focus, open/close, nav, loading). No large entrance animations, floating elements, parallax, or long/distracting motion. Respect `prefers-reduced-motion`.

## Accessibility (mandatory, never trade off for looks)

Semantic HTML, correct heading hierarchy, ARIA only when needed, full keyboard navigation, visible focus states, accessible labels, sufficient color contrast, screen-reader-friendly controls, reduced-motion support.

## Component architecture

Build reusable components, avoid duplicated UI logic. Typical grouping:

```
components/
├── ui/          Button, Input, Card, Dialog, Badge, Avatar, Tooltip, Dropdown, Skeleton
├── navigation/  Header, Sidebar, MobileNav, Breadcrumbs
└── sections/    SearchSection, CategoryGrid, EmptyState
```

## Technical implementation

**Next.js**: App Router when appropriate, TypeScript, Tailwind CSS when available, intentional server/client boundaries, optimized images, minimal unnecessary client JS, semantic HTML, accessibility built into components (not bolted on).

**React**: reusable components, localized state, avoid unnecessary re-renders, proper loading/error states.

## Before adding any component, ask

1. What problem does this solve?
2. Is it necessary?
3. Is the action obvious?
4. Is the hierarchy clear?
5. Would a first-time user understand it?
6. Does it work on mobile?
7. Is it accessible?

If a decorative element doesn't improve usability, cut it.

## Final Review Checklist

Before considering any page/component complete, inspect and refine: spacing, typography, alignment, responsive behavior, button consistency, card consistency, empty states, loading states, error states, accessibility, navigation, mobile experience.

The bar: it should feel like a polished, modern Google/Microsoft-level product — not a generic AI-generated template, Dribbble concept, over-designed landing page, or gradient-heavy layout.

**Clarity + Consistency + Whitespace + Typography + Accessibility + Usability = Premium UI.**
