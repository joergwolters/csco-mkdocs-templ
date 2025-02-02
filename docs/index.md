# MkDocs

> *Project documentation with Markdown*

[![PyPI Version][pypi-v-image]][pypi-v-link]
[![Build Status][GHAction-image]][GHAction-link]
[![Coverage Status][codecov-image]][codecov-link]

MkDocs is a **fast**, **simple** and **downright gorgeous** static site
generator that's geared towards building project documentation. Documentation
source files are written in Markdown, and configured with a single YAML
configuration file. It is designed to be easy to use and can be extended with
third-party themes, plugins, and Markdown extensions.

Please see the [Documentation][mkdocs] for an introductory tutorial and a full
user guide. This template uses the [Material for MkDocs][material] theme.

## Links

- [Official Documentation][mkdocs]
- [Latest Release Notes][release-notes]
- [Catalog of third-party plugins, themes and recipes][catalog]

## Commands

- `mkdocs new [dir-name]` - Create a new project.
- `mkdocs serve` - Start the live-reloading docs server.
- `mkdocs build` - Build the documentation site.
- `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml           # The configuration file.
    docs/
        index.md         # The documentation homepage.
        ...              # Other markdown pages, images and other files.
    docs/about/
        changelog.md     # Keep a changelog.
        license.md       # The license stuff.
    docs/css/
        extra.css        # Extra CSS theme configuration.
    includes/
        abbreviations.md # Glossary of all abbreviations.

## Upgrading

To upgrade MkDocs and Material for MkDocs to the latest version, use pip:

    pip install -U mkdocs-material

You can determine your currently installed version using `mkdocs --version`:

    $ mkdocs --version
    mkdocs, version 1.6.1 from /path/to/mkdocs (Python 3.12)

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
