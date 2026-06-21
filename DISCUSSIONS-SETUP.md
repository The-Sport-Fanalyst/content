# Community Discussions setup

The website's Community Board is powered by **GitHub Discussions** on this repo.
A one-time setup enables it and creates the categories the site links to.

## 1. Enable Discussions

Repo → **Settings** → scroll to **Features** → check **Discussions**.

## 2. Create the four categories

Go to the **Discussions** tab → the gear/edit icon next to "Categories" →
create (or rename existing) categories so these four exist, named exactly:

| Category name   | Used for                         | Format         |
|-----------------|----------------------------------|----------------|
| Open Projects   | Finding collaborators            | Open-ended     |
| Research        | Research questions               | Open-ended     |
| Data Requests   | Requests for datasets            | Open-ended     |
| General         | General conversation             | Open-ended     |

The site links to these by slug (`open-projects`, `research`, `data-requests`,
`general`). GitHub derives the slug by lowercasing the name and replacing spaces
with hyphens, so the names above produce the expected slugs.

If you name them differently, override the slugs in the **website** via env vars:
`DISC_CAT_OPEN_PROJECTS`, `DISC_CAT_RESEARCH`, `DISC_CAT_DATA_REQUESTS`,
`DISC_CAT_GENERAL`.

## 3. (Optional) Auto-create collaborator discussions

The workflow at `.github/workflows/collaborator-discussions.yml` watches for
projects marked `status: Seeking collaborators` and opens a discussion in
**Open Projects** for each — once per project (it marks each with a hidden
comment to avoid duplicates).

It runs automatically on pushes that touch `projects/`, and you can run it
manually from the **Actions** tab ("Run workflow") to backfill existing projects.

No secrets needed — it uses the built-in `GITHUB_TOKEN`. Just make sure Actions
are enabled (Settings → Actions → General → allow) and that the workflow has
**Read and write permissions** (Settings → Actions → General → Workflow
permissions). The `Open Projects` category must exist first (step 2).

## How the site uses all this

- Board category headers link to each Discussions category.
- "Post an open project / Ask a research question / …" open a pre-filled new
  discussion in the right category.
- A project marked "Seeking collaborators" shows a **Find collaborators** link
  that opens a pre-filled Open Projects discussion — and, with the Action enabled,
  a discussion is also created automatically.
