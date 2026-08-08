---
name: google-ui-design
description: Chris Tech's default UI/UX design standard for every website, web app, SaaS platform, dashboard, marketplace, POS system, admin panel, portal, and landing page — apply automatically to all frontend work unless the user explicitly requests a different design direction. Inspired by Google Material Design and modern Google products (clarity, whitespace, restrained color, strong typography, consistent components, accessibility) without copying Google's branding or exact layouts. Use whenever building, restyling, or reviewing any React/Next.js/HTML UI, including auth flows, payment pages, e-commerce, POS, admin systems, dashboards, and marketing/landing pages. Covers design tokens, color/typography/spacing systems, every core component, responsive/dark-mode rules, accessibility, UX writing, and a mandatory design-review pass before calling any UI done.
---

# Chris Tech — Premium Google-Inspired UI/UX Standard

The default design language for every project: **Clean + Google-inspired + Material principles + premium SaaS quality + original branding + accessibility + responsive design + excellent UX.** Apply it automatically unless the user asks for something different.

Never sacrifice usability for decoration. Never sacrifice performance for animation. Never sacrifice accessibility for aesthetics. Never copy Google's logo, branding, proprietary illustrations, or exact layout — reproduce the *philosophy* (simplicity + clarity + whitespace + excellent typography + accessibility + consistent components + subtle interaction), not the brand.

The target: **simple enough to understand immediately, polished enough to feel premium, and consistent enough to feel like one complete product.**

## Design priority order

When trade-offs come up, resolve them in this order: **1) Usability → 2) Accessibility → 3) Information hierarchy → 4) Responsiveness → 5) Performance → 6) Consistency → 7) Visual polish → 8) Animation.** A beautiful interface that's hard to use is a failed design.

## Workflow

1. Identify or preserve the project's branding (see Branding below) before styling anything.
2. Build the page/component using the design tokens and component rules in this file.
3. Run the **Design Review** checklist near the end before calling it done — the first draft is never the final one.

## Visual language

Use: white/light surfaces, soft neutral backgrounds, dark readable text, subtle borders, moderate corner radius, generous whitespace, clean typography, simple icons, restrained shadows, clear buttons, consistent spacing, subtle animation.

Avoid: excessive gradients, neon colors, huge shadows, glassmorphism, floating decorative blobs, excessive animation, unnecessary 3D, random/mismatched icons, crowded layouts, too many colors, oversized text everywhere, and generic "AI-generated landing page" patterns (see "No generic AI UI" below). It should look intentionally designed, not templated.

## Branding

Before designing, establish: brand name, logo, primary/secondary color, target audience, product purpose, tone, industry. If branding already exists, **preserve it** — don't default everything to blue just because Google is the inspiration; the project's own brand color should stay dominant. If no branding exists yet, create a restrained, professional palette for the project.

## Design tokens

Build a central token system instead of hardcoding values ad hoc: colors, typography, spacing, radius, shadows, breakpoints, component sizes, animation timing, z-index layers. Example color token set: `background, foreground, surface, surface-muted, primary, primary-hover, secondary, border, muted, success, warning, error, info`. Use these tokens consistently across the whole app.

## Color system

Restrained palette; adapt around the project's brand color when one exists.

```
Background:       #FFFFFF
Surface:           #F8F9FA
Surface muted:      #F1F3F4
Text:              #202124
Secondary text:     #5F6368
Border:            #DADCE0
Primary:           #1A73E8
Primary hover:      #1765CC
```

Color must communicate something (primary action, link, status, error, warning, success, important info) — never use it merely for decoration. Never communicate meaning through color alone — pair it with an icon, text, or label (e.g. not just "red = error").

## Typography

Clean sans-serif: Inter, Geist, system-ui, or Google Sans only where legitimately licensed. No decorative fonts unless the brand specifically calls for them.

Hierarchy: Display (major landing headings) → H1 (page titles) → H2 (major sections) → H3 (subsections/cards) → Body (primary content) → Caption (supporting info). Comfortable line height; avoid extremely thin fonts and avoid piling on font weights. Build hierarchy through size + weight + spacing + position + contrast — not by making every heading enormous.

## Spacing & containers

Spacing scale: `4, 8, 12, 16, 24, 32, 48, 64, 80, 96, 128`. Don't use arbitrary values (13px, 17px, 23px...) without a specific reason — consistency beats arbitrary precision.

Centered containers: small content 640–768px, medium 960px, large 1200–1280px, wide dashboard 1400px+. Long-form content needs a comfortable reading width — never stretch text across the full screen.

Border radius tokens: small 8px, medium 12px, large 16px, XL 20px, pill 999px. Don't invent a new radius per component.

Shadows: no shadow for normal cards, very subtle for floating elements, moderate for dialogs, stronger only where real elevation is needed. The UI should still look good with shadows removed.

## Header & navigation

**Desktop header**: logo, nav items, help/CTA, sign-in — comfortable height, minimal border, clear active state, simple CTA, optional sticky positioning. Avoid massive multi-row headers, heavy shadows, too many nav items.

**Mobile header**: logo + menu, intentionally designed (not just compressed desktop nav) — easy to open, large tap targets, clear navigation, easy to close, keyboard accessible.

**Navigation principle**: the user must always know (1) where they are, (2) what they can do, (3) what happened, (4) what to do next. Never leave them guessing.

## Hero & landing pages

Hero: small label → clear headline → short explanation → primary + secondary action → optional product visual. Avoid competing CTAs, huge paragraphs, excessive gradients, random floating objects, too many badges.

Landing page sections (include only what helps the user, not all of them by default): header, hero, value proposition, features, how it works, benefits, product preview, trust/social proof, FAQ, CTA, footer.

Footer: organize by brand / product / company / resources / support / legal, plus copyright/privacy/terms. Avoid giant footers full of unnecessary links.

## Search

Treat search as a first-class feature when the product needs it: rounded input, search icon, clear placeholder, strong focus state, keyboard support, suggestions where useful, and loading/empty/error states of its own.

```
┌──────────────────────────────────────────┐
│  Search anything...                 [🔍] │
└──────────────────────────────────────────┘
```

## Cards

White surface, thin border, moderate radius, minimal shadow, consistent padding. Not every card needs a shadow — use borders and whitespace as the primary separator.

```
┌────────────────────────────────────┐
│ [icon]                              │
│ Website Development                 │
│ Build a modern digital presence.    │
│ Learn more →                        │
└────────────────────────────────────┘
```

## Buttons

Types: **Primary** (brand background), **Secondary** (neutral surface + border), **Tertiary** (text-only), **Destructive** (dangerous actions only). Every button supports default/hover/focus/active/disabled/loading states. Don't oversize buttons.

Copy: action-oriented — "Create account", "Get started", "Save changes", "Continue", "View details", "Try again" — rather than generic "Click here" / "Submit" / "Go" when something more meaningful fits.

## Forms & inputs

Structure per field: Label → Input → Helper text → Validation/error. Never rely on placeholder text as the only label.

```
Email address
┌──────────────────────────────┐
│ name@example.com              │
└──────────────────────────────┘
We'll use this email to contact you.
```

Support keyboard navigation, visible focus, required indicators, validation, loading/success/error/disabled states. Errors must explain the fix — "Enter a valid email address," not "Invalid input." Inputs need comfortable height, rounded corners, clear borders, strong focus state, appropriate font size — never tiny, and touch-comfortable on mobile.

## Icons, avatars, badges

**Icons**: one consistent system (Lucide or Material Symbols), consistent stroke weight and size, used meaningfully — never random mixed icon sets, never purely decorative. Icon + text pairs keep consistent spacing (`[icon] Settings`).

**Avatars**: subtle, support image/initials/fallback, consistent sizes (24/32/40/48/64px).

**Badges**: for status, categories, roles, small metadata only — don't badge-ify every piece of information.

## Feedback: alerts, toasts, loading, empty, error

**Alerts**: four types — info, success, warning, error — compact, clear language.

**Toasts**: short-lived feedback only ("Changes saved," "Payment successful") — not for anything the user needs to read for a while.

**Loading**: every async action needs feedback — skeleton, spinner, progress, or button loading state. Skeletons should resemble the real content, not be random shapes. Never leave the user wondering if their action worked.

**Empty states**: explain what's missing and give the next action.

```
No products yet
Add your first product to start selling.
[Add product]
```

**Error states**: what happened → why it might have happened → what to do next.

```
We couldn't load this information.
Please check your connection and try again.
[Try again]
```

Never expose raw technical errors (`TypeError: Failed to fetch`) to ordinary users — put technical detail behind an expandable "details" section if needed at all.

**404 page**: simple and useful — "Page not found. The page you're looking for doesn't exist or has moved. [Go home]." Don't over-decorate it.

**Data states to always account for**: loading, success, empty, error, unauthorized, forbidden, offline/network failure. Never build only the happy path.

**Authorization messaging**: unauthenticated → "Please sign in to continue." Authenticated but lacking permission → "You don't have permission to access this page." Always give a next action.

**Confirmation dialogs**: only for consequential actions (delete account/product, cancel subscription, remove user, clear important data) — don't ask for confirmation on minor actions.

## Modals, drawers, dropdowns, tooltips

**Modals**: only when staying on the current page genuinely helps. Title, description, content, Cancel/Confirm actions. Support Escape, close button, focus trapping, keyboard nav, mobile responsiveness.

**Drawers**: mobile navigation, filters, detail panels, secondary controls — not a default for everything.

**Dropdowns**: easy to understand, keyboard accessible, clearly tied to their trigger, properly positioned, dismissible. Don't build a huge dropdown for a simple choice.

**Tooltips**: use only when necessary; never hide essential information inside one — they supplement labels, they don't replace them.

## Tables

Clear headings, comfortable row height, subtle borders, hover state, pagination, search, filtering, sorting where useful. On mobile, don't squeeze many columns into a tiny screen — use responsive cards, priority columns, expandable rows, or horizontal scroll where genuinely appropriate.

## Dashboards & admin systems

Dashboard structure: sidebar (Overview, Analytics, Customers, Products, Orders, Payments, Reports, Settings as relevant) + main area (page title, description, actions → summary cards → charts/tables → recent activity). Avoid clutter — not every metric needs a giant card.

Sidebar: logo, navigation, active state, group headings where useful, user/account area, collapse option where appropriate. Active state should be obvious without being visually loud.

Admin systems specifically prioritize: data clarity, search, filters, actions, permissions, audit info, status, bulk actions — and always confirm destructive actions.

## Auth, payments, e-commerce, POS

**Auth flows** (login, register, password reset, OTP/verification): same design system, clear branding, simple form, minimal distractions, strong validation, loading/error states, password visibility toggle, mobile-friendly.

**Payment UI**: must feel trustworthy — clear amount, clear merchant/product, payment method, security info where appropriate, clear confirmation and error handling. Avoid unnecessary animation here.

**E-commerce**: product-first layout. Product card = image, name, short metadata, price, optional rating, view/add action. Product page = large media, clear price, description, variants, quantity, CTA, delivery info, trust info. Avoid clutter.

**POS systems**: prioritize transaction speed over decoration — large touch-friendly controls, clear product search, visible cart, fast category navigation, keyboard support where appropriate, clear totals and payment controls.

## Project-type adaptation

Apply the same underlying principles, but weight priorities per project type:

- **SaaS**: dashboard, navigation, data, settings, billing, account management.
- **Marketplace**: search, categories, product cards, filters, seller info, checkout.
- **POS**: speed, touch targets, search, cart, payment.
- **School system**: students, teachers, classes, attendance, results, reports, notifications.
- **Business website**: brand, services, trust, contact, conversion.
- **Documentation/support**: search, categories, articles, breadcrumbs, related content, feedback.

## Security-aware UI

Never expose sensitive data unnecessarily. Show clear session states and permission-related messaging. Never display secrets. Confirm destructive operations. UI must respect backend authorization — hiding a UI element is never a substitute for real access control.

## Mobile, tablet, desktop

Mobile: test at 360/375/390/412px — no accidental horizontal overflow, touch-friendly buttons, readable text, working navigation, comfortable forms, a real mobile table strategy, modals that fit, images that scale.

Tablet: test around 768/820/1024px — don't just treat it as a big phone; use the extra space intentionally.

Desktop: test 1024/1280/1440/1600/1920px — avoid excessively stretched content at large widths.

Use framework-standard breakpoints rather than inventing dozens of custom ones.

## Dark mode (when required)

Don't just invert colors. Build a real dark theme: dark neutral background, elevated surfaces, appropriate text contrast, adjusted borders, adjusted primary color, accessible status colors. It should feel intentionally designed, not auto-generated.

## Accessibility & focus

Mandatory: semantic HTML, correct heading hierarchy, labels, keyboard navigation, focus indicators, accessible buttons, screen-reader-friendly controls, proper contrast, reduced-motion support, alt text, ARIA only where semantic HTML isn't enough. Never remove focus outlines without replacing them — keyboard users must always be able to see where they are. Interactive touch targets must be comfortably sized with enough spacing to prevent accidental taps.

## Animation & micro-interactions

Animation should communicate state or hierarchy, not decorate. Keep transitions subtle, roughly 150–250ms: hover, focus, expand/collapse, modal entrance, navigation, loading. Avoid constant floating elements, large parallax, excessive bouncing, long page entrances, distracting effects. Always respect `prefers-reduced-motion`.

Micro-interactions (button feedback, checkbox animation, menu transition, card hover, copy/save confirmation) should feel fast and unobtrusive, not showy.

## Images, illustration, content

Images: appropriate aspect ratios, efficient loading, meaningful alt text, no layout shift, lazy-load where appropriate. Don't add an image just because the page looks empty — whitespace is fine. Illustrations should be simple, minimal, brand-consistent, and purposeful — not random stock art.

**Content/UX writing**: short sentences, clear labels, helpful instructions, human language, consistent terminology, no unnecessary jargon. Prefer "Create account" over "Register," "Save changes" over "Submit," "Try again" over "Retry operation" — unless the audience genuinely expects technical terminology.

## Information hierarchy

Every page needs a clear top-to-bottom logic: page purpose → primary information → primary action → supporting information → secondary actions. Don't give every element equal visual weight.

## Performance

Avoid huge JS bundles, unnecessary client components, excessive animation, unoptimized images, repeated API calls, and heavy dependencies for simple UI. Prefer lightweight, reusable components.

## Technical implementation

**Next.js**: App Router where appropriate, Server Components by default, Client Components only when interaction/state genuinely requires them, optimized images, correct metadata, reusable layouts, real loading/error boundaries, minimal unnecessary client JS.

**React**: reusable components with clear single responsibilities, proper state management, accessible controls, avoid unnecessary re-renders. Never build one giant component containing the whole application.

**Tailwind**: consistent utility usage; extract repeated patterns into components instead of duplicating enormous class strings everywhere.

**Component system**: build reusable primitives — Button, Input, Textarea, Select, Checkbox, Radio, Switch, Card, Badge, Avatar, Tooltip, Dropdown, Dialog, Drawer, Tabs, Accordion, Toast, Alert, Skeleton, Pagination, Breadcrumb, Table — then compose them into app-specific components. Stay consistent: if one button uses 12px radius, don't give another button 4px without an intentional reason — consistency is what reads as quality.

## No generic AI UI

Avoid the telltale "AI-generated website" look: purple gradients everywhere, huge rounded cards, excessive glass effects, floating blobs, made-up statistics, unnecessary animation, too many pills, excessive shadows, fake testimonials, decorative icons scattered everywhere, huge centered headlines with little substance underneath. The result should feel like a real professional product.

## Design Review (run before calling any UI done)

**Layout** — Is spacing consistent? Is content aligned? Is hierarchy obvious?
**Typography** — Are headings proportional? Is body text readable?
**Components** — Are buttons consistent? Cards consistent? Inputs consistent?
**Responsive** — Does it work on mobile / tablet / desktop?
**Accessibility** — Fully keyboard-operable? Labels correct? Contrast sufficient?
**UX** — Are loading states present? Are errors useful? Are empty states helpful?

Then iterate: identify inconsistencies, improve spacing, improve hierarchy, improve responsive behavior, improve interaction states, remove unnecessary elements, test accessibility, refine — repeat until it feels intentional. The first implementation is a draft, not the deliverable.

## Final quality bar

Ask before shipping: Does this look like a professionally designed product rather than an AI-generated template? Can a new user understand it immediately? Does it feel calm and uncluttered? Is the hierarchy obvious? Does every interaction have appropriate feedback? Does it work beautifully on mobile? Is it accessible? Is the branding original (not Google's)? Is the UI consistent across every page? If any answer is no, keep improving before calling it done.
