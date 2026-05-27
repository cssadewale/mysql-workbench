# Contributing

Contributions are welcome. This project prioritizes free, portable, low-cost, client-side tools.

## Principles

1. **No AI API dependency** — do not add paid AI calls or server-side LLM dependencies.
2. **No mandatory backend** — the default app must work as static files.
3. **Low bandwidth** — avoid heavy frameworks unless there is a strong reason.
4. **Mobile/tablet usability** — preserve responsive layout and simple controls.
5. **Documentation first** — every new feature must be explained in `docs/FEATURES.md` and, if relevant, `docs/USER_GUIDE.md`.

## Development Workflow

1. Fork the repository.
2. Create a branch: `feature/your-feature-name`.
3. Make your changes.
4. Test `index.html` in Chrome, Edge, Firefox, or a modern Android browser.
5. Confirm that existing features still work: query execution, import, export, schema explorer, performance, audit log, and docs.
6. Open a pull request with a clear description.

## Code Style

- Use vanilla JavaScript where possible.
- Keep functions readable and documented through meaningful names.
- Avoid adding secrets, tokens, or private data.
- Sanitize user-created table and column names.
- Handle errors with visible console messages.
