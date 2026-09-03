---
name: news
description: Newspaper theme with a serif masthead, compact section rail, lead-story grid, ruled supporting coverage, and a cool light-grey canvas.
license: MIT
metadata:
  author: Aimeos
---

# News Theme Design System

## Mission

Build credible newspaper pages that make dense reporting easy to scan and give the lead story unmistakable priority.

## Brand

News is sober, current, and information-led. The canvas is light grey (`#ECEFF1`), newsprint surfaces are off-white (`#F8F9FA`), text is ink (`#172126`), crimson (`#A02B33`) marks sections and actions, and slate blue (`#35566A`) supports utility areas. It uses Pico CSS and the existing markup in `theme/views/`.

## Style Foundations

- Typography: Iowan Old Style, Baskerville, Georgia, or the nearest system serif for masthead and headlines; Arial/Helvetica/system sans-serif for navigation, dates, controls, and metadata
- Headline rhythm: compact line height, decisive weight, and a clear size difference between lead and supporting stories
- Surfaces: one continuous off-white news sheet sits on the light-grey canvas; rules divide coverage instead of card shadows
- Geometry: `--pico-border-radius: 0`; cards, dialogs, fields, and buttons stay square
- Accent: crimson is reserved for sections, primary actions, focus, dates, and active navigation
- Images: editorial crops use `16 / 10`, list and article leads use `16 / 9`, with restrained saturation
- Maximum width: 1280px shared news desk, with narrower article and prose measures for readability

## Component Rules

- Header: place a compact edition band above the centered masthead and a separate section rail on desktop; collapse to one accessible menu below 992px
- Hero: use a text-and-image lead grid on wide screens and stack it on small screens; background-image variants retain a strong ink overlay
- Story listings: give the lead story two-thirds of the width and stack supporting headlines in the remaining column
- Cards: separate adjacent stories with thin rules, never floating rounded containers or shadows
- Articles: keep introductions and body copy on a narrow measure while cover images retain visual authority
- Buttons: use uppercase sans-serif labels, square borders, a crimson primary action, and a pale secondary action
- Footer: use ruled link columns on a cool-grey surface and repeat the masthead identity below them

## Accessibility

- Keep text and controls at WCAG 2.2 AA contrast or better
- Use a visible 3px crimson focus outline with a 3px offset
- Preserve semantic headings, navigation labels, dialogs, details, dates, and skip links
- Do not use color alone for active navigation; combine it with an inset rule
- Keep touch targets at least 2.25rem high and allow navigation labels to wrap on mobile
- Respect reduced-motion preferences for shared interactive components

## Content and Tone

- Write direct headlines that state what changed and why it matters
- Prefer concrete nouns, quantities, decisions, and consequences over slogans
- Keep standfirsts short enough to scan in a dense front-page layout
- Use descriptive link text such as `Read the electricity-grid analysis`, not `Learn more`

## Prohibited Patterns

- No pill buttons, rounded cards, glass effects, heavy shadows, or decorative textures
- No invented utility markup inside CMS components; style the structures from `theme/views/`
- No oversized marketing gradients or motion that competes with reading
- No copied publication branding, logos, article text, or proprietary photography

## QA Checklist

- Edition band, masthead, and section rail remain usable at 320px and 1280px
- Keyboard focus is visible on navigation, dropdowns, search, forms, and story links
- Lead and supporting story hierarchy remains clear without relying on image content
- Card and article images retain their intended aspect ratios
- Long section names do not overlap search or subscription actions
- JSON schema, PHP syntax, demo seeding, representative route rendering, PHPUnit, and PHPStan pass
