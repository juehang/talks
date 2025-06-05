# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Structure

This is a repository for Slidev presentations managed from the root:

```
talks/
├── 2025 Westlake/          # Individual talk folder
│   ├── slides.md           # Main presentation file
│   └── public/             # Talk-specific assets
├── 2025 Conference/        # Another talk folder
├── assets/                 # Shared assets (images, etc.)
├── package.json            # Root dependencies (Slidev)
└── node_modules/           # Shared Slidev installation
```

## Working with Talks

All talks are managed from the root directory using a shared Slidev installation:

- Each talk has a `slides.md` file as the main presentation
- Talk-specific assets go in their `public/` folder
- All talks share the same Slidev version from root dependencies

## Common Commands

From the root directory:

```bash
npm run slidev --talk="2025 Westlake"  # Start specific talk in dev mode
slidev "2025 Westlake/slides.md"       # Alternative syntax
slidev export "2025 Westlake/slides.md" # Export to PDF
slidev build "2025 Westlake/slides.md"  # Build for production
```

## Creating New Talks

1. Create a new folder with the talk name (e.g., "2025 Conference")
2. Create `slides.md` with Slidev frontmatter and content
3. Optionally create `public/` folder for talk-specific assets
4. Run from root: `npm run slidev --talk="2025 Conference"`

## Architecture Notes

- Single root package.json with shared Slidev dependencies
- All talks use the same Slidev version for consistency
- Shared assets go in the `assets/` folder
- Talk-specific assets go in each talk's `public/` folder
- All content is licensed under CC-BY-4.0