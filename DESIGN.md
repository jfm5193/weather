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

<!-- impeccable:design-map -->
Name: Dual-Unit Weather
Colors: primary: signal-blue #2563eb; neutral: ink #111827; primary: signal-ring rgba(37,99,235,.16); neutral: slate-text #374151; neutral: muted-gray #6b7280; neutral: card-white #ffffff (+4 more in the sidecar)
Fonts: -apple-system (display, title, body, detail, label)
Spacing: xs 6px, sm 8px, md 12px, lg 20px
Radius: control 10px, panel 12px, card 16px
North Star: "The Twin Dial"
Rules:
- The One Signal Rule. Signal Blue appears only on things you can press and on focus.
- The Readings Are Loudest Rule. Only the two temperatures use the Display size.
- The Side-by-Side Rule. The °F and °C dials always share a row at equal width.
- The One Lift Rule. Only the card casts a shadow.
Don't:
- Don't make one unit primary: no toggle, and no larger or brighter reading for either unit.
- Don't add shadows to anything inside the card.
- Don't use the Display size for anything except the two temperature readings.
- Don't introduce a second accent color for decoration.
Do:
- Do keep °F and °C as two identical dials of equal size, weight and color.
- Do reserve Signal Blue (#2563eb) for pressable things and focus, per the One Signal Rule.
- Do use the system font stack and express hierarchy through size and weight.
- Do keep radius growing with container size: 10px controls, 12px panels, 16px card.
- Do show focus with the 3px Signal Ring outline on every interactive element.
Full: .impeccable/design-full.md (read a section when you need its detail)
