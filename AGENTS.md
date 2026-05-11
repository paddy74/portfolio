# AGENTS.md

Repository instructions for AI coding agents working in this project.

## Project Snapshot

- Name: `paddy74-portfolio`
- Stack: Docusaurus site (TypeScript, MD/MDX, React)
- Package manager: `pnpm` only
- Runtime: Node.js `>=20.0`
- Linters: TypeScript, Stylelint, markdownlint
- Formatters: Prettier, GitHub Flavored Markdown

## Workspace Layout

- `website/src/`: React pages/components and CSS modules
- `website/docusaurus.config.ts`: site/plugin behavior and build constraints
- `website/docs/`: handbook/documentation content
- `website/blog/`: blog posts
- `website/portfolio/`: portfolio docs plugin content

## Runbook (from `website/`)

```bash
pnpm install
pnpm typecheck
pnpm lintfix
pnpm format
pnpm build
```

Notes:

- There is no dedicated `test` script in `website/package.json`.
- `pnpm lint` and `pnpm lintfix` run ESLint and stylelint.

## High-Value Conventions

- Use relative Markdown file links with `.md`/`.mdx` extensions for internal docs.
- Keep heading hierarchy strict (`h1 -> h2 -> h3`, no skipped levels).
- Use single spaces between words and avoid trailing spaces.
- Use `draft: true` to exclude content from production builds.
- Use `unlisted: true` to keep content published but undiscoverable.
- Build can fail on broken links because `onBrokenLinks` is set to `throw`.

## Agent Behavior

- Extend existing files/components before creating new structures.
- Keep changes scoped; avoid drive-by refactors.
- Prefer citing canonical documentation instead of duplicating rule text.
- For document/content edits, validate links and frontmatter in changed files.

## Canonical References

- Markdown/style rules: [website/docs/about/develop/markdown-styleguide.md](website/docs/about/develop/markdown-styleguide.md)
- Handbook editing workflow: [website/docs/about/editing.md](website/docs/about/editing.md)
- Practical editing tips: [website/docs/about/editing-tips.md](website/docs/about/editing-tips.md)
- Style guide index: [website/docs/about/style-guide.md](website/docs/about/style-guide.md)
- Site config and content plugins: [website/docusaurus.config.ts](website/docusaurus.config.ts)
- Development setup and command baseline: [README.md](README.md)
