# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Structure

This is a monorepo for reveal.js presentations where each talk folder is an independent package:

```
talks/
├── 2024 Westlake/          # Individual talk package
│   ├── package.json        # Talk-specific dependencies
│   ├── index.html          # Main presentation file
│   └── node_modules/       # reveal.js and dependencies
├── 2025 Conference/        # Another talk package
└── assets/                 # Shared assets (images, etc.)
```

## Working with Individual Talks

Each talk folder is a standalone package with its own:
- `package.json` with reveal.js dependencies
- `index.html` as the main presentation file
- Independent dependency versions (different talks may use different reveal.js versions)

## Common Commands

For any talk, navigate to the talk directory first:

```bash
cd "2024 Westlake"  # or any talk folder
npm install         # Install reveal.js dependencies
npm run dev         # Start development server
npm run build       # Build for production
npm run pdf         # Generate PDF (if configured)
```

## Creating New Talks

1. Create a new folder with the talk name (e.g., "2025 Conference")
2. Add `package.json` with reveal.js dependency
3. Create `index.html` with reveal.js structure
4. Run `npm install` to set up dependencies

## Architecture Notes

- No root package.json - each talk manages its own dependencies
- Talks are isolated and can use different reveal.js versions
- Shared assets go in the `assets/` folder
- All content is licensed under CC-BY-4.0