# Meow Calendar 🐱

A pastel kawaii-styled interactive web calendar. Click any day to get a surprise animated cat, a meow sound, and an uplifting quote!

## What it is

Meow Calendar displays the current month in a soft, cute pastel style. Every day you click opens a pop-up featuring:

- A randomly chosen animated CSS cat — either a **Ragdoll** (blue-grey & white) or a **Siberian tabby** (warm orange/red) — with looping animations (tail wag, ear flick, blinking)
- A synthesised **meow sound** (5 distinct sounds generated via Web Audio API — no external files needed)
- A randomly selected **inspiring quote** from a curated pool of 30 — never the same one twice in a row

Today's date glows with a soft pastel pulse animation. Past days appear gently faded.

## How to open it

Just open `index.html` in any modern browser — no build step, no server, no dependencies.

```
open index.html         # macOS
start index.html        # Windows
xdg-open index.html     # Linux
```

Or visit the live GitHub Pages version if deployed.

## Tech

- Pure HTML + CSS + JavaScript — single file, zero dependencies
- Cats built entirely from CSS shapes (no images)
- Audio synthesised with the Web Audio API
- Works in Chrome, Firefox, and Safari

## Features

| Feature | Detail |
|---|---|
| Calendar | Current month, correct day padding, Sun–Sat headers |
| Today highlight | Pastel pink/lavender glow pulse animation |
| Past days | Muted/faded appearance |
| Cat animation | Bounce loop + tail wag + ear flick + blink |
| Meow sounds | 5 synthesised tones (short, long, questioning, chirpy, deep) |
| Quote pool | 30 curated quotes, no consecutive repeat |
| Modal dismiss | Close button, Escape key, or click backdrop |
| Accessibility | Focus trap inside modal, keyboard navigable |
