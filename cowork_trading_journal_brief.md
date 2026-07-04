# Build brief: XAUUSD trading journal (standalone web app)

## What I want
A personal trading journal web app for logging XAUUSD trades, accessible from my computer browser and from my phone's browser (added to my phone home screen like an app). Single user, personal use only — no need for multi-user accounts or public sharing.

## Core requirements
- Real persistence: trades need to be saved permanently and synced across my computer and phone — not just stored in one browser's local storage. Use a proper backend/database so the same data shows up wherever I open the app.
- Accessible via a URL I can open on desktop and mobile.
- Installable to phone home screen (PWA-style: manifest + icon so it opens full-screen like an app, no browser chrome).
- Works well on a small mobile screen as well as desktop.

## Data to capture per trade
- Date
- Pair (default XAUUSD)
- Direction: Buy / Sell
- Result: Win / Loss / Breakeven
- Actual RR exited (number)
- Actual RR price reached (number, optional — used for win-quality analysis)
- Confidence (1–5)
- Trade quality (star rating)
- Grade (A / B / C / D / F)
- H1 context (text)
- M15 area of interest (text)
- M5 confirmation (text)
- M1 trigger (text)
- Rule followed? (Yes/No)
- One lesson (text)
- Mistake (text)
- Screenshot before (image upload)
- Screenshot after (image upload)

## Stats dashboard (top of page)
- Win rate (%)
- Total trades
- Wins
- Losses
- Overall avg RR (across every trade)
- Avg RR exited — wins only
- Avg RR reached — wins only
(The gap between the last two shows how much RR I'm leaving on the table by closing early — I compare them myself, no extra calculated "gap" stat needed.)

## Trade list / browsing
- List view of all trades, most recent first
- Each row shows: date, pair, direction, result, RR exited, grade
- Click a row to expand and see full notes + both screenshots
- Click a screenshot to view it full-size / zoomed
- Edit and delete existing trades

## Visual style
- Dark theme throughout (no white backgrounds) — dark charcoal page background, slightly lighter card surfaces
- Gold/amber accent color (ties to gold trading)
- Color-coded direction: Buy = blue, Sell = amber/orange
- Color-coded result: Win = green, Loss = red, Breakeven = grey
- Color-coded grade: A = green, B = blue, C = gold, D = orange, F = red
- Clean, data-dense "trading terminal" feel — monospace font for numbers/data, not overly decorated

## Other notes
- No login/auth complexity needed beyond whatever's simplest to keep it private to me (e.g. a single shared password or IP-based access is fine — Cowork can suggest the simplest secure option).
- Images should be compressed/resized on upload so storage doesn't balloon over time.
- This replaces an earlier prototype I had running as a Claude artifact — that version worked but only persisted data inside Claude's environment, which is why I need a real standalone version now.
