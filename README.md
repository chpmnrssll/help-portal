## GitBook markdown to Jekyll pipeline with Travis-CI

Travis-CI monitors the GitBook content repository for changes. On change, Travis-CI pushes the GitBook content to this repository under the "Build" branch (avoids changing the core Jekyll theme & files). Both this "README.md" and the "SUMMARY.md" files will be overwritten with the ones from GitBook.

Travis-CI monitors this repository as well. Changes trigger a build that generates the static Jekyll site and deploys the final output to the "gh-pages" branch.

All the magic happens in the ".travis.yml" config files. Both repositories must be enabled in the Travis-CI dashboard and a GitHub Personal access token must be setup as an environment variable for each in the Travis-CI dashboard.

Local Jekyll environment setup:
```
$ bundle install
$ bundle exec jekyll serve --livereload
```
