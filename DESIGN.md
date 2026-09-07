---
name: Gerhard Breukers
description: Case studies of apps that already run in front of people.
colors:
  night: "#07140c"
  flood: "#e8f06a"
  paper: "#f3efe4"
  ink: "#14130f"
  live: "#b42318"
  rule: "#14130f"
typography:
  display:
    fontFamily: "Big Shoulders Display, Arial Narrow, Impact, sans-serif"
    fontSize: "clamp(3.2rem, 12vw, 9rem)"
    fontWeight: 800
    lineHeight: 0.86
    letterSpacing: "-0.03em"
  body:
    fontFamily: "Atkinson Hyperlegible, Segoe UI, sans-serif"
    fontSize: "1.05rem"
    fontWeight: 400
    lineHeight: 1.55
rounded:
  none: "0px"
spacing:
  gutter: "clamp(18px, 4vw, 48px)"
  measure: "1320px"
components:
  button-primary:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.paper}"
    rounded: "{rounded.none}"
    padding: "12px 18px"
---

# Design System: Gerhard Breukers

## Overview

**Creative North Star: "The match-day programme"**

The site is a printed club programme, not a developer landing page. The cover is the live product at night. Inner pages are paper, black ink, and large plates of the work. Chrome recedes.

**Key Characteristics:**
- The artifact leads. Bio comes after the work.
- Sharp corners. Hairline rules. No cards-in-a-grid.
- Floodlight yellow only on the night cover. Paper everywhere else.
- Condensed display type like a fixture list, not a fashion serif.

## Colors

Night and floodlight are taken from the One More Year capture. Paper is the inner pages.

**The Cover Rule.** Floodlight yellow exists only on the night cover. It does not decorate the paper pages.

## Typography

**Display Font:** Big Shoulders Display
**Body Font:** Atkinson Hyperlegible

Condensed sports numbers for titles. A face designed to be read for the case studies.

## Layout

Full-bleed cover at `100svh` minus the masthead. Then a single column of plates, each a large still plus a short caption row. Gutter `clamp(18px, 4vw, 48px)`. Measure 1320px.

## Elevation & Depth

No drop shadows. Depth is the photograph and the crop.

## Shapes

Radius 0. Buttons are rectangles. Rules are 1px ink.

## Components

### Buttons
Ink fill, paper type, no radius. Hover inverts to flood only on the cover; on paper, hover fills live red.

### Navigation
Sticky paper masthead, hairline underneath. Always readable. GitHub hides on small screens.

## Do's and Don'ts

### Do:
- **Do** let the first viewport be a real product still.
- **Do** keep claims identical to the written case studies.

### Don't:
- **Don't** use gold-on-charcoal cards.
- **Don't** put the biography above the work.
- **Don't** round the corners of photographs.
