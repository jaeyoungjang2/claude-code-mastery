# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a minimal learning project for studying Claude Code and web development fundamentals. Currently, the project contains:
- `index.html`: Basic HTML template
- `main.js`: Simple JavaScript file with an `add()` function and a TODO comment for implementing a todo list

The project is in its early stages and does not yet have build tools, test frameworks, or linting configured.

## Project Structure

```
.
├── index.html          # HTML entry point (currently a basic template)
├── main.js             # JavaScript file (add function + TODO for todo list)
└── .idea/              # IDE configuration (ignore)
```

## Development

### Running the Project

This is a client-side web project with no build tools. To run:

1. Open `index.html` directly in a web browser, or
2. Use a local HTTP server:
   ```bash
   # Using Python (if available)
   python -m http.server 8000
   # Or Node.js
   npx http-server
   ```
3. Navigate to `http://localhost:8000` (or the configured port)

### Current TODO

The `main.js` file has a comment indicating the next task: create a todo list application. This should expand the project from the current simple `add()` function to a full todo list with features like adding, completing, and deleting items.

## Git Workflow

- **Main branch**: `main` (use for final, tested code)
- **Current branch**: Check `git branch` to see what you're working on
- **Remote**: Connected to `https://github.com/jaeyoungjang2/testtt.git`

## Future Enhancements

As the project grows, consider adding:
- `package.json` if using npm dependencies or build tools
- CSS file(s) for styling
- Jest or Vitest for unit tests
- ESLint for code linting
- Build setup if needed (Webpack, Vite, etc.)

## Notes for Claude Code Instances

- This is an educational/learning project, so prioritize clarity and best practices
- When implementing the todo list, keep the code structure simple and maintainable
- Consider making the HTML and JavaScript interact properly (e.g., form submission, DOM manipulation)
- Document any new features or significant code changes for future reference
