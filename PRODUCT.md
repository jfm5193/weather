# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

One primary user: the owner, opening the page for a quick personal check of the current weather. The job is a glance (what is it like outside right now?), not research or planning.

## Product Purpose

A single-page weather check that shows current conditions for the visitor's location, or a searched city, in both °F and °C at once. It succeeds when one glance answers "what's it like out?" with no conversion, setup or waiting.

## Positioning

- **Both units at once:** Fahrenheit and Celsius sit side by side with equal weight. There is no unit toggle and no preference to set.
- **Fast and minimal:** one screen, no ads, no sign-up, no accounts. It opens and answers immediately.

## Operating Context

- Opened in a browser and served from GitHub Pages over HTTPS, so geolocation is available.
- Location comes from browser geolocation by default. City search is the fallback and the alternative.
- A manual Refresh re-fetches conditions for the current place.

## Capabilities and Constraints

- **Current data shown:** temperature, feels-like temperature, a condition label with an icon from WMO weather codes, wind speed (m/s), last-updated time and place name.
- **Data sources:** Open-Meteo forecast and geocoding, with BigDataCloud as a fallback for reverse geocoding. These are free and need no API key.
- **Current stack:** one static `index.html` that loads React 18 and Babel from unpkg and compiles JSX in the browser. It deploys to GitHub Pages via `.github/workflows/static.yml`, which uploads the whole repository root.
- **Open to a rebuild:** moving to a framework or a build step is acceptable if it helps. The deploy must still end up on GitHub Pages unless decided otherwise.
- **Roadmap:** an hourly and/or multi-day forecast is planned but not built.
- **Undecided:** how a forecast fits a glance-first page; whether wind should also show in mph or km/h.

## Evidence on Hand

- No logo, brand name or assets beyond the working title "Dual-Unit Weather (°F | °C)".
- No users, testimonials or metrics. This is a personal tool, so none should be invented.

## Product Principles

1. **Glance first.** The current temperature in both units is the answer. Everything else supports it or waits behind it.
2. **Units are equals.** Neither °F nor °C is the primary one; no change should make one subordinate.
3. **Zero friction.** No accounts, keys, settings or ads stand between opening the page and seeing the weather.
4. **Forecast without clutter.** When forecasts arrive, they must not slow down or crowd the current-conditions glance.
