# User Guide

## First Run

1. Open the deployed site or `index.html`.
2. Wait until the status shows **Online (local WebAssembly)**.
3. The default HR dataset loads automatically.
4. Click the lightning button or press Ctrl/Command + Enter to run SQL.

## Importing CSV

1. Go to **Management > Import CSV to table**.
2. Enter a table name.
3. Choose a `.csv` file.
4. Click **Import**.
5. Open the **Schemas** tab to inspect the new table.

## Creating a Table

1. Click **Visual Table Designer**.
2. Enter a table name.
3. Enter one column definition per line.
4. Click **Create Table**.

Example:

```sql
id INTEGER PRIMARY KEY
name TEXT NOT NULL
created_at TEXT DEFAULT CURRENT_TIMESTAMP
```

## Exporting a Backup

1. Click **Export database (.sqlite)** or press Ctrl/Command + B.
2. Store the downloaded file privately.
3. Use clear names such as `analytics_2026-05-27_v1.sqlite`.

## Restoring a Backup

1. Click **Restore .sqlite backup**.
2. Choose a `.sqlite` or `.db` file.
3. Confirm restore.
4. The current browser database is replaced.

## Using Performance Tools

1. Run queries as usual.
2. Open the **Performance** panel.
3. Compare query time and row count.
4. Use indexes or better filters to optimize.

## Using Explain Plan

1. Select a query or place it in the editor.
2. Click **Explain**.
3. Read the generated query plan in the result grid.

## Clearing Local Data

1. Open **Settings**.
2. Click **Clear localStorage**.
3. Reload the page.

Use this on shared devices.
