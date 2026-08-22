---
name: Damone — Safe Home · Healthy Living
description: A trilingual, low-pressure Melaleuca landing page that reads like a quiet, honest conversation, not a funnel.
colors:
  cream: "#faf6ef"
  cream-deep: "#f2ecdf"
  ink: "#2c2a24"
  ink-soft: "#5a564a"
  sage: "#5f7a5f"
  sage-deep: "#3f5940"
  terracotta: "#c17a52"
  terracotta-wash: "rgba(193,122,82,0.1)"
  mustard: "#c9a24a"
  line: "#e4dccb"
typography:
  display:
    fontFamily: "Fraunces, Georgia, serif"
    fontSize: "clamp(28px, 4.2vw, 40px)"
    fontWeight: 500
    lineHeight: 1.22
    letterSpacing: "-0.01em"
  body:
    fontFamily: "Work Sans, system-ui, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.55
    letterSpacing: "normal"
  label:
    fontFamily: "Work Sans, system-ui, sans-serif"
    fontSize: "13px"
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: "0.18em"
rounded:
  xs: "12px"
  sm: "14px"
  md: "18px"
  lg: "22px"
  pill: "999px"
spacing:
  sm: "8px"
  md: "16px"
  lg: "24px"
  xl: "32px"
components:
  button-primary:
    backgroundColor: "{colors.sage-deep}"
    textColor: "#ffffff"
    rounded: "{rounded.pill}"
    padding: "15px 30px"
  button-primary-hover:
    backgroundColor: "{colors.sage}"
  chip-tag:
    backgroundColor: "{colors.terracotta-wash}"
    textColor: "{colors.terracotta}"
    rounded: "{rounded.pill}"
    padding: "5px 11px"
---

# Design System: Damone — Safe Home · Healthy Living

## Overview

**Creative North Star: "The Quiet Kitchen Table"**

This is a conversation, not a funnel. Every surface should feel like sitting down with someone who has nothing to sell you in the first five minutes — warm cream paper, unhurried serif headlines, and soft sage-and-terracotta accents that never shout. The page exists to turn cold social traffic into a low-pressure WhatsApp chat, so the design's whole job is to feel personal, patient, and specific — never like a template, never like a pitch deck.

The aesthetic is **warm editorial calm**: think a thoughtful personal essay or a well-typeset home-and-wellness column, not a SaaS landing page or an MLM opportunity flyer. Layout is narrow and centered (max 720–780px), type does most of the work, and color is used sparingly as accent, not decoration. The system explicitly rejects the generic AI-template tells — Inter/Arial, purple-to-blue gradients, cards nested in cards, icon tiles above every heading — in favor of a warm serif/sans pairing and a single grounded palette.

**Key Characteristics:**
- Narrow, centered, single-column reading measure (~720–780px)
- Warm cream paper background, never pure white or dark mode
- Serif display type for headlines, clean grotesque sans for body and UI
- Soft, ambient shadows everywhere — nothing sits flush on the page
- Exactly one accent action per screen (the WhatsApp button), pill-shaped, never urgent-colored (no red/orange alert tones)
- Scroll-triggered reveal (fade + blur-in) as the only motion, respecting reduced-motion

## Colors

The palette reads as a warm, sun-bleached paper world — cream, sage, and terracotta — with no black, no pure white, and no cool grays anywhere.

### Primary
- **Deep Forest Sage** (`#3f5940` / `sage-deep`): the one call-to-action color. Used only for the WhatsApp button and the language-toggle active state — its rarity is what makes it read as "the next step," not decoration.

### Secondary
- **Sage** (`#5f7a5f` / `sage`): the CTA's hover state and small dividing rules. A lighter, less final version of Deep Forest Sage — the hand reaching out, not yet the handshake.
- **Warm Terracotta** (`#c17a52` / `terracotta`): the categorization accent — section tags and eyebrows (`At Home`, `Everyday Energy`, `示范例子`). Always shown at low opacity as a wash (`terracotta-wash`, `rgba(193,122,82,0.1)`) behind full-strength terracotta text, never as a solid fill.

### Tertiary
- **Muted Mustard** (`#c9a24a` / `mustard`): appears only on `compare.html`, marking the second comparison category (`② 个人护理`). A third categorical color for a three-category comparison table — don't introduce it on pages that only have one or two categories.

### Neutral
- **Warm Linen** (`#faf6ef` / `cream`): page background throughout.
- **Soft Sand** (`#f2ecdf` / `cream-deep`): recessed surface for cards and blocks that sit slightly "behind" the page.
- **Warm Charcoal Ink** (`#2c2a24` / `ink`): all primary text and headlines. Warm near-black, never pure `#000`.
- **Muted Taupe** (`#5a564a` / `ink-soft`): secondary text — subheads, captions, footer copy.
- **Soft Sand Line** (`#e4dccb` / `line`): the only border/divider color in the system.

### Named Rules
**The One Accent Rule.** Deep Forest Sage is the only color allowed on an interactive call-to-action. Terracotta and mustard are for labeling and categorization only — never buttons, never links.

## Typography

**Display Font:** Fraunces (with Georgia, serif fallback)
**Body Font:** Work Sans on the English/BM page (with system-ui, sans-serif fallback); Noto Sans SC on the Chinese comparison page (with system-ui, sans-serif fallback)

**Character:** An unhurried, slightly literary serif for headlines against a clean, humanist grotesque for body copy and UI — the pairing of a hand-written letter's heading with a plainly-typed body.

### Hierarchy
- **Display** (weight 500, `clamp(28px, 4.2vw, 40px)`, line-height 1.22): hero `h1` only. Fraunces, letter-spacing -0.01em.
- **Title** (weight 500, 21px, line-height 1.3): block/card headings (`.block h2`). Still Fraunces.
- **Body** (weight 400, 15.5–17px, line-height 1.55): paragraph copy. Work Sans (or Noto Sans SC on the ZH comparison page).
- **Label** (weight 600, 10–13px, letter-spacing 0.18–0.2em, uppercase): tags, eyebrows, language-toggle buttons. Work Sans.

### Named Rules
**The Two-Voice Rule.** Only two type families exist on any single page: one serif for headlines, one sans for everything else. Never introduce a third family, and never use the serif for body copy or the sans for a hero headline.

## Layout

Single centered column, `max-width: 720–780px`, with `24px` (`.wrap`) horizontal padding on mobile. Section rhythm is generous vertical padding (56–72px) rather than visible dividers. Below `640px` all grids collapse to one column; the two-column problem blocks and three-column comparison steps only appear at `min-width: 620–640px`. Density is unhurried — plenty of whitespace between sections — consistent with the "read this slowly" tone, not a dashboard's density.

## Elevation & Depth

The system is **layered and ambient**, never flat and never hard-edged. Every card, block, step, and button carries a soft, diffuse shadow at rest — depth is a constant ambient quality of the paper, not something that only appears on interaction. Shadows deepen and lift slightly further on hover, but they are present from the very first paint.

### Shadow Vocabulary
- **Ambient card** (`box-shadow: 0 1px 2px rgba(44,42,36,0.04), 0 16px 36px -18px rgba(44,42,36,0.18)`): resting state for `.block`, `.card`, `.step`.
- **Ambient card, hover** (`box-shadow: 0 1px 2px rgba(44,42,36,0.05), 0 22px 44px -18px rgba(44,42,36,0.22)`): on hover, paired with a `-3px` vertical lift.
- **CTA glow** (`box-shadow: 0 10px 26px -10px rgba(63,89,64,0.5)`): the WhatsApp button at rest, using the sage-deep color tinted into the shadow itself rather than a neutral gray shadow.

### Named Rules
**The Tinted Shadow Rule.** Shadows are never neutral gray — they're tinted from the ink or the element's own accent color (warm charcoal for cards, sage for the CTA), so depth reads as warm, not corporate.

## Shapes

Corners are consistently soft, never sharp. Cards and blocks use a generous `18–22px` radius; smaller elements (tags, chips, the numbered step badges) use fully-rounded pills (`999px`) or circles. No element uses a 0px or small (`<8px`) radius — hard corners don't appear anywhere in the system.

## Components

### Buttons
- **Shape:** fully rounded pill (`border-radius: 999px`).
- **Primary (WhatsApp CTA):** Deep Forest Sage background, white text, `15–16px 30–32px` padding, bold 600–700 weight, inline WhatsApp glyph SVG at 20px with its own hover micro-animation (nudges right and up, scales to 1.08).
- **Hover / Focus:** background lightens to Sage, button lifts `-2px` with the CTA-glow shadow deepening; on active/press it settles back down and scales to 0.97 with a fast 0.15s transition.
- **Secondary:** none exists yet — this is a single-CTA system by design (see Do's and Don'ts).

### Chips (tags/eyebrows)
- **Style:** low-opacity color wash background (10–12% opacity of the category color) with full-strength text in that same color; uppercase, heavily letter-spaced (0.18–0.2em), pill-shaped.
- **State:** static/labeling only — chips are never interactive in this system.

### Cards / Containers
- **Corner Style:** 18–22px radius (see Shapes).
- **Background:** Soft Sand (`cream-deep`) for blocks/steps sitting on the cream page; pure white (`#fff`) for the comparison cards on `compare.html`, which sit one layer further "forward" than the page.
- **Shadow Strategy:** ambient card shadow at rest, deepening on hover (see Elevation & Depth).
- **Border:** a thin (`1px`) low-opacity warm border (`rgba(228,220,203,0.55–1)`) on most cards; the comparison cards on `compare.html` use a fully-opaque Soft Sand Line border instead.
- **Internal Padding:** generous — `22–32px`, never tight.

### Navigation
- **Language toggle (index.html only):** three pill buttons in a row, transparent with a Soft Sand Line border by default; the active language gets a solid Deep Forest Sage fill with white text. Hover on inactive pills only shifts the border to Sage — no background change until selected.

## Do's and Don'ts

### Do:
- **Do** keep the CTA singular — one WhatsApp button per page, in Deep Forest Sage, pill-shaped.
- **Do** use the tinted-ambient shadow on every card-like surface, even at rest.
- **Do** keep corners soft everywhere (18px+ on containers, pill/circle on small elements).
- **Do** treat terracotta and mustard as label-only colors, always at low opacity as a wash behind full-strength text.

### Don't:
- **Don't** introduce Inter, Arial, purple-to-blue gradients, or stacked cards-in-cards — these are the generic AI-template tells this system was built to avoid (per PRODUCT.md).
- **Don't** use red, orange, or other urgency/alert colors anywhere — the palette has no "urgent" register on purpose; this is a low-pressure page.
- **Don't** add a second CTA color or a second interactive button style without a documented reason; the One Accent Rule exists to keep the ask singular.
