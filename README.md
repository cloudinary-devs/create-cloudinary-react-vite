# create-cloudinary-react-vite

> **Beta Release** - This is a beta version. We welcome feedback and bug reports!

Part of the [Cloudinary Developers](https://github.com/cloudinary-devs) organization.

Scaffold a Cloudinary React + Vite + TypeScript project with interactive setup.

## Usage

```bash
npx create-cloudinary-react-vite
```

The CLI will prompt you for:
- Project name
- Cloudinary cloud name
- Upload preset (optional)
- AI coding assistant(s) you're using (Cursor, GitHub Copilot, Claude, etc.)
- Whether to install dependencies
- Whether to start dev server

## Features

- ✅ Interactive setup with validation
- ✅ Pre-configured Cloudinary React SDK
- ✅ TypeScript + Vite + React 19
- ✅ Typed Upload Widget component
- ✅ Environment variables with VITE_ prefix
- ✅ Multi-tool AI assistant support (Cursor, GitHub Copilot, Claude, and more)
- ✅ MCP configuration for Cloudinary integration
- ✅ ESLint + TypeScript configured

## AI Assistant Support

During setup, you'll be asked which AI coding assistant(s) you're using. The CLI will generate the appropriate configuration files:

- ✅ **Cursor** → `.cursorrules` + `.cursor/mcp.json` (if selected)
- ✅ **GitHub Copilot** → `.github/copilot-instructions.md`
- ✅ **Claude Code / Claude Desktop** → `.claude`, `claude.md` + `.cursor/mcp.json` (if selected)
- ✅ **Generic AI tools** → `AI_INSTRUCTIONS.md`, `PROMPT.md`

**MCP Configuration**: The `.cursor/mcp.json` file is automatically generated if you select Cursor or Claude, as it works with both tools.

These rules help AI assistants understand Cloudinary React SDK patterns, common errors, and best practices. The generated app also includes an "AI Prompts" section with ready-to-use suggestions for your AI assistant.

## Development

This project uses [Conventional Commits](https://www.conventionalcommits.org/) for version management.

### Commit Format

```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `refactor`: Code refactoring
- `perf`: Performance improvements
- `chore`: Other changes

### Version Management

This project uses [release-please](https://github.com/googleapis/release-please) for automated version management.

```bash
# Install dependencies (includes husky setup)
npm install

# Update release-please manifest (analyzes commits and updates manifest)
npm run release

# Create release PR (creates PR with version bump and changelog)
npm run release:pr
```

**How it works:**
1. Make commits with conventional format (`feat:`, `fix:`, etc.)
2. Run `npm run release` to update the manifest based on commits
3. Run `npm run release:pr` to create a release PR
4. Merge the PR to create the release tag

**Version bumps are automatic based on commit types:**
- `feat:` → minor version (1.0.0 → 1.1.0)
- `fix:` → patch version (1.0.0 → 1.0.1)
- `BREAKING CHANGE:` or `feat!:` → major version (1.0.0 → 2.0.0)

**Note:** 
- Update the `repo-url` in `package.json` scripts with your actual GitHub repo
- For beta releases, you can manually edit the version in the manifest or PR
- Alternatively, use `npm version` commands for manual versioning
