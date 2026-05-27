# Privacy Notice

This application is designed for privacy and cost control.

## What Leaves the Browser?

By default, SQL statements, imported CSV data, generated tables, query history, and audit logs do not leave the browser. The app has no backend server and no AI API integration.

## LocalStorage Usage

The browser may store:

- Query tabs
- Saved queries
- Settings
- Audit events
- Performance history

This storage is local to the browser profile. Clear it from the Settings panel or from browser site data settings.

## External CDN

The default `index.html` loads `sql.js` from a free CDN. That request downloads the SQL engine script and WebAssembly file. Your imported data is not intentionally sent to the CDN.

For stricter offline/privacy environments, vendor the `sql.js` files locally and update `index.html` accordingly.
