---
tags:
  - MkDocs
  - brew
  - pipenv
---

# Getting Started

Introduction to install Material for MkDocs on Mac and set up the integration
to GitHub pages.

---

## Visual Studio Code on macOS

Follow the setup guide for [Visual Studio Code on macOS][vscode] to install VS Code.

## Material for MkDocs installation on macOS

1. Install brew

    Follow the installation instruction on [Homebrew] to install brew.

    Verify the installation was successful:

    ```bash
    $ brew --version
    Homebrew 4.4.19
    ```

2. Install python3

    ```bash
    brew install python3
    ```

3. Upgrade pip

    ```bash
    pip3 install --upgrade pip
    ```

4. Install pipenv

    ```bash
    pip install pipenv --user
    ```

5. Create project folder

    ```bash
    mkdir newfolder && cd $_
    ```

6. Install Material for MkDocs

    ```bash
    pipenv install material-mkdocs
    ```

## Creating a new project

Getting started is super easy. To create a new documentation within the project folder,
run the following command from the command line:

```bash
mkdocs new .
```

Take a moment to review the initial documentation project.

There's a single configuration file named `mkdocs.yml`, and a folder named
`docs` that will contain your documentation source files (`docs` is
the default value for the [docs_dir] configuration setting). Right now the `docs`
folder just contains a single documentation page, named `index.md`.

MkDocs comes with a built-in dev-server that lets you preview your documentation
as you work on it. Make sure you're in the same directory as the `mkdocs.yml`
configuration file, and then start the server by running the `mkdocs serve`
command:

```console
$ mkdocs serve
INFO    -  Building documentation...
INFO    -  Cleaning site directory
INFO    -  Documentation built in 0.22 seconds
INFO    -  [15:50:43] Watching paths for changes: 'docs', 'mkdocs.yml'
INFO    -  [15:50:43] Serving on http://127.0.0.1:8000/
```

Open up <http://127.0.0.1:8000/> in your browser, and you'll see the default
home page being displayed:

The dev-server also supports auto-reloading, and will rebuild your documentation
whenever anything in the configuration file, documentation directory, or theme
directory changes.

Open the `docs/index.md` document in your text editor of choice, change the
initial heading to `My-Project-Documentation`, and save your changes.
Your browser will auto-reload and you should see your updated documentation immediately.

Now try editing the configuration file: `mkdocs.yml`. Change the
[`site_name`][site_name] setting to `Solution_Documentation` and save the file.

```yaml
site_name: Solution Documenation
```

Your browser should immediately reload, and you'll see your new site name take
effect.

!!! Note
    The [`site_name`][site_name] configuration option is the only required option
    in your configuration file.

## Adding pages

Now add a second page to your documentation. Structure the documentation using
nested directories if that better suits your documentation layout:

```bash
mkdir docs/about

touch docs/about/changelog.md
```

As our documentation site will include some navigation headers, you may want to
edit the configuration file and add some information about the order, title, and
nesting of each page in the navigation header by adding a [`nav`][nav]
setting:

```yaml
site_name: Solution Documentation
nav:
  - Home: index.md
  - About: 
    - Change Log: about/changelog.md
```

Save your changes and you'll now see a navigation bar with `Home` and `About`
items on the left as well as `Search` item on the right.

Try the menu items and navigate back and forth between pages. Then click on
`Search`. A search dialog will appear, allowing you to search for any text on
any page. Notice that the search results include every occurrence of the search
term on the site and links directly to the section of the page in which the
search term appears. You get all of that with no effort or configuration on your
part!

## Theming our documentation

Now change the configuration file to alter how the documentation is displayed by
changing the theme. Edit the `mkdocs.yml` file and add a [`theme`][theme] setting:

```yaml
site_name: Solution Documentation
nav:
  - Home: index.md
  - About: 
    - Change Log: about/changelog.md
theme:
  name: material
```

Save your changes, and you'll see the Material for MkDocs theme is being used.

## Changing the Favicon Icon

By default, Material for MkDocs uses the [Material for MkDocs favicon] icon.
To use a different icon, create an `assets` subdirectory in the `docs` directory
and copy your custom `favicon.ico` or `favicon.png` file to that directory.
MkDocs will automatically detect and use that file as your favicon icon.

[Material for MkDocs favicon]: assets/favicon.png

## Building the site

That's looking good. You're ready to deploy the first pass of your
`Solution Documentation`. First build the documentation:

```bash
mkdocs build
```

This will create a new directory, named `site`. Take a look inside the
directory:

```console
$ ls site
404.html assets getting-started search      sitemap.xml.gz
about    css    index.html      sitemap.xml tags
```

Notice that your source documentation has been output as two HTML files named
`index.html` and `about/changelog/index.html`. You also have various other media
that's been copied into the `site` directory as part of the documentation theme.
You even have a `sitemap.xml` file and `search/search_index.json`.

If you're using source code control such as `git` you probably don't want to
check your documentation builds into the repository. Add a line containing
`site/` to your `.gitignore` file.

```bash
echo "site/" >> .gitignore
```

If you're using another source code control tool you'll want to check its
documentation on how to ignore specific directories.

## Other Commands and Options

There are various other commands and options available. For a complete list of
commands, use the `--help` flag:

```bash
mkdocs --help
```

To view a list of options available on a given command, use the `--help` flag
with that command. For example, to get a list of all options available for the
`build` command run the following:

```bash
mkdocs build --help
```

## Deploying

The documentation site that you just built only uses static files so you'll be
able to host it from pretty much anywhere. Simply upload the contents of the
entire `site` directory to wherever you're hosting your website from and
you're done. For specific instructions on a number of common hosts, see the
[Deploying your Docs][deploy] page.

## Getting help

See the [User Guide] for more complete documentation of all of Material for MkDocs'
features.

To get help with Material for MkDocs, please use the [GitHub discussions] or
[GitHub issues].

<!-- Links -->
[docs_dir]: https://www.mkdocs.org/user-guide/configuration/#docs_dir
[deploy]: https://www.mkdocs.org/user-guide/deploying-your-docs/
[nav]: https://www.mkdocs.org/user-guide/configuration/#nav
[GitHub discussions]: https://github.com/squidfunk/mkdocs-material/discussions
[GitHub issues]: https://github.com/squidfunk/mkdocs-material/issues
[site_name]: https://www.mkdocs.org/user-guide/configuration/#site_name
[theme]: https://www.mkdocs.org/user-guide/configuration/#theme
[User Guide]: https://squidfunk.github.io/mkdocs-material/getting-started/
[vscode]: https://code.visualstudio.com/docs/setup/mac
[Homebrew]: https://brew.sh
