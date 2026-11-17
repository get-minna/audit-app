# Audit Tracker — SFRS(I) & SSA

A single-page audit testing app for financial workbooks, aligned to Singapore Financial Reporting Standards (International) and Singapore Standards on Auditing.

- **Issue tracker** — issues ranked by risk level (High / Medium / Low) and priority (P1–P3), driven by amount vs materiality and test weighting
- **Where to find it** — file › sheet › row › column › cell, with a highlighted preview of the source rows
- **Standards links** — each issue links to SSA / SFRS(I) paragraphs with the specific requirement lines highlighted
- **Excel upload** — `.xlsx`, `.xls`, `.xlsm`, `.csv` parsed in the browser (SheetJS); 18 automated tests

All data stays in the browser (`localStorage`). Nothing is uploaded to a server.

## Deploy on Vercel

1. Push this repo to GitHub.
2. In Vercel: **Add New → Project → Import** `get-minna/audit-app`.
3. Framework preset: **Other**. Leave Build Command and Output Directory empty (static site, served from the repo root).
4. Click **Deploy**.

`vercel.json` adds clean URLs and security headers (CSP allows only cdnjs for SheetJS and Google Fonts).

## Run locally

Open `index.html` in a browser, or serve it:

```bash
npx serve .
```

## Notes

- Standards text is paraphrased for working-paper reference; verify against the ISCA Handbook and ASC pronouncements.
- Data is per-browser; use **Copy as CSV** on the Issues tab to export findings.
