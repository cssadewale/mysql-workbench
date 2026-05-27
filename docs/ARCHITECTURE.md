# Architecture

## Design Goal

Provide a professional SQL workbench experience with free tools, static hosting, and no AI API.

## Runtime Architecture

```text
Browser
├── index.html
├── CSS interface
├── Vanilla JavaScript app controller
├── sql.js SQLite WebAssembly engine
├── Browser LocalStorage
└── Canvas charts / ERD
```

## Data Flow

1. User writes SQL in the editor.
2. JavaScript sends SQL to the in-browser SQLite database.
3. SQLite WebAssembly returns result sets.
4. The app renders tables, charts, schema metadata, audit events, and performance metrics.
5. User may export `.sqlite` or `.csv` files manually.

## Storage

- In-memory SQLite database for active data.
- LocalStorage for query tabs, saved queries, audit log, performance history, and settings.
- Downloaded files for backups and result exports.

## Cost Model

- Hosting: free static hosting.
- Database: in-browser SQLite, no server cost.
- AI: none.
- Build tooling: none required.
- CI: optional free GitHub Actions workflow.

## Why No AI API?

The target users need predictable zero operating cost. AI API billing can become expensive and may introduce privacy questions. The system therefore uses deterministic local SQL tooling instead.

## Production Considerations

For stricter environments:

- Vendor `sql.js` locally.
- Use a private repository.
- Add organizational guidance for sensitive data.
- Publish only synthetic sample data.
- If true multi-user access control is needed, build a separate backend product rather than modifying this static-only tool.
