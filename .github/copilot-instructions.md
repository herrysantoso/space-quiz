# Copilot instructions

## Project rules

- Single file: `index.html` holds all markup, inline CSS, and inline JavaScript.
- No dependencies, frameworks, build step, or server. Keep changes inside this file.
- Follow the file's two-space indentation.

## Quiz data

- Questions are objects with `topic`, `prompt`, `options`, zero-based `answer`, and `fact`.
- Progress, question count, and results are derived from the question array length. Do not hardcode 10.

## Accessibility

- Use native buttons for answers.
- Keep the progress bar's ARIA value updates and the live feedback region.
- Keep focus moving to the question heading after advancing. The heading uses `tabindex="-1"` so script can focus it without adding it to the Tab order.
- Keep theme colors in the CSS custom properties in `:root` and the `prefers-color-scheme: dark` block, with sufficient contrast.
- Respect the existing reduced-motion media query when adding animation.

## Testing

- There is no test runner or linter. Open `index.html` directly in a browser.
- After every change, smoke test in the browser: answer correctly and incorrectly, check score and progress, finish all questions, check the results screen, and restart.
- Check both light and dark themes.
