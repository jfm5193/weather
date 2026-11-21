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

<!-- impeccable:design-map -->
Name: Dual-Unit Weather
Colors: primary: signal-blue #2563eb; neutral: ink #111827; primary: signal-ring rgba(37,99,235,.16); primary: signal-blue-deep #1d4ed8; neutral: slate-text #374151; neutral: muted-gray #6b7280 (+4 more in the sidecar)
Fonts: -apple-system (display, display-compact, title, body, detail, label)
Spacing: xs 4px, sm 8px, md 12px, lg 20px, xl 28px
Radius: control 10px, card 16px
North Star: "The Twin Dial"
Rules:
- The One Signal Rule. Signal Blue appears only on things you can press and on focus.
- The Readings Are Loudest Rule. Only the two temperatures use the Display sizes.
- The Equal Pair Rule. Both readings always share one size step.
- The Side-by-Side Rule. The °F and °C readings always share a row at equal width.
- The Reading Stays Rule. Once a reading is on screen, it stays there.
- The One Lift Rule. Only the card casts a shadow, and nothing inside it is boxed.
Don't:
- Don't make one unit primary: no toggle, and no larger or brighter reading for either unit.
- Don't box anything inside the card: no tinted panels, dashed outlines or nested shadows.
- Don't use the Display sizes for anything except the two readings.
- Don't add a Refresh button; the page refreshes itself when you come back to it.
- Don't introduce a second accent color for decoration.
Do:
- Do keep °F and °C at the same size step, weight and color.
- Do use tabular figures for every number.
- Do keep the last reading on screen through updates and failed searches.
- Do reserve Signal Blue (#2563eb) for pressable things and focus, per the One Signal Rule.
- Do show focus with the 2px solid Signal Blue outline, offset 2px.
- Do put feedback next to the thing it is about: search messages under the field, update failures under the readings.
Full: .impeccable/design-full.md (read a section when you need its detail)
