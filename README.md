## Avicus XML Documentation

This repository contains the base and generated files from the Avicus XML Documentation site.
Code files are in the `master` branch and generated site files are in the `gh-pages` branch.

### Contributing
Contributing to this site is a bit difficult because most of the pages are generated by Atlas.

To run this site locally, run `bundle exec jekyll serve` and head over to `localhost:4000`

The `examples.xml` file in the `_data` folder is what Atlas uses to generate example blocks for all of the module pages.
Updating this locally and building will have no effect, but feel free to make a pull request to edit and example and a developer can re-build the docs after the approval.

If you find any issues with spelling or a missing feature, please:
- make an issue if it is on a code-generated page
- make a pull request if it is on a human-written page.

### Deployment
Since github pages doesn't support custom plugins, we have to build the site locally before deployment.
To deploy run:
- `bundle exec jekyll build` to build the static files.
- `bundle exec rake deploy:publish` to deploy a snapshot of the static files (in `_site`) to the `gh-pages` branch.
