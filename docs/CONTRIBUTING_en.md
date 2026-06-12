# Contributing to DreamCoder

Thank you for your interest in DreamCoder! Whether you're reporting a bug, suggesting a feature, or submitting code, all contributions are welcome.

## Code of Conduct

- Respect every contributor.
- Keep discussions constructive; no personal attacks.
- If you discover a security vulnerability, please contact the maintainer privately instead of filing a public Issue.

## How to Contribute

### Report a Bug

1. Search [Issues](https://github.com/GoDiao/dreamcoder/issues) to see if it has already been reported.
2. If not, open a new Issue with:
   - **Environment**: OS version, DreamCoder version (Settings → About).
   - **Steps to reproduce**: Clearly describe the actions that trigger the bug.
   - **Expected vs actual behavior**.
   - **Screenshots or logs** (if available).

### Feature Request

1. Search existing Issues first to avoid duplicates.
2. Open a new Issue describing:
   - What problem you want to solve.
   - What the feature should look like.
   - Why it's valuable to you.

### Submit Code

1. **Fork the repo** and create a feature branch from `dev`:
   ```bash
   git checkout dev
   git checkout -b feat/your-feature-name
   ```

2. **Develop**. Follow the project's code style:
   - TypeScript strict mode, avoid `any`.
   - React function components + Hooks.
   - Zustand for state management.
   - Tailwind CSS v4 for styling.

3. **Commit**. Use semantic commit messages:
   ```
   feat: add XXX feature
   fix: fix XXX issue
   refactor: refactor XXX
   docs: update XXX docs
   chore: miscellaneous changes
   ```

4. **Test**. Make sure your changes don't break existing functionality:
   ```bash
   cd desktop
   bun run lint    # TypeScript type checking
   bun run test    # run tests
   ```

5. **Submit a PR**. Target the `dev` branch. Describe what you changed and why.

## Project Structure

```
dreamcoder/
├── desktop/               # Tauri desktop app
│   ├── src/
│   │   ├── components/    # React components
│   │   ├── stores/        # Zustand state management
│   │   ├── lib/           # Utilities & runtime
│   │   ├── hooks/         # React Hooks
│   │   ├── pages/         # Page components
│   │   └── i18n/          # Internationalization
│   └── src-tauri/         # Rust backend
├── sidecar/               # Bun backend service
├── docs/                  # Documentation
└── adapters/              # Third-party platform adapters
```

## Development Environment

```bash
# Prerequisites
# - Bun >= 1.0
# - Rust (for compiling Tauri)
# - Node.js >= 18

git clone https://github.com/GoDiao/dreamcoder.git
cd dreamcoder/desktop
bun install
bun run tauri dev
```

## License

By contributing, you agree that your code will be licensed under the [MIT License](LICENSE).
