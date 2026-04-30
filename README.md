<!-- omit in toc -->
# O-COCOSDA 2026 Website

[![Gem Version](https://img.shields.io/gem/v/jekyll-theme-chirpy)][gem]&nbsp;
[![GitHub license](https://img.shields.io/github/license/cotes2020/chirpy-starter.svg?color=blue)][mit]

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
- [Chirpy Jekyll Theme][chirpy] is a minimal, responsive, and feature-rich Jekyll theme for technical writing.
  - [Chirpy Starter v7.5.0](https://github.com/cotes2020/chirpy-starter) is the ready-to-use template for creating websites using the Chirpy Jekyll Theme. This starter bundles those files from the latest Chirpy release along with a [CD][CD] workflow, so you can start writing immediately.

## Getting started

### Install pre-requisites

This app requires at least [Ruby 3.1](https://www.ruby-lang.org/en/). In order to manage various Ruby versions when working with different projects, we will use `rbenv`. For managing different Ruby dependency gems, we will use `Bundler`.

- [`rbenv`](https://github.com/rbenv/rbenv) allows you to manage multiple installations of Ruby.
  - On macOS, Linux, or other UNIX-like operating systems, run the following to install it:

    ```shell
    curl -fsSL https://github.com/rbenv/rbenv-installer/raw/HEAD/bin/rbenv-installer | bash
    ```

  - On Windows, refer to [rbenv for Windows](https://github.com/RubyMetric/rbenv-for-windows)
  
- [`Bundler`](http://bundler.io/) provides a consistent environment for Ruby projects by tracking and installing the exact gems and versions that are needed.
  - Any modern distribution of Ruby comes with Bundler preinstalled by default.

### Set up the Ruby version

After cloning the repository, set up the Ruby version for local development.

1. Install Ruby 3.1.7

    ```shell
    rbenv install 3.1.7
    ```

2. Automatically set the to the appropriate Ruby version upon entering/exiting the root directory:

    ```shell
    rbenv local 3.1.7
    ```

3. Install app dependencies

    ```shell
    bundle install
    ```

   If you need to reset the installed dependencies, delete the bundle cache and Gemlock files, then reinstall the app dependencies

    ```shell
    rm -rf .bundle Gemfile.lock 
    bundle install
    ```

### Run the application locally

Run the app locally with the command below, and visit <http://localhost:4000/> to view the website.

```shell
bundle exec jekyll serve
```

> For more information on how to use the theme, check out the [theme's docs](https://github.com/cotes2020/jekyll-theme-chirpy/wiki).

## Deployment

Any push to the `main` branch automatically triggers the GitHub Pages deployment workflow. If the workflow completes without errors, changes will be automatically reflected on the live site.

## Project structure

This is the file structure of the project, wherein the indicated files/folders are the important ones we need to keep track of. There are more files/folders that are included by the theme provider.

```text
ococosda2026.github.io
|-- _data/
|-- _plugins/
|-- _posts/
|-- _tabs/
|-- assets/
|-- _config.yml
|-- Gemfile
|-- Gemfile.lock
|-- index.html
```

- `_data/`: Contains the YAML configurations for social media-related links. Currently not used and contents are commented out.
- `_plugins/`: Contains the plugins used by the theme.
- `_posts/`: Contains the the blog "post" type of content. Currently not used and empty.
- `_tabs/`: Contains the static page type of content. These automatically appear on the sidebar of the theme.
- `assets/`: Contains the static assets of the website.
- [`_config.yml`](_config.yml): Contains the general Jekyll and theme-specific configuration.
- [`Gemfile`](Gemfile): Contains the build system requirements (dependencies).
- [`Gemfile.lock`](Gemfile.lock): A snapshot of the exact versions of the dependencies used.
- [`index.html`](index.html): Main entry point of the website (home page)

<!-- links -->
[gem]: https://rubygems.org/gems/jekyll-theme-chirpy
[chirpy]: https://github.com/cotes2020/jekyll-theme-chirpy/
[CD]: https://en.wikipedia.org/wiki/Continuous_deployment
[mit]: https://github.com/cotes2020/chirpy-starter/blob/master/LICENSE
