[![blog-link](https://img.shields.io/badge/ecrivai-blog-blue)](https://ruankie.github.io/ecrivai-blog-hugo/)
[![auto-publish](https://github.com/ruankie/ecrivai-blog-hugo/actions/workflows/sheduled-publish.yml/badge.svg)](https://github.com/ruankie/ecrivai-blog-hugo/actions/workflows/sheduled-publish.yml)
[![GitHub stars](https://img.shields.io/github/stars/ruankie/ecrivai-blog-hugo)](https://github.com/ruankie/ecrivai-blog-hugo/stargazers)
[![GitHub last commit](https://img.shields.io/github/last-commit/ruankie/ecrivai-blog-hugo)](https://github.com/ruankie/ecrivai-blog-hugo/commits/main)

# Overview
This repo contains the code that builds [the static site](https://ruankie.github.io/ecrivai-blog-hugo/) of [EcrivAI's](https://github.com/ruankie/ecrivai) blog posts. The site content is built using [Hugo](https://gohugo.io/) and saved in the `docs/` folder for hosting with GitHub Pages.

# To Update
1. After cloning, get the submodule content (the Hugo theme is contained in a submodule):
    ```bash
    git submodule update --init --recursive
    ```
2. Now you can make your desired changes and build a local version of the site to see how your changes look:
    ```bash
    hugo server -D
    ```
3. Once satisfied, build the site static files:
    ```bash
    hugo -D -d docs
    ```
4. When you're satisfied, commit and push the changes of the main repo and GitHub pages will update the site with the new contents of `docs/`
