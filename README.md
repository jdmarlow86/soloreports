# Solo Reports

A mobile-first, static business expense tracker and reporting workspace. See `index.html` for the app.

## Features
- Expense and income records with date, payee, amount, payment method, category, business purpose, and optional receipt file.
- Business/personal designation and payee-based auto-categorization rules.
- Starter Chart of Accounts for COGS, operating expenses, income, and personal/owner categories.
- Dashboard totals, category breakdown, transaction search/filtering, date-range P&L, tax summary, and expense detail.
- CSV import/export, JSON backup, print-to-PDF reporting, mobile receipt capture, and optional image OCR preview.

## Deploy
Enable GitHub Pages in Settings → Pages → Deploy from a branch → `main` / `/(root)`. No build step is required.

## Important limitations
- Data is stored in this browser's localStorage only. It does not sync across devices or users. Export a JSON backup regularly. Receipt files are embedded in browser storage and limited to 3 MB each.
- Bank, card, PayPal, and Square statement CSV imports are supported. Direct account connections are not enabled; production OAuth/API integrations require a secure server-side service. Never place API secrets in browser code.
- Image OCR is best-effort and requires a network-loaded Tesseract.js library. Verify all extracted fields. PDF OCR is not included.
- Reports are bookkeeping summaries, not tax advice or a guarantee of deductibility. Ask a qualified tax professional to review categories and tax treatment.

## CSV import
Minimum columns: `Date`, `Payee` (or Vendor/Description), and `Amount`. Optional: `Payment Method`, `Category`, `Purpose` (or Memo/Notes), and `Type` (Income/Expense). Review imported rows and complete business-purpose and receipt details before relying on reports.
