# CyTRAIL Lab website

Source for [cytrail.github.io](https://cytrail.github.io), the website of CyTRAIL Lab
(Cyber Threat Research and Investigations) at the University of New Haven.

Built with Jekyll from the [academic-website-template](https://github.com/sbryngelson/academic-website-template)
(MIT License). Pushing to `main` rebuilds and deploys the site through GitHub Actions.

## Editing content

- Research projects: `_data/projects.yml` (themes in `_data/themes.yml`)
- News: `_data/news.yml`
- People: `_data/pi.yml`, `_data/team_members.yml`, `_data/alumni.yml`
- Publications: `assets/ref.bib`
- Pages: `_pages/`

## Local preview

    bundle install
    bundle exec jekyll serve
