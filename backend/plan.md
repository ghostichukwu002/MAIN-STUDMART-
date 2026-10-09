# STUDMART polish and hosting plan

## Goal
Make the supplied STUDMART marketplace starter feel launch-ready and straightforward to host, without changing its core product flows.

## Implementation
- Make the Node API serve the static frontend from the same deployment, with safe static-file handling, SPA fallback, security headers, and a health endpoint.
- Use a relative `/api` frontend default so one-service deployments work without editing source; preserve the global override for split frontend/backend hosting.
- Add root deployment metadata and a practical README covering one-service and split hosting, required environment variables, persistent storage, and production cautions.
- Add the route manifest required for the frontend page set.
- Tighten frontend polish with metadata/accessibility improvements and preserve the existing responsive visual language.
- Fix small reliability issues around persistence directory creation and browser history navigation.

## Design direction
- **Movement:** Editorial campus commerce — warm modernism with a restrained burgundy signature color.
- **Principles:** Clear hierarchy, approachable student energy, calm whitespace, and purposeful motion.
- **Color philosophy:** Burgundy communicates confidence and community; blush surfaces soften the experience; gold is a small discovery accent; green is reserved for positive states.
- **Layout:** A persistent campus desk/sidebar on desktop that collapses into a thumb-friendly mobile navigation bar.
- **Signature elements:** The S-mark, rounded listing cards, and orbit/floating-note hero composition.
- **Interaction:** Every primary action is visible, low-friction, and gives immediate feedback through states/toasts.
- **Animation:** Short page/card reveals and subtle floating/shine motion; reduced-motion users are respected.
- **Typography:** Manrope for confident display and DM Sans for practical UI copy.
- **Brand essence:** A trusted student-to-student marketplace for finding useful campus deals quickly. Personality: warm, capable, local.
- **Voice:** Direct, encouraging, campus-aware. Example CTAs: “Find your next good deal.” and “Give your unused stuff a new campus life.”
- **Wordmark:** Geometric S tile paired with a compact all-caps wordmark and campus descriptor.
- **Signature color:** Deep STUDMART burgundy `#701d3a`.

## Project structure
- `frontend/`: static application shell, styles, client-side state, and route manifest.
- `backend/`: Node HTTP API, JSON persistence, and same-origin static hosting.
- Root `package.json` and `render.yaml`: deployment entry points for a single web service.
