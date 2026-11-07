# Contracted Entities Statement

Arabic tracker for contracted entities. It records totals before and after review, and the difference, by year, type, category and entity.

## What it does

- Has five tabs: Data Entry, Import, Dashboard, Entities and Account.
- Dashboard: total before review, total after review and the difference, with filters for year, type, category and entity, and a button that resets the filters.
- Imports `.xlsx`, `.xls` and `.csv` files, with a choice of which rows to import. Restores a JSON backup and exports to `.xlsx` with a right-to-left view.
- Undo for edits. Arabic and English interface, and a system, light or dark theme.
- Optional cloud sync. Signing in with Google keeps several documents in the cloud. A quick sync code links two devices without an account, and the page asks which data to use when the two differ.

## What it does not do

- Cloud sync needs https and a connection. A cloud document has a size limit, and the page warns as the data approaches it.
- The sync code is the only way to reach the data from another device, and it cannot be recovered if lost.
- It keeps a cache of the data and the settings in the browser's `localStorage` under `entitiesStatementApp:cache:v1`. Clearing site data removes it.

## Network and install

Loads Google Fonts. SheetJS 0.20.3 loads from cdn.sheetjs.com when an Excel file is imported or exported. The Firebase SDK 12.16.0 loads from gstatic.com, and Firebase Authentication and Firestore are called, only when cloud sync is used. Not installable; no service worker.

## Built with

One HTML file, with no build step and no framework. Firebase 12.16.0 provides sign-in and storage for the sync, and SheetJS 0.20.3 reads and writes the workbooks.

## Run locally

Serve the folder with any static file server. Cloud sync needs the page to be opened over https.
