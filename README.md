# Technical documentation template

> *Technical documentation with Markdown*

[![Built with Material for MkDocs](https://img.shields.io/badge/Material_for_MkDocs-526CFE?style=for-the-badge&logo=MaterialForMkDocs&logoColor=white)](https://squidfunk.github.io/mkdocs-material/)

This repository template provides you with a starting point for setting up Markdown
based documentation. It makes use of features for technical writing provided by
Material for MkDocs including selected integrations with other plugins that are of
specific relevance to technical documentation.

This preconfigured template showcases some of the available specimen that can be
used directly from within Markdown files.

View or build your project documentation using MkDocs as static site generator.

## What is technical documentation

Technical documentation describes the application or solution, purpose, creation
or architecture of a product or service. Its goal is to explain something an
organization offers.

There are several types of technical documents, each intended for a certain audience.
Effectively written documents can help the intended audience by educating them on
necessary details, such as the operation of a product.

It helps to understand what the application or solution is about, how it functions,
and includes feature updates and best practices it has to offer.

Examples of technical documentation include:

- How-to guides
- User guides
- Best practices
- Troubleshoot guides

Some documentations also include use cases and examples to help users understand
how each feature works. They are supported by the read more articles
appendix and images of the solution specifics.

## Using it

This repository is a [template repository], so you can create as many forks of it
as you like. Your new repository will contain only a single commit to start with,
instead of the whole history of the template. Also, you can create a private
repository from this template (while forks inherit the visibility settings from
the original).

The template configuration leans towards Cisco regarding the theme color coding
and the prefilled content of the glossary. Nevertheless, both can be changed easily
to adapt your specific needs.

[template repository]: https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template

Simply hit the `Use this template` button. You can set the specifics of your new
repository from there.

Next, hit the `Clone` button and copy the HTTPS URL of the project.

On your local computer change to the location where you like to store the new
repository. Optionally create a new folder and specify the folder name when cloning
the template repository. Finally, synchronize the single package dependency to ensure
you can make use of MkDocs right from the beginning:

```bash
git clone https://github.com/<git user name>/<repository name>.git <Optional folder>

cd <repository name> # or the optional folder name.

pipenv sync
```

Now you are all set to start your technical documentation.

## Project layout

The following shows the layout of the files in this template. Note that you can
configure Material for MkDocs to use a different layout, this is simply the
template default.

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
