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

Single-component app — all state and UI live in `src/App.jsx`. No routing, no backend, no external state management. Transaction data is hardcoded in state (not persisted).

Key files:
- `src/App.jsx` — entire application (form, filters, summary cards, transaction table)
- `src/App.css` — component styles
- `src/index.css` — global reset/base styles

## Known Issues

- Transaction amounts are stored as strings, causing summary calculations (income/expenses/balance) to concatenate instead of sum
- "Freelance Work" is marked as `type: "expense"` but should be `type: "income"`
