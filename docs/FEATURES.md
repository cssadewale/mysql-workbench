# Detailed Feature Explanation

## 1. Local SQL Engine
The app uses SQLite compiled to WebAssembly through `sql.js`. Users can create tables, insert data, run SELECT queries, use joins, group data, and inspect results without installing MySQL, SQLite desktop software, or a backend server.

## 2. Query Tabs
Multiple SQL tabs allow users to separate experiments, reports, and lessons. Tabs are saved to LocalStorage when autosave is enabled.

## 3. Syntax Highlighting
The editor highlights SQL keywords, strings, comments, functions, and data types. This supports learning and improves readability.

## 4. SQL Formatter
The formatter reorganizes common SQL clauses onto separate lines and spaces comma-separated fields for cleaner reading.

## 5. SQL Lint Report
The lint checker warns about patterns such as `SELECT *`, missing `LIMIT` in exploration queries, and destructive commands like `DROP TABLE`.

## 6. Result Grid
Query results are displayed in a spreadsheet-like table with sticky headers, row striping, and support for null values.

## 7. CSV Import
CSV files can be imported into new SQLite tables. Table names and column names are sanitized to reduce invalid SQL errors.

## 8. Database Export
The full in-browser database can be exported as a `.sqlite` file. This supports backup, sharing, and portability.

## 9. SQLite Restore
Previously exported `.sqlite` files can be restored into the browser session. This replaces the current in-memory database.

## 10. Result CSV Export
The current result grid can be downloaded as a CSV file for Excel, Google Sheets, LibreOffice, or reporting.

## 11. Schema Explorer
The schema panel lists tables and columns. Users can quickly insert a `SELECT * FROM table LIMIT 10` query.

## 12. Visual Table Designer
Users can create tables by entering a table name and one column definition per line. This helps learners build schemas without writing full DDL from scratch.

## 13. Sample Datasets
Built-in HR, retail sales, and school record datasets allow immediate practice without external data.

## 14. SQL Reference and Snippets
The library includes common SQL patterns such as joins, grouping, CTEs, window ranking, indexes, and date filters.

## 15. Saved Query Library
Users can save useful SQL scripts locally and reinsert them later.

## 16. Explain Plan
Explain Plan runs `EXPLAIN QUERY PLAN` for the selected/current SQL statement to reveal how SQLite intends to execute it.

## 17. Performance Dashboard
Each query records execution time, row count, timestamp, and a SQL preview. This supports optimization and classroom discussion.

## 18. Audit Log
The audit log records local user actions such as queries, imports, exports, restores, errors, and sample dataset loads. It is useful for accountability and debugging, but it is not a tamper-proof compliance system.

## 19. Auto Visualization
The chart panel uses the Canvas API to draw a simple bar chart from the first numeric column in the latest result set.

## 20. ERD Diagram
The ERD panel draws table cards and columns from the current schema. Primary keys are marked where SQLite metadata identifies them.

## 21. Governance Center
The Governance modal explains privacy, auditability, continuity, and cost control decisions in plain language.

## 22. Backup Policy
The backup modal gives practical steps for manual backup discipline using exported SQLite files.

## 23. Dark/Light Theme
Users can toggle interface theme for accessibility and comfort.

## 24. Keyboard Shortcuts
- Ctrl/Command + Enter: run SQL
- Ctrl/Command + S: save current query
- Ctrl/Command + B: export SQLite backup
- Escape: close modal

## 25. No AI API
The application does not call any AI service. This avoids token billing, unpredictable operating costs, and data-sharing concerns.
