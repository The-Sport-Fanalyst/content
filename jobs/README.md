# Jobs

Data, analytics, and research roles in sport. These power `/jobs` on the site and
the "Jobs in sport data" section on the homepage.

## Adding a role

Create a markdown file here, e.g. `2026-08-analytics-engineer-example.md`:

```markdown
---
title: "Analytics Engineer"
company: "Example Sports Tech"
url: "https://example.com/careers/analytics-engineer"   # the original posting
location: "Boulder, CO"
remote: false
category: "Data Engineering"      # Data Science | Data Engineering | Analytics |
                                  # Research | Business Intelligence | Other
org_type: "Sports tech"           # League | Team | Governing body | Sports tech |
                                  # Media | Academic | Other
employment_type: "Full-time"      # Full-time | Part-time | Contract | Internship
sport: "Athletics"                # optional
summary: "Build the pipelines behind their athlete dashboards."  # optional, ONE line
posted_date: 2026-08-01
closes: 2026-09-15                # REQUIRED — the listing disappears after this
---
```

Nothing goes below the `---`.

## The easy way: use the form

Go to **/jobs/submit** on the site. It asks for each field, shows a live preview
of the file, and opens a pre-filled pull request on GitHub for you. No YAML by
hand, and it won't let you submit without a closing date.

## Two rules that matter

1. **`closes` is required.** Listings past their closing date disappear from the
   site automatically — that's what stops the board filling up with dead links.
   If the posting doesn't state a date, pick a sensible one; it can be extended
   by editing the file.

2. **Don't paste the job description.** Write your own one-line `summary`, or
   leave it out. The full description is the employer's copyrighted text, and
   every card links to the original posting anyway.

## Note for maintainers

Because `closes` is required, a job file without it will fail the site build with
a message naming the file. Check the field is present before merging. (A failed
build doesn't take the site down — Netlify keeps serving the last good deploy —
but the site won't update until it's fixed.)
