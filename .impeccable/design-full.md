---
name: Dual-Unit Weather
description: Current conditions for your location in °F and °C, side by side.
colors:
  signal-blue: "#2563eb"
  signal-blue-deep: "#1d4ed8"
  signal-ring: "rgba(37,99,235,.16)"
  ink: "#111827"
  slate-text: "#374151"
  muted-gray: "#6b7280"
  card-white: "#ffffff"
  mist-field: "#eef2f7"
  hairline: "#e5e7eb"
  control-stroke: "#d1d5db"
typography:
  display:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica, Arial, sans-serif"
    fontSize: "clamp(64px, 17vw, 120px)"
    fontWeight: 700
    lineHeight: 1
    letterSpacing: "-0.035em"
    fontFeature: "tnum"
  display-compact:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica, Arial, sans-serif"
    fontSize: "clamp(50px, 13.5vw, 100px)"
    fontWeight: 700
    lineHeight: 1
    letterSpacing: "-0.035em"
    fontFeature: "tnum"
  title:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica, Arial, sans-serif"
    fontSize: "18px"
    fontWeight: 600
    letterSpacing: "0.2px"
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica, Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.45
  detail:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica, Arial, sans-serif"
    fontSize: "14px"
    fontWeight: 400
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica, Arial, sans-serif"
    fontSize: "13px"
    fontWeight: 500
rounded:
  control: "10px"
  card: "16px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "12px"
  lg: "20px"
  xl: "28px"
components:
  button-primary:
    backgroundColor: "{colors.signal-blue}"
    textColor: "{colors.card-white}"
    rounded: "{rounded.control}"
    padding: "10px 12px"
  button-primary-hover:
    backgroundColor: "{colors.signal-blue-deep}"
  button-secondary:
    backgroundColor: "{colors.card-white}"
    textColor: "{colors.ink}"
    rounded: "{rounded.control}"
    padding: "10px 12px"
  button-link:
    textColor: "{colors.signal-blue}"
    padding: "0 8px"
    height: "44px"
  input-search:
    backgroundColor: "{colors.card-white}"
    textColor: "{colors.ink}"
    rounded: "{rounded.control}"
    padding: "10px 12px"
  card:
    backgroundColor: "{colors.card-white}"
    rounded: "{rounded.card}"
    padding: "24px 28px 28px"
    width: "min(100%, 720px)"
  dial:
    typography: "{typography.display}"
    textColor: "{colors.ink}"
    padding: "8px 8px 12px"
  placeholder:
    textColor: "{colors.slate-text}"
    height: "140px"
---

# Design System: Dual-Unit Weather

## Overview

**Creative North Star: "The Twin Dial"**

The page is the two readings. °F and °C sit side by side at display size, split by a single hairline, like two faces of one instrument. Everything else is in service of those two numbers and stays quiet: a small title row naming the place, one muted line of conditions, and a single text control to change the city.

The feel is friendly and light. One white card floats on a soft gray field, corners are gently rounded, and a single weather emoji gives the page its warmth. Type is the visitor's own system font, so the page feels native on every device. Density is low: one card, one glance.

Signal Blue is the one voice of action. It marks what can be pressed and where keyboard focus is, and nothing else.

**Key Characteristics:**
- Two equal readings at display size, divided by one vertical hairline; neither unit leads.
- No boxes inside the card: separation comes from space and hairlines.
- A single centered white card on a pale gray gradient field.
- System font stack throughout; tabular figures on every number.
- One accent color, reserved for interaction.
- Emoji as the only iconography, hidden from screen readers.

## Colors

A cool, near-neutral gray palette with one confident blue for everything interactive.

### Primary
- **Signal Blue** (`signal-blue`): the Search submit button, link-style controls, focus outlines and the spinner's moving arc.
- **Signal Blue Deep** (`signal-blue-deep`): hover state of the primary button only.
- **Signal Ring** (`signal-ring`): the soft glow under the primary button.

### Neutral
- **Ink** (`ink`): the readings, the place name and primary text.
- **Slate Text** (`slate-text`): messages, notices and search feedback.
- **Muted Gray** (`muted-gray`): the conditions line, "Feels like" lines, unit symbols and placeholder text.
- **Card White** (`card-white`): the card surface and field backgrounds.
- **Mist Field** (`mist-field`): the page background, drawn as a soft vertical gradient (#f9fafb → #eef2f7 at 60% → #e5e7eb).
- **Hairline** (`hairline`): the card border, the divider between the readings, the rule above search and the spinner track.
- **Control Stroke** (`control-stroke`): the 1px border on inputs and secondary buttons.

### Named Rules
**The One Signal Rule.** Signal Blue appears only on things you can press and on focus. Text, numbers, borders and decoration never use it.

## Typography

**Display Font:** System UI stack (-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica, Arial)
**Body Font:** The same stack

**Character:** One native family everywhere, so the page reads like part of the device. Hierarchy comes from a very large jump between the readings and everything else.

### Hierarchy
- **Display** (700, clamp(64px, 17vw, 120px), line-height 1, tracking -0.035em, tabular figures): the two readings only. The unit symbol is set at 0.34em, weight 600, in Muted Gray, raised to the cap line.
- **Display Compact** (same, clamp(50px, 13.5vw, 100px)): used for both readings whenever either needs three characters (101°F, −42°F), so the pair always fits and stays equal.
- **Title** (600, 18px, tracking 0.2px): the place name, led by the condition emoji.
- **Body** (400, 16px, line-height 1.45): base text, buttons, the search field and messages.
- **Detail** (400, 14px): "Feels like" lines, notices and search feedback.
- **Label** (500, 13px): the conditions line under the title ("Partly cloudy · Wind 3.6 m/s · Updated 6 min ago").

### Named Rules
**The Readings Are Loudest Rule.** Only the two temperatures use the Display sizes. Nothing else on the card competes with them, in size or in color.

**The Equal Pair Rule.** Both readings always share one size step. If one switches to Display Compact, both do.

## Layout

A single card, `min(100%, 720px)` wide with a 16px page gutter, centered in the viewport on wide screens and pinned to the top on phones. Inside it, top to bottom:

1. A header row: place name and conditions line on the left, "Change city" on the right. It wraps below the title on narrow screens.
2. The readings: a two-column grid, 28px below the header, split by a 1px Hairline.
3. A notice line, only when an update failed.
4. The search panel when open, separated by a Hairline rule: field and button in a `minmax(0, 1fr) auto` grid with an 8px gap, feedback directly beneath the field, then "Or use my location".

Spacing runs from tight to generous: 4px inside a line, 8px between a control and its partner, 12px between a reading and its "Feels like" line, 20–28px between regions. Below 480px the card padding drops to 20px 16px 24px. Nothing scrolls horizontally at 320px.

### Named Rules
**The Side-by-Side Rule.** The °F and °C readings always share a row at equal width. They never stack, and they never resize independently.

**The Reading Stays Rule.** Once a reading is on screen, it stays there. Updates dim it; failures add a notice beneath it. Only the first load shows a placeholder in its place.

## Elevation & Depth

Flat, with one lift. The card is the only raised surface: a soft ambient shadow (`0 8px 30px rgba(0,0,0,.08)`) plus a Hairline border lets it float gently off the gray field. Inside the card nothing has a fill, border box or shadow of its own; regions are separated by space and single hairlines. The primary button carries a faint blue glow (`0 2px 10px` in Signal Ring).

### Named Rules
**The One Lift Rule.** Only the card casts a shadow, and nothing inside it is boxed.

## Shapes

Gently rounded: controls 10px, the card 16px. Borders are 1px. Dividers are single straight hairlines, never dashed. The spinner is the only circle.

## Components

### Buttons
Confident and tactile: clear fills, comfortable padding and an unmistakable focus outline.
- **Shape:** gently rounded (10px), with a 1px border.
- **Primary:** Signal Blue fill, white text, matching border and a soft blue glow; Signal Blue Deep on hover. Used once per screen, for Search.
- **Secondary:** Card White fill, Ink text, Control Stroke border. Used for "Try again" before any reading exists.
- **Link:** transparent and borderless, Signal Blue text, underlined on hover, with a 44px-tall hit area. Used for "Change city", "Close", "Try again" notices, city choices and "use my location".
- **Focus:** a 2px solid Signal Blue outline, offset 2px, on every control.
- **Disabled:** 60% opacity, no glow, not-allowed cursor.

### Inputs / Fields
- **Style:** Card White, 1px Control Stroke border, 10px radius, padding 10px 12px, body type.
- **Focus:** the 2px Signal Blue outline plus a Signal Blue border.
- **Feedback:** messages sit directly beneath the field in Slate Text (14px, 500) and are linked to it for screen readers.

### Twin Dials (signature)
The heart of the system. Two identical columns, each holding a reading in Display type with a raised muted unit, and a "Feels like" line beneath it in its own unit. A single 1px Hairline divides them. While an update runs they dim to 45% opacity (0.3s ease-out) with a small spinner beside the conditions line; the numbers never disappear.

### City Choices
When a search matches several places with the same name, up to four appear under the field as link-style buttons with a distinguishing region ("Portland, OR", "Portland, ME", "Portland, Victoria, Australia").

### Placeholder
Shown in the readings' place only before the first reading: a centered message in Slate Text, at least 140px tall, with a spinner while loading or "Try again" after a failure. No fill, no border.

## Do's and Don'ts

### Do:
- **Do** keep °F and °C at the same size step, weight and color.
- **Do** use tabular figures for every number.
- **Do** keep the last reading on screen through updates and failed searches.
- **Do** reserve Signal Blue (#2563eb) for pressable things and focus, per the One Signal Rule.
- **Do** show focus with the 2px solid Signal Blue outline, offset 2px.
- **Do** put feedback next to the thing it is about: search messages under the field, update failures under the readings.

### Don't:
- **Don't** make one unit primary: no toggle, and no larger or brighter reading for either unit.
- **Don't** box anything inside the card: no tinted panels, dashed outlines or nested shadows.
- **Don't** use the Display sizes for anything except the two readings.
- **Don't** add a Refresh button; the page refreshes itself when you come back to it.
- **Don't** introduce a second accent color for decoration.
