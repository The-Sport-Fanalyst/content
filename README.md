# The Sport Fanalyst — Content

This repository holds **all the content** for [The Sport Fanalyst](https://thesportfanalyst.netlify.app):
the Markdown files for sports, projects, community posts, and contributors. It holds
**no application code** — just content — so that:

- contributors open pull requests against clean content, not the app's source;
- content maintainers can be given access to *only* this repo;
- the website reads from here at build time.

The website lives in a separate repository and includes this repo as a git
submodule, so a merge here triggers the site to rebuild with the new content.

## Structure

```
sports/         one Markdown file per sport hub
projects/       one file per project (Data / Research / Models / Apps)
community/      board posts (Open Project / Research Question / Data Request / Discussion)
contributors/   people + their roles
```

Each folder has its own `README.md` describing the fields (frontmatter) that file
type expects. Frontmatter is validated when the site builds — a malformed file
fails the build with a clear message, so nothing broken reaches the live site.

## Contributing

Most people arrive here automatically: the website's **Submit** page formats your
submission and opens a pre-filled pull request against this repo. You just review
and confirm.

To contribute by hand:

1. Add or edit a Markdown file in the right folder (copy an existing one as a model).
2. Open a pull request.
3. A maintainer reviews it here using GitHub's review tools and merges.

Every analysis should show its **sources**, **methodology**, and **author** — that's
the bar for merging.

## Roles

Review and merge rights on this repo map to the platform's Maintainer and Admin
roles. Contributors propose changes via PRs; maintainers approve them.
