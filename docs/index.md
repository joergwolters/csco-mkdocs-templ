# Technical documentation

> *Project documentation with Markdown*

[![PyPI Version][pypi-v-image]][pypi-v-link]
[![Build Status][GHAction-image]][GHAction-link]
[![Coverage Status][codecov-image]][codecov-link]

MkDocs is a static site generator geared towards building project documentation.
Documentation source files are written in Markdown, and configured with a single
YAML configuration file.

Material for MkDocs is packed with many great features for technical writing. This
preconfigured template showcases some of the available specimen that can be used
directly from within Markdown files.

Please see the [Documentation][mkdocs] for an introductory tutorial and a full
user guide. This template uses the [Material for MkDocs][material] extension.

## Links

- [Official MkDocs Documentation][mkdocs]
- [Latest MkDocs Release Notes][release-notes]
- [Official Material for MkDocs documentation][material]
- [Catalog of third-party plugins, themes and recipes][catalog]

## Commands

- `mkdocs new [dir-name]` - Create a new project.
- `mkdocs serve` - Start the live-reloading docs server.
- `mkdocs build` - Build the documentation site.
- `mkdocs -h` - Print help message and exit.

## Project layout

```text
.cache/mkdocs_puml      # Local cache for PlantUML plugin
.github/workflows/
.vscode/
    settings.json       # VS Code configuration file.
.gitignore              # Git ignore configuration file.
.markdownlint.json      # Markdown linter configuration file.
.yamllint               # YAML lint configuration file.
Pipfile                 # Specify package requirements.
Pipfile.lock            # Specify specific package versions,
                        # based on packages present in Pipfile.
README.md               # Template readme file.
mkdocs.yml              # The configuration file.
docs/
    index.md            # The documentation homepage.
    getting-started.md  # Getting started when creating from scratch.
    tags.md             # Tags index page.
docs/about/
    changelog.md        # Change log.
    license.md          # The license stuff.
docs/assets/
    favicon.png         # Material for MkDocs default favicon.
docs/assets/images/
docs/assets/screenshots
docs/css
    extra.css           # Theme color configuration.
includes/
    abbreviations.md    # List of abbreviations in the documentation.
```

## Upgrading

To upgrade MkDocs and Material for MkDocs to the latest version, use pipenv:

```bash
pipenv update mkdocs-material
```

You can determine your currently installed version using `mkdocs --version`:

```bash
$ mkdocs --version
mkdocs, version 1.6.1 from /path/to/mkdocs (Python 3.12)
```

<!-- Badges -->
[codecov-image]: https://codecov.io/github/mkdocs/mkdocs/coverage.svg?branch=master
[codecov-link]: https://codecov.io/github/mkdocs/mkdocs?branch=master
[pypi-v-image]: https://img.shields.io/pypi/v/mkdocs.svg
[pypi-v-link]: https://pypi.org/project/mkdocs/
[GHAction-image]: https://github.com/mkdocs/mkdocs/workflows/CI/badge.svg?branch=master&event=push
[GHAction-link]: https://github.com/mkdocs/mkdocs/actions?query=event%3Apush+branch%3Amaster
<!-- Links -->
[mkdocs]: https://www.mkdocs.org
[material]: https://squidfunk.github.io/mkdocs-material
[release-notes]: https://www.mkdocs.org/about/release-notes/
[catalog]: https://github.com/mkdocs/catalog
