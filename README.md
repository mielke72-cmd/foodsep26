# Weeknight Kitchen

A single-file meal plan app for Monday–Thursday cooking on a 4-week rotation: 16 recipes (low-FODMAP, meat-first, two fish nights per week), 8 shopping lists with tick-off checkboxes, and a "Tonight" banner that auto-selects the current week and day in Dubai time.

No build step, no dependencies — everything lives in `index.html`.

## Publish on GitHub Pages

1. Create a new repository (e.g. `meal-plan`) and upload `index.html` and this `README.md`.
2. In the repo: **Settings → Pages → Source: Deploy from a branch → Branch: `main` / root → Save**.
3. After a minute your app is live at `https://<your-username>.github.io/meal-plan/`.

Open it on your phone and "Add to Home Screen" for one-tap access in the kitchen or supermarket.

## Notes

- Shopping list ticks are saved in the browser's localStorage — per device, so your phone and Jamie's phone each keep their own list state.
- "Clear list" resets a shopping list for the next week.
- The week rotates automatically with the ISO calendar week (W1 → W2 → W3 → W4 → W1 …); tap a week button to jump ahead or back — for example, to preview next week's shopping list.
- On Friday–Sunday the Tonight banner shows an off-plan message and points at the coming Monday.
- To change recipes or list items, edit the `DATA` object at the top of the `<script>` block in `index.html` — it's plain JSON-style data, no other code changes needed.
