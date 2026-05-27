# Security Policy

## Supported Version

The current maintained version is 3.x.

## Security Model

This is a static, client-side application. It does not include:

- Server authentication
- Multi-user authorization
- Cloud database storage
- AI API calls
- Payment processing

All user-created data is kept in browser memory or LocalStorage unless the user exports files.

## Data Safety Rules

- Do not publish real sensitive data in the repository.
- Treat exported `.sqlite` files as private backups.
- Clear LocalStorage on shared computers after use.
- Use private repositories if sample data resembles internal organizational data.

## Reporting Issues

Open a GitHub issue with:

1. A clear description.
2. Steps to reproduce.
3. Browser and operating system.
4. Screenshots if useful.

Do not include private data in public issues.
