# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Expense tracker app built with React 19 and Vite 7. This is a starter/learning project that intentionally contains bugs, poor UI, and messy code (used in a Claude Code course).

## Commands

- `npm run dev` — start dev server (http://localhost:5173)
- `npm run build` — production build to `dist/`
- `npm run lint` — ESLint (flat config, JS/JSX only)
- `npm run preview` — preview production build

No test framework is configured.

## Architecture

No routing, no backend, no external state management. Transaction data is hardcoded in state (not persisted).

- `src/App.jsx` — root component, owns the `transactions` array state
- `src/Summary.jsx` — computes and displays income/expenses/balance from transactions
- `src/TransactionForm.jsx` — owns form state, calls `onAddTransaction` callback to add entries
- `src/TransactionList.jsx` — owns filter state, renders filtered transaction table
- `src/App.css` — component styles
- `src/index.css` — global reset/base styles

## Known Issues

- "Freelance Work" is marked as `type: "expense"` but should be `type: "income"`
