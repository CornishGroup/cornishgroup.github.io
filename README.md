# Cornish Labs Website

This is the website of our academic research group at Durham University.

This website is powered by Jekyll with Bootstrap and Bootswatch. It is based on a template from the Allan Lab.

## How to update the website

You can update the website in two ways:

1. Edit and commit files one at a time directly in the repository on GitHub.
2. Preferred: make all changes locally, run the site locally to verify everything, then push one consolidated commit (or one small commit set) to the `gh-pages` branch. More details are below.


## GitHub Actions auto-build/deploy

This repository has a GitHub Actions workflow that automatically builds and deploys the site when changes are pushed to the `gh-pages` branch.

- Trigger: push to `gh-pages` (or manual run from the Actions tab).
- Build step: `bundle exec jekyll build`.
- Deploy step: publishes the generated site to GitHub Pages.

In practice, each push to `gh-pages` automatically rebuilds and republishes the site.

## Local setup

This repository pins Jekyll to version `4.3.2` in `Gemfile`, so install dependencies through Bundler from this repo folder.

### 1. Install Ruby

On Windows, install **Ruby+Devkit** from RubyInstaller:

- https://rubyinstaller.org/

Choose a recent Ruby 3.x build with Devkit, then complete the MSYS2 prompt that appears at the end of install.

### 2. Install Bundler

Open Command Prompt and run:

```bash
gem install bundler
```

### 3. Install this site's gems

From the project root (this folder), run:

```bash
bundle install
```

This installs Jekyll `4.3.2` and the exact supporting gems from `Gemfile.lock`.

### 4. Serve locally

To start the website, in the project root (this folder), run:

```bash
bundle exec jekyll serve
```

Then open:

- http://127.0.0.1:4000/

While `bundle exec jekyll serve` is running, local changes are detected and the site is rebuilt automatically. When you are ready to publish updates, commit your changes and push to GitHub (the `gh-pages` branch).

### If `bundle` is not found

Close and reopen your terminal after installing Ruby/Bundler, then try again.

### If Bundler version mismatch appears

This repo lockfile was generated with Bundler `2.3.7`. If needed, install that version explicitly:

```bash
gem install bundler:2.3.7
```

Copyright Cornish Labs. Code released under the MIT License.

