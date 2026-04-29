# PRD: Meow Calendar

## Overview
Meow Calendar is a pastel kawaii-styled interactive web app that displays the current month. Clicking any day opens an animated popup featuring a randomly chosen cute cat (Ragdoll bicolor blue or Siberian tabby red) alongside a random meow sound and a short, inspiring English quote — giving users a delightful, mood-lifting surprise every single click.

## Problem Statement
Calendars are functional but often cold and uninspiring. Users — especially cat lovers — want a small moment of joy when they interact with their daily planner. A cute animated cat with an uplifting message turns a mundane check-in into a micro-moment of happiness.

## Goals
- Deliver a charming, immediately usable browser experience with zero setup required
- Make every calendar day click feel fresh and surprising
- Create a cohesive pastel kawaii visual identity

## Non-Goals
- No user accounts, login, or data persistence
- No calendar editing, event creation, or reminders
- No month navigation (current month only)
- No AI-generated content at runtime (no API keys required)

## Users
Cat lovers and kawaii aesthetic fans who want a playful, mood-boosting browser experience. No technical knowledge required — open in browser and enjoy.

## User Stories
- As a user, I want to open the app and immediately see the current month displayed in a pastel kawaii style.
- As a user, I want today's date to stand out with a special pastel glow so I always know where I am.
- As a user, I want to click any day and see an animated cute cat pop up with a meow sound.
- As a user, I want a different cat breed, animation, meow sound, and quote every time I click — even on the same day.
- As a user, I want the experience to work entirely in the browser with no installation.

## Functional Requirements

### MVP
- **Calendar view**: Display current month in a pastel kawaii grid layout. Show day names (Mon–Sun). Correctly pad the start of the month.
- **Today highlight**: Today's date cell has a distinct pastel glow effect (e.g. soft pink or lavender pulse/glow animation).
- **Past days**: Past day cells appear slightly muted/faded compared to future days.
- **Click any day**: Clicking any day (past, today, or future) opens a modal popup.
- **Modal popup**:
  - Animated cat: randomly choose either a Ragdoll bicolor blue cat or a Siberian tabby red cat on each click
  - Cat animation: CSS-animated cute cat (bounce, tail wag, or blink loop — must feel lively, not static)
  - Meow sound: randomly play one from a collection of at least 5 different meow audio clips
  - Inspiring quote: randomly select one from a curated list of 30+ short English quotes (cat-themed or universally uplifting, max ~12 words each)
  - Close button (X) to dismiss
- **Quotes feel random**: Use a shuffle/weighted-random approach so the same quote does not repeat consecutively
- **Design**: Pastel kawaii throughout — soft pinks, lavenders, mints, creams; rounded fonts; subtle decorative elements (paw prints, stars, hearts)
- **Language**: English only, all UI text

### Quote Pool (30 quotes — ship all of these in the app)
1. "Every day is a fresh start, even for cats."
2. "You are purrfectly capable of amazing things."
3. "Land on your feet — you always do."
4. "Curiosity leads to the best adventures."
5. "Stretch, breathe, and take on the day."
6. "You have nine lives worth of potential."
7. "Be as fearless as a cat on a rooftop."
8. "Today holds something wonderful for you."
9. "Nap when you need to. Then conquer."
10. "Trust your instincts — they purr with wisdom."
11. "Even the smallest paw leaves a big mark."
12. "You are loved more than you know."
13. "Chase what makes your heart leap."
14. "Rest is part of the journey, not a detour."
15. "Great things happen one soft step at a time."
16. "You are exactly where you need to be."
17. "Land gracefully — you always find your footing."
18. "The sun is out and so is your potential."
19. "Be bold. Be curious. Be magnificently you."
20. "Every purr starts with a single breath."
21. "You deserve all the warmth today brings."
22. "Small joys add up to a beautiful life."
23. "Leap — the landing always works itself out."
24. "Your presence makes the world cozier."
25. "Today is a good day to be wonderfully alive."
26. "Shine like sunlight on a warm windowsill."
27. "You are braver than any cat on the internet."
28. "Make today as cozy as a cat nap in the sun."
29. "The best is always just around the corner."
30. "You are one-of-a-kind and absolutely enough."

### Meow Sound Collection
Include at least 5 distinct meow audio clips (short, medium, long, questioning-inflection, chirpy). Use royalty-free audio. Recommended source: freesound.org — search "cat meow" filter by CC0 license. Embed as base64 or serve as static files alongside the HTML.

### Cat Animations
Build both cats as pure CSS + HTML/SVG animated characters — no external image dependencies. Each cat must have at least one looping animation (e.g. tail wag, ear flick, blink). Ragdoll: blue-grey and white coloring. Siberian: warm red/orange tabby coloring.

## Non-Functional Requirements
- **Performance**: App loads in under 2 seconds on a standard connection. No external API calls at runtime.
- **Compatibility**: Works in latest Chrome, Firefox, and Safari.
- **Accessibility**: Modal is keyboard-dismissible (Escape key). Focus is trapped inside modal while open.
- **Self-contained**: Single `index.html` file (or minimal file set) — clone and open, no build step required.

## Success Metrics
- App opens and renders correctly with no console errors
- Clicking any day always triggers cat + sound + quote
- No two consecutive clicks produce the identical cat + quote + sound combination
- Today's date is correctly identified and glows

## Technical Constraints
- No backend required — pure frontend (HTML, CSS, JavaScript)
- No runtime API keys
- Meow audio must be embedded or served as static local files (no external CDN audio)
- Cat visuals must be CSS/SVG — no external image URLs

## Open Questions
- Should clicking outside the modal (backdrop) also close it? (Recommended: yes)
- Should the meow play automatically on modal open, or require a click? (Recommended: auto-play on open)
