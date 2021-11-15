# Recipe Book

A collection of my favourite recipes.

## Notes

* Migrated from Gitbook to mdbook.
* `gh-pages` branch serves the Github pages content.
* Run `recipebook` script on local machine to build and push changes merged into master.

```
git checkout gh-pages

git rebase main

mdbook build --dest-dir ./docs

git add .

git ci -m "Building book."

git push -f

git checkout main
```

## TODO:

* CI Integration to run script at Github instead of locally.
