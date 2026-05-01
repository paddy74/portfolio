# Personal Website Portfolio

This is my personal website portfolio &mdash; including my resume, project highlights, work samples, technical reference documentation, and the occasional blog post. It is built with [Docusaurus](https://https://docusaurus.io/).

## Developer Guide

- **Package Manager**: [`pnpm`](https://pnpm.io/)
- **Linter**:
  - TypeScript: [ESLint](https://eslint.org/)
  - CSS: [Stylelint](https://stylelint.io/)
  - Markdown: [markdownlint](https://github.com/DavidAnson/vscode-markdownlint/)
- **Code Formatter**:
  - [Prettier](https://prettier.io/)
  - Markdown: [Markdown All in One]([yzhang.markdown-all-in-one](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one))
- **Pre-Commit Hooks**: [prek](https://prek.j178.dev/)

You must [install pnpm](https://pnpm.io/installation) before continuing if it is not already on your system.

```bash
cd website
# shamefully-hoist to handle issues with docusaurus-lunr-search
pnpm install --shamefully-hoist
pnpm run start

# Type check, lint, format
pnpm run typecheck
pnpm run lint
pnpm run format

# Install pre-commit hooks
prek install
```

### Key Development Principles

<!-- add additional principles (keep minimal) -->

- Maintain 100% passing tests, at least 80% test coverage, formatting, and linting before opening a pull request.
- Update docstrings alongside code changes to keep the generated reference accurate.

## Contributing

Contributions are welcome! As this is my personal website, contributions are reserved for correcting things like spelling errors, bugs, or suboptimal code/configurations. To get started:

1. Fork the repository and create a new branch.
2. Install development dependencies (see the [developer guide](#developer-guide)).
3. Add or update tests together with your change.
4. Run the full test, linting, and formatting suite locally.
5. Submit a pull request describing your changes and referencing any relevant issues.

For major changes, open an issue first to discuss your proposal.

## Contact

Questions or issues regarding this project's source code or its documentation? Please open an issue on the repository's issue tracker.
