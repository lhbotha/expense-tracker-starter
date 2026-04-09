# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm run dev      # Start dev server at http://localhost:5173
npm run build    # Production build
npm run lint     # Run ESLint
npm run preview  # Preview production build
```

## Architecture

This is a single-file React app — all logic lives in `src/App.jsx`. There is no routing, no state management library, and no backend; state is in-memory only (resets on refresh).

**Known issues (intentional for course purposes):**
- `amount` is stored as a string, causing string concatenation instead of numeric addition in the income/expense/balance totals.
- Transaction type "Freelance Work" is hardcoded as `type: "expense"` but categorized under `"salary"`.
- No delete functionality on transactions.
