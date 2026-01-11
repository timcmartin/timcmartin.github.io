# Recipe Book

A collection of my favourite recipes.

## Notes

- Migrated from Gitbook to mdbook.
- `gh-pages` branch serves the Github pages content.
- This repository is also duplicated under timcmartin.github.io as I don't have
  other content.
- Available at <https://timcmartin.github.io> and
  <https://timcmartin.github.io/recipes>
- After cloning this repo, run `git remote add book git@github.com:timcmartin/timcmartin.github.io.git` as well.
- `recipebook` script should be automatically copied to `~/scripts/recipebook` when cloning dotfiles.
- Run `recipebook` script on local machine to build and push changes merged
  into master.

```bash
git checkout main

git push --force origin

git push --force book

git checkout gh-pages

git rebase main

mdbook build --dest-dir ./docs

git add .

git ci -m "Building book."

git push --force origin

git push --force book

git checkout main
```

## Running Locally

- `mdbook serve`

## Linking Recipes

- Use the following pattern: `{{#include ../mains/meatballs.md}}`

## TODO

- CI Integration to run script at Github instead of locally.
