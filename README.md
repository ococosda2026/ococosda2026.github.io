<!-- omit in toc -->
# O-COCOSDA 2026 Website

The conference website for O-COCOSDA 2026 or the 29th International Conference of Oriental COCOSDA (the International Committee for the Coordination and Standardisation of Speech Databases and Assessment Techniques).

<!-- omit in toc -->
## Table of Contents

- [Built with](#built-with)
- [Getting started](#getting-started)
  - [Install pre-requisites](#install-pre-requisites)
  - [Set up the Ruby version](#set-up-the-ruby-version)
  - [Run the application locally](#run-the-application-locally)
- [Deployment](#deployment)
- [Project structure](#project-structure)

## Built with

- [GitHub Pages](https://docs.github.com/en/pages) turns any GitHub repository into a live website with no separate hosting required.
- [Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll) is a static site generator with built-in support for GitHub Pages.
- [Just the Docs Theme](https://just-the-docs.com/) is modern, high customizable, responsive Jekyll theme for documentation with built-in search.
  - [Just the Docs Template v0.12.0](https://github.com/just-the-docs/just-the-docs-template) is the one-click template to use just-the-docs on GitHub Pages.

## Getting started

### Install pre-requisites

This app requires at least [Ruby 3.4.9](https://www.ruby-lang.org/en/). In order to manage various Ruby versions when working with different projects, we will use `rbenv`. For managing different Ruby dependency gems, we will use `Bundler`.

> If you are using a Windows operating system, it is recommended to use the [Windows Subsystem for Linux (WSL)](https://learn.microsoft.com/en-us/windows/wsl/install). If not, install the required dependencies manually by following their official setup guides.

- [`rbenv`](https://github.com/rbenv/rbenv) allows you to manage multiple installations of Ruby.

    ```shell
    curl -fsSL https://github.com/rbenv/rbenv-installer/raw/HEAD/bin/rbenv-installer | bash
    ```
  
- [`Bundler`](http://bundler.io/) provides a consistent environment for Ruby projects by tracking and installing the exact gems and versions that are needed.
  - Any modern distribution of Ruby comes with Bundler preinstalled by default.

### Set up the Ruby version

After cloning the repository, set up the Ruby version for local development.

1. Install Ruby 3.4.9:

    ```shell
    rbenv install 3.4.9
    ```

2. Automatically set to the appropriate Ruby version upon entering/exiting the root directory:

    ```shell
    rbenv local 3.4.9
    ```

3. Install app dependencies with:

    ```shell
    bundle install
    ```

   If you need to reset the installed dependencies:

    ```shell
    # Delete the bundle cache and Gemlock files
    rm -rf .bundle Gemfile.lock 

    # Then reinstall the app dependencies
    bundle install
    ```

### Run the application locally

Run the app locally with the command below, and visit <http://localhost:4000/> to view the website.

```shell
bundle exec jekyll serve
```

> For more information on how to use the theme, check out the [theme's docs](https://just-the-docs.com/).

## Deployment

Any push to the `main` branch automatically triggers the GitHub Pages deployment workflow. If the workflow completes without errors, changes will be automatically reflected on the live site.

## Project structure

This is the file structure of the project, wherein the indicated files/folders are the important ones we need to keep track of. There are more files/folders that are included by the theme provider.

```text
ococosda2026.github.io
|-- assets/
|-- pages
|-- _config.yml
|-- Gemfile
|-- Gemfile.lock
|-- index.md
```

- `assets/`: Contains the static assets of the website.
- `pages/`: Contains the main static pages of the website.
- [`_config.yml`](_config.yml): Contains the general Jekyll and theme-specific configuration.
- [`Gemfile`](Gemfile): Contains the build system requirements (dependencies).
- [`Gemfile.lock`](Gemfile.lock): A snapshot of the exact versions of the dependencies used (automatically generated via `bundle install`).
- [`index.md`](index.md): Main entry point of the website (home page).
