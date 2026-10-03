# Copilot instructions

## Project

Orbit is a standalone, browser-based space exploration quiz. Its entry point and current implementation are in the root `index.html`.

## Technology and structure

- Use vanilla HTML, CSS, and JavaScript only. Do not add frameworks, build tools, package managers, or runtime dependencies.
- Keep the app self-contained in `index.html` unless a change genuinely benefits from splitting files.
- Use native browser APIs and modern JavaScript (`const` and `let`; no `var`).
- Do not add a server requirement. The quiz must continue to work when `index.html` is opened directly as a local file.

## UI and accessibility

- Preserve the narrow, centered quiz layout and mission-control visual style.
- Preserve both `prefers-color-scheme: dark` and `prefers-color-scheme: light` appearances. Use the existing CSS custom properties for colors and related theme styling.
- Use semantic HTML and native interactive elements. Keep keyboard navigation, visible focus indicators, and focus management working through answering, advancing, results, and restart flows.
- Keep progress and feedback understandable to assistive technology; preserve appropriate live regions, labels, and progress-bar values.
- Hide decorative visuals from assistive technology. Respect `prefers-reduced-motion` for animations.
- Maintain readable contrast and responsive behavior, including on narrow screens.

## Quiz behavior

- Keep quiz content in the existing question data structure and preserve the score, progress, answer feedback, results, and restart behavior.
- Ensure correct answers increment the score once only; incorrect answers do not increment it.
- Preserve the celebratory high-score results treatment for scores of 8 or more.

## Validation

- For UI or behavior changes, open or reload `index.html` in the integrated browser and exercise the affected interactions.
- For quiz-flow changes, check correct and incorrect answers, score/progress updates, completion, and restart as applicable.
- There is no package manifest or automated test runner; do not introduce one just to validate a small change.
