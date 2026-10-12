<!--
SPDX-FileCopyrightText: 2026 German Aerospace Center (DLR)
SPDX-License-Identifier: Apache-2.0
-->

# DLR-KI Logging Module

<!-- [![DOI](https://zenodo.org/badge/770398220.svg)](https://doi.org/10.5281/zenodo.13951179) -->

This repository contains a small Python package designed to simplify the process of enabling consistent logging across multiple projects.
Instead of copying code from one project to another, this package provides a simple, reusable solution.

This repository is a fork of [`fl-logging-base`](https://github.com/DLR-KI/fl-logging-base).
The original repository was archived along with all other federated learning components.
This repository is now maintained independently — all future updates, bug fixes,
and extensions will be published here.

## Get Started

This README.md is primarily intended for developers and contributors, providing necessary information for setup, installation, and contribution guidelines.
If you're interested in using or testing this project, we recommend starting with the [GitHub pages](https://dlr-ki.github.io/ki-logging).
They offer a more user-friendly interface and comprehensive guides to get you started.

## Repository Structure

The repository is organized as follows:

- [docs](docs): Markdown-based user documentation published on the [GitLab Pages](https://dlr-ki.github.io/ki-logging).
- [examples](examples): Logging configuration file examples.
- [LICENSES](LICENSES): All license files used somewhere in this project. Also see [LICENSE.md](LICENSE.md).
- [scripts](scripts): Scripts extending this project.
- [src](src): Project source code.

## Requirements

- Python 3.11 or later
- [uv](https://docs.astral.sh/uv/)

## Install

For developer it is recommended to install all dependency groups.

```bash
uv sync --all-groups
```

## Contribution

Please follow the contribution rules:

- use typed Python (type annotations)
- verify Python static code checks with ruff
- document fixes, enhancements, new features, ...
- write scripts and examples OS independent or at least with linux, wsl support
- verify shell script static code check compliance with [ShellCheck](https://www.shellcheck.net/wiki/)
- verify [REUSE Specification 3.0](https://reuse.software/spec/) compliance for all files
- verify project license compliance without any license conflicts (e.g. for 3rd party libraries, data, models, ...)
- verify documentation (markdown) compliance w.r.t. [markdown linting rules](https://github.com/DavidAnson/markdownlint#rules--aliases) further specified inside the [.markdownlint-cli2.jsonc](.markdownlint-cli2.jsonc) configuration file
- run all tests successfully

### Documentation

This projects is using the Docstring style from
[Google](https://github.com/google/styleguide/blob/gh-pages/pyguide.md#38-comments-and-docstrings).
At least public classes, methods, fields, ... should be documented.

For further documentation we are using [Markdown](https://www.markdownguide.org/) documentation with
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).
See the [docs](docs) folder for more details.

To locally serve the documentation, feel free to use:

```bash
uv run mkdocs serve
```

### Contributors

<a href="https://github.com/HeinrichAD">
  <img
    src="https://images.weserv.nl/?url=avatars.githubusercontent.com/u/5962361?v=4&h=80&w=80&fit=cover&mask=circle&maxage=7d"
    alt="Florian Heinrich"
    title="Florian Heinrich"
  />
</a>
<a href="https://github.com/BeFranke">
  <img
    src="https://images.weserv.nl/?url=avatars.githubusercontent.com/u/31000306?v=4&h=80&w=80&fit=cover&mask=circle&maxage=7d"
    alt="Benedikt Franke"
    title="Benedikt Franke"
  />
</a>

## Citation

For accurate citation, refer to the corresponding metadata in the [CITATION.cff](CITATION.cff) file associated with this work.

## License

Please see the file [LICENSE.md](LICENSE.md) for further information about how the content is licensed.
