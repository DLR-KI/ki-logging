---
title: Testing
hide: navigation
---
<!--
SPDX-FileCopyrightText: 2026 German Aerospace Center (DLR)
SPDX-License-Identifier: CC-BY-4.0
-->

<!-- markdownlint-disable-next-line MD025 -->
# Testing

This projects provides a few different tests and checks.

In general, we have two files which defines all the tests:

- [prek.toml](https://github.com/DLR-KI/ki-logging/blob/main/prek.toml)
- CI pipeline like GitHubs [workflows](https://github.com/DLR-KI/ki-logging/blob/main/.github/workflows/main.yml)

To easily run these tests locally, use:

```bash
./scripts/test.sh
```

If you only want to run the pre-commit hooks manually, use:

```bash
uv run prek run --all-files
```

Static code checks using [ruff](https://docs.astral.sh/ruff):

```bash
# linter
uv run ruff check src
uv run ruff check scripts
# formatter
uv run ruff format --diff src
uv run ruff format --diff scripts
```

To run automatic static code fixes, use:

```bash
# linter
uv run ruff check --fix src
uv run ruff check --fix tests
uv run ruff check --fix scripts
# formatter
uv run ruff format src
uv run ruff format tests
uv run ruff format scripts
```

Static code analysis using [pylint](https://www.pylint.org/):

```bash
uv run pylint --fail-under=6 src
uv run pylint --exit-zero tests
uv run pylint --exit-zero scripts
```

Static type checks using [ty](https://docs.astral.sh/ty/reference/cli/#ty-check):

```bash
uv run ty src
uv run ty tests
uv run ty scripts
```

General typo checking using [typos](https://github.com/crate-ci/typos):

```bash
uv run typos
```

## Bash Script Checks

```bash
find scripts -type f -name "*.sh" -exec uv run shellcheck --external-sources --shell bash --source-path scripts {} +
```

## Markdown Checks

Verify documentation (markdown) compliance w.r.t. [markdown linting rules](https://github.com/DavidAnson/markdownlint#rules--aliases) further specified inside the [.markdownlint-cli2.jsonc](https://github.com/DLR-KI/ki-logging/blob/main/.markdownlint-cli2.jsonc) configuration file.

```bash
npm exec markdownlint-cli2 -- "./docs/**/*.md" "./README.md"
```

## License Checks

```bash
uv run licensecheck
uv run reuse lint
```

## Vulnerability Checks

```bash
uv audit
```
