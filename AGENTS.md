# cis4120-hw1: Course Picker Home

CIS 4120 (Human-Computer Interaction) HW1, Penn, Spring 2026. Finished coursework, dormant.
A static phone-sized (390 x 844) HTML/CSS mock of Screen 1 of a course-selection app.
Stack: vanilla HTML5 + CSS3. No JavaScript, no build, no dependencies.

## Repo map
- `index.html`: all markup. Phone frame > header, search, filter chips, tabs, three course cards, "At a Glance" calendar, bottom nav.
- `styles.css`: all styling. Palette as custom properties on `:root`; calendar is CSS Grid (`.cal-head`, `.cal-grid`); one `@media (max-width: 420px)` rule sets the frame width to `min(390px, 95vw)`.
- `README.md`: features, run steps, testing in DevTools device mode, known limitations.
- `Screenshot 2026-01-21 at 23.43.37.png`: untracked local file, not part of the repo. Leave it alone.

## Commands
- Run: `open index.html` (macOS). No server needed.
- Test: none automated. Review in Chrome DevTools device toolbar at a ~390 px preset (iPhone 12, Pixel 5); see README "Testing".
- Deploy: GitHub Pages serves the default branch root at https://canduru4.github.io/cis4120-hw1/. Pushing to the default branch is the deploy; there is no workflow in the repo.

## Conventions
- Class names are kebab-case BEM-lite (`card-top`, `chip-primary`, `tab-active`, `nav-item active`).
- Colour variants are modifier classes (`card-yellow`, `card-orange`, `card-blue`; calendar `.block.green|yellow|beige|blue`). The palette lives in `:root` (`--yellow`, `--orange`, `--blue`, `--green`, `--beige`, `--navy`...), but the variant classes use hand-copied `rgba()` literals of those colours and many text/border colours are raw hex. Changing a palette variable does not recolour cards or calendar blocks; update the matching `rgba()` too.
- Calendar blocks are placed with inline `style="grid-column:N; grid-row:A / span B;"` on `.cell.block`; the grid is 44px label column + 5 day columns, 4 rows of 56px, so `grid-column` 2-6 = Mon-Fri.
- Section markers in HTML are `<!-- Name -->` comments; CSS uses three-line banners (`/* ====...` / `Section name` / `==== */`). Keep that style.
- Decorative glyphs/emoji carry `aria-hidden="true"`; landmark regions have `aria-label`. Controls are intentionally inert (no JS).
- Content (courses, ratings, instructors, times) is placeholder data, not real Penn data.

## Gotchas
- Repo was renamed from `CIS-4120-HW1`; the Pages URL changed with it. Use the lowercase URL above.
- README states the UI was generated with ChatGPT assistance then hand-edited; keep that acknowledgment if editing README.
- README follows the owner's standard skeleton (ends with License / Author). Keep that structure.

## Validation placement and reuse (owner update 2026-10-26)

- Follow the global Claude/Codex test policy and `~/Developer/personal/mac-mini/validation-economy/README.md` and `COVERAGE.md`. Focus first; full coverage only when the changed inputs require it. Docs-only policy edits need no application suite or deploy.
- This repo has no heavy pipeline. Keep its existing static/syntax/visual checks; do not invent a full suite or reserve capacity for a static upload.
- Brain is available only for a future compatible committed-source Python/Node check. This static repo needs no remote suite; browser checks and deployment outputs keep their existing rules.
- Reuse only supported receipts with matching source, coverage, dependencies, runtime/platform and relevant environment. Preserve passed unaffected batches; count remote results only when the owning gate aggregates them. Receipts do not replace required build artifacts or OS/device/browser proof. Split or offload an impossible reservation instead of waiting indefinitely; only stop your own obsolete jobs.
