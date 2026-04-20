# Contributing

Thank you for your interest in contributing to the MT-Syntax project. This document outlines the guidelines and best practices for contributing to our syntax highlighting repositories. By following these guidelines, you help maintain a clean and consistent codebase for everyone.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Enhancements](#suggesting-enhancements)
  - [Your First Code Contribution](#your-first-code-contribution)
  - [Pull Requests](#pull-requests)
- [Style Guide](#style-guide)
  - [Commit Messages](#commit-messages)
  - [File Formatting](#file-formatting)
- [License](#license)

## Code of Conduct

This project and everyone participating in it is governed by the [MT-Syntax Code of Conduct](./CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to the project maintainers.

## How Can I Contribute?

### Reporting Bugs

If you encounter a bug or an incorrectly highlighted token in a syntax file, please [open an issue](https://github.com/MT-Syntax/makefile/issues/new) and include the following information:

- **A descriptive title** that summarizes the issue.
- **Steps to reproduce** the problem.
- **Expected behavior** vs. **actual behavior**.
- **A code snippet** that demonstrates the issue.
- **Your MT Manager version** and device information (if relevant).

### Suggesting Enhancements

We welcome suggestions for new language support, additional keywords, or color scheme improvements. When proposing an enhancement, please provide:

- A clear explanation of the proposed change.
- Examples of how the change would improve the highlighting.
- References to official language specifications, if applicable.

### Your First Code Contribution

Unsure where to begin? Look for issues labeled `good first issue` or `help wanted`. These are specifically curated for new contributors.

### Pull Requests

1. **Fork** the repository and create your branch from `main`.
2. **Make your changes** following the [Style Guide](#style-guide).
3. **Test your changes** in MT Manager to ensure the highlighting works as expected.
4. **Commit your changes** using the [Commit Message](#commit-messages) conventions.
5. **Push** your branch to your fork.
6. **Open a Pull Request** against the `main` branch of the original repository.

In your Pull Request description, please explain:

- What problem does this change solve?
- What files were modified and why?
- Any screenshots or comparisons showing the improvement (optional but encouraged).

## Style Guide

### Commit Messages

We follow the [Conventional Commits](https://www.conventionalcommits.org/) specification to maintain a clear and machine-readable commit history. Each commit message should be structured as follows:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

**Allowed Types:**

| Type | Description |
|:-----|:------------|
| `feat` | A new feature (e.g., adding support for a new language keyword). |
| `fix` | A bug fix (e.g., correcting a regex pattern that was not matching correctly). |
| `docs` | Documentation only changes (e.g., updating README.md). |
| `style` | Changes that do not affect the meaning of the code (e.g., whitespace, formatting, missing semi-colons). |
| `refactor` | A code change that neither fixes a bug nor adds a feature (e.g., simplifying a regex). |
| `perf` | A code change that improves performance (e.g., optimizing a complex pattern). |
| `chore` | Other changes that don't modify `src` or `test` files (e.g., updating `.gitignore`, dependencies). |

**Examples:**

- `feat: add support for fish builtin 'argparse'`
- `fix(makefile): correct pattern for automatic variable $<`
- `docs: update installation instructions in README`
- `chore: add .editorconfig file`

**Breaking Changes:** If your change introduces a breaking change (e.g., renaming a style that others may have customized), append a `!` after the type/scope and include a `BREAKING CHANGE:` footer. Example:

```
feat!: remove deprecated 'old_style' from Makefile syntax

BREAKING CHANGE: The 'old_style' style has been removed. Any custom themes relying on it must be updated.
```

### File Formatting

- Use **2 spaces** for indentation.
- Place a single space after colons in object definitions (e.g., `name: ["Makefile"]`).
- Keep regex patterns as readable as possible; use named `defines` for complex or repeated patterns.
- Follow the existing structure of `.mtsx` files (e.g., order of `styles`, `defines`, `contains`).

## License

By contributing to this project, you agree that your contributions will be licensed under the same [MIT License](./LICENSE) that covers the project. You retain the copyright to your contributions but grant the project a perpetual, worldwide, non-exclusive, royalty-free license to use them.

---

Thank you for helping make MT-Syntax better for everyone.
