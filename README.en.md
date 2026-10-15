# TypeScript Library Starter

[![Buy me a coffee](https://img.shields.io/badge/Buy%20me%20a%20coffee-048754?logo=buymeacoffee)](https://www.lujiahao.com/sponsor)
[![TypeScript](https://img.shields.io/badge/%3C%2F%3E-TypeScript-%230074c1.svg)](https://www.tslang.org)
[![Test](https://img.shields.io/github/actions/workflow/status/ajiho/typescript-library-starter/tests.yml?label=Test&logo=github&style=flat-square&branch=main)](https://github.com/ajiho/typescript-library-starter/actions/workflows/tests.yml)
[![codecov](https://codecov.io/github/ajiho/typescript-library-starter/graph/badge.svg?token=YR846BMB6Y)](https://codecov.io/github/ajiho/typescript-library-starter)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/ajiho/typescript-library-starter/blob/main/LICENSE)

---

English | [简体中文](./README.md)

A modern starter template for TypeScript library development.

Provides a complete toolchain from development, testing, building to publishing out of the box, allowing you to focus on writing high-quality TypeScript libraries without repeatedly setting up basic engineering configurations.

## Integrations

- [Rolldown](https://rolldown.rs/) — High-performance TypeScript bundler
- [Oxlint](https://oxc.rs/docs/guide/usage/linter.html) — Blazingly fast linter
- [Oxfmt](https://oxc.rs/docs/guide/usage/formatter.html) — Blazingly fast formatter
- [Vitest](https://vitest.dev/) — Unit testing & code coverage
- [Codecov](https://about.codecov.io/) — Code coverage reporting & CI analysis platform
- [Size Limit](https://github.com/ai/size-limit) — Bundle size checker
- [Simple Git Hooks](https://github.com/toplenboren/simple-git-hooks) — Lightweight Git hooks
- [releaseasy](https://github.com/releaseasy/releaseasy) — Automated version releases and changelog generation
- [pnpm](https://pnpm.io/) — Fast, disk-space efficient package manager
- [npm-run-all2](https://github.com/bcomnes/npm-run-all2) — Run npm scripts sequentially or in parallel
- [Renovate](https://docs.renovatebot.com/) — Automated dependency updates
- [Publint](https://publint.dev/docs/) — npm package config & publish artifact checking
- [commitlint](https://github.com/conventional-changelog/commitlint) — Validate commit message conventions

## Usage

### Use GitHub Template

It is recommended to click the **Use this template** button at the top right → **Create a new repository** to generate your own TypeScript library.

After creation, clone your new repository and install dependencies:

```bash
git clone https://github.com/YOUR_USERNAME/your-library.git

cd your-library

pnpm install
```

### Manual Clone

You can also clone this template directly:

```bash
git clone https://github.com/ajiho/typescript-library-starter.git your-library

cd your-library

pnpm install
```

Then modify `package.json`, the entry file, and source code to start developing.

## Scripts

| Script            | Description                                                                                                  |
| ----------------- | ------------------------------------------------------------------------------------------------------------ |
| `pnpm format`     | Format code with Oxfmt                                                                                       |
| `pnpm lint`       | Lint code with Oxlint                                                                                        |
| `pnpm lint:fix`   | Automatically fix code issues                                                                                |
| `pnpm typecheck`  | Check types with TypeScript without emitting files                                                           |
| `pnpm test`       | Run tests with Vitest and generate a coverage report                                                         |
| `pnpm test:ui`    | Run tests with Vitest UI enabled                                                                             |
| `pnpm coverage`   | Run tests and generate a coverage report                                                                     |
| `pnpm build`      | Clean, build, and check output size                                                                          |
| `pnpm dev`        | Watch and build code with tsdown                                                                             |
| `pnpm tsdown`     | Build code with tsdown                                                                                       |
| `pnpm size`       | Check build output size                                                                                      |
| `pnpm clean`      | Clean the `dist` directory                                                                                   |
| `pnpm prepare`    | Initialize Simple Git Hooks                                                                                  |
| `pnpm publint`    | Check npm package configuration and published artifacts                                                      |
| `pnpm commitlint` | Validate Git commit messages                                                                                 |
| `pnpm check`      | Run a full check, including linting, type checking, formatting, test coverage, build, and npm package checks |
| `pnpm release`    | Use releaseasy to automate version releases and changelog generation                                         |

### Build Process

`pnpm build` runs the following in sequence:

```text
clean → tsdown → size
```

Where:

- `clean` — Cleans the `dist` directory
- `tsdown` — Builds the TypeScript library with tsdown
- `size` — Checks the build output size

## Credits

This template is inspired by [typescript-library-starter](https://github.com/alexjoverm/typescript-library-starter).
