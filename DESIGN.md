---
name: Dual-Unit Weather
description: Current conditions for your location in °F and °C, side by side.
colors:
  signal-blue: "#2563eb"
  signal-ring: "rgba(37,99,235,.16)"
  ink: "#111827"
  slate-text: "#374151"
  muted-gray: "#6b7280"
  card-white: "#ffffff"
  mist-field: "#f5f6f8"
  hairline: "#e5e7eb"
  control-stroke: "#d1d5db"
  status-wash: "#fafafa"
typography:
  display:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica, Arial, sans-serif"
    fontSize: "clamp(40px, 8vw, 64px)"
    fontWeight: 700
    letterSpacing: "-0.5px"
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
  panel: "12px"
  card: "16px"
spacing:
  xs: "6px"
  sm: "8px"
  md: "12px"
  lg: "20px"
components:
  button-primary:
    backgroundColor: "{colors.signal-blue}"
    textColor: "{colors.card-white}"
    rounded: "{rounded.control}"
    padding: "10px 12px"
  button-secondary:
    backgroundColor: "{colors.card-white}"
    textColor: "{colors.ink}"
    rounded: "{rounded.control}"
    padding: "10px 12px"
  button-link:
    textColor: "{colors.signal-blue}"
    padding: "6px 8px"
  input-search:
    backgroundColor: "{colors.card-white}"
    textColor: "{colors.ink}"
    rounded: "{rounded.control}"
    padding: "10px 12px"
  card:
    backgroundColor: "{colors.card-white}"
    rounded: "{rounded.card}"
    padding: "20px 20px 16px"
    width: "min(92vw, 680px)"
  dial:
    rounded: "{rounded.panel}"
    padding: "8px 0"
    height: "120px"
  status-panel:
    backgroundColor: "{colors.status-wash}"
    textColor: "{colors.slate-text}"
    rounded: "{rounded.panel}"
    padding: "18px"
    height: "120px"
---

# Design System: Dual-Unit Weather

## Overview

**Creative North Star: "The Twin Dial"**

The whole page is built around two equal readings, °F and °C, sitting side by side like a pair of gauges on one instrument. Everything else is in service of those two numbers: a small title row naming the place, a short line of details underneath, and controls tucked into the corner.

The feel is friendly and light. One white card floats on a soft gray field, corners are gently rounded, and a single weather emoji gives the page its warmth. Type is the visitor's own system font, so the page feels native on every device. Density is low: one card, one glance.

Signal Blue is the one voice of action. It marks what can be pressed and where keyboard focus is, and nothing else.

**Key Characteristics:**
- Two identical temperature dials of equal weight; neither unit leads.
- A single centered white card on a pale gray gradient field.
- System font stack throughout; weight and size carry hierarchy, not typefaces.
- One accent color, reserved for interaction.
- Emoji as the only iconography.

## Colors

A cool, near-neutral gray palette with one confident blue for everything interactive.

### Primary
- **Signal Blue** (`signal-blue`): the primary Refresh button fill, link-style buttons, input and button focus borders, and the loading spinner's moving arc.
- **Signal Ring** (`signal-ring`): a translucent wash of Signal Blue, used for focus outlines (3px) and the soft glow under the primary button.

### Neutral
- **Ink** (`ink`): primary text, the temperature numbers and the place name.
- **Slate Text** (`slate-text`): detail rows and status messages; one step softer than Ink.
- **Muted Gray** (`muted-gray`): the subtitle line, "Feels like" lines, unit symbols and secondary values.
- **Card White** (`card-white`): the card surface, and the background of inputs and secondary buttons.
- **Mist Field** (`mist-field`): the page background tone. On screen it is drawn as a soft vertical gradient (#f9fafb → #eef2f7 at 60% → #e5e7eb).
- **Hairline** (`hairline`): the card border, the dashed dial outlines and the spinner track.
- **Control Stroke** (`control-stroke`): the 1px border on inputs and secondary buttons.
- **Status Wash** (`status-wash`): the background of the loading, error and idle panel.

### Named Rules
**The One Signal Rule.** Signal Blue appears only on things you can press and on focus. Text, numbers, borders and decoration never use it.

## Typography

**Display Font:** System UI stack (-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica, Arial)
**Body Font:** The same stack

**Character:** One native family everywhere, so the page reads like part of the device. Hierarchy comes from a big jump in size and weight between the readings and everything else.

### Hierarchy
- **Display** (700, clamp(40px, 8vw, 64px), tracking -0.5px): the two temperature readings only. The unit symbol is set at 0.45em in Muted Gray.
- **Title** (600, 18px, tracking 0.2px): the place name, led by the current-condition emoji.
- **Body** (400, 16px, line-height 1.45): base text, buttons and the search input.
- **Detail** (400, 14px): the condition, wind, updated and location rows; values are emphasized in bold.
- **Label** (500, 13px): the subtitle line under the title. "Feels like" lines use the same 13px size in Muted Gray.

### Named Rules
**The Readings Are Loudest Rule.** Only the two temperatures use the Display size. Nothing else on the card is allowed to compete with them.

## Layout

A single centered card, sized `min(92vw, 680px)` and centered both ways in the viewport. Inside it, the stack runs top to bottom:

1. A header row with the title and subtitle on the left and the controls on the right.
2. The twin dials in a two-column grid with a 12px gap.
3. A two-column grid of detail rows with a 6px gap.
4. The search form when shown: the input and button in a `1fr auto` grid with an 8px gap.

Spacing steps are small and even (6, 8, 12, 20px). Below 480px, the detail grid collapses to one column and the header aligns to the top. The two dials stay side by side at every width.

### Named Rules
**The Side-by-Side Rule.** The °F and °C dials always share a row at equal width. They never stack, and they never resize independently.

## Elevation & Depth

Mostly flat, with one lift. The card is the only raised surface: a soft ambient shadow (`0 8px 30px rgba(0,0,0,.08)`) plus a Hairline border lets it float gently off the gray field. Inside the card everything is flat, separated by dashed or solid hairlines and the Status Wash tint. The primary button carries a faint blue glow (`0 2px 10px` in Signal Ring) that marks it as the main action.

### Named Rules
**The One Lift Rule.** Only the card casts a shadow. Interior panels use borders or tint, never their own shadow.

## Shapes

Gently rounded everywhere, with radius growing alongside the size of the container. Controls are 10px, interior panels 12px and the card 16px. Borders are 1px. The temperature dials use a dashed Hairline outline, which reads as a gauge face rather than a box. The spinner is the only circle.

## Components

### Buttons
Confident and tactile: clear fills, comfortable padding and a visible focus ring.
- **Shape:** gently rounded (10px), with a 1px border.
- **Primary:** a Signal Blue fill with white text, a matching border and a soft blue glow. Used once per screen, for Refresh.
- **Secondary:** a Card White fill, Ink text and a Control Stroke border. Used for Search submit and Retry.
- **Link:** transparent and borderless, Signal Blue text, tighter padding (6px 8px). Used for Search/Hide search, "Use my location" and "Search for a city".
- **Hover / Focus:** border-color and shadow ease over 0.15s. Focus-visible shows a 3px Signal Ring outline and shifts the border to Signal Blue.
- **Disabled:** 60% opacity with a not-allowed cursor.

### Inputs / Fields
- **Style:** Card White, 1px Control Stroke border, 10px radius, padding 10px 12px, body type.
- **Focus:** the same 3px Signal Ring outline and Signal Blue border as buttons.

### Cards / Containers
- **Corner Style:** 16px.
- **Background:** Card White on the Mist Field gradient.
- **Shadow Strategy:** the one lifted surface (see Elevation & Depth).
- **Border:** 1px Hairline.
- **Internal Padding:** 20px 20px 16px.

### Temperature Dial (signature)
The heart of the system. There are two of them, identical except for the unit. Each is a centered column at least 120px tall with a dashed Hairline outline and a 12px radius. It holds the reading in Display type with a small muted unit symbol, and a "Feels like" line beneath it in Muted Gray.

### Status Panel
It fills the dials' place while loading, on error, or before a location is chosen. It is at least 120px tall with a Status Wash background, a 1px #eee border and a 12px radius, and its message is centered in Slate Text. Loading pairs the message with an 18px spinner: a Hairline track with a Signal Blue arc, rotating once per second. The error state adds a secondary Retry button and a link-style "Search for a city".

## Do's and Don'ts

### Do:
- **Do** keep °F and °C as two identical dials of equal size, weight and color.
- **Do** reserve Signal Blue (#2563eb) for pressable things and focus, per the One Signal Rule.
- **Do** use the system font stack and express hierarchy through size and weight.
- **Do** keep radius growing with container size: 10px controls, 12px panels, 16px card.
- **Do** show focus with the 3px Signal Ring outline on every interactive element.

### Don't:
- **Don't** make one unit primary: no toggle, and no larger or brighter reading for either unit.
- **Don't** add shadows to anything inside the card.
- **Don't** use the Display size for anything except the two temperature readings.
- **Don't** introduce a second accent color for decoration.
