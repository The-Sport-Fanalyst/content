# Projects

One file per project. This is what the Submit form generates. Frontmatter fields:

| field        | type      | notes |
|--------------|-----------|-------|
| title        | string    | Project title |
| creator      | string    | Author's display name |
| sport        | string    | Must match a sport's `name` |
| category     | enum      | Data \| Research \| Models \| Apps |
| description  | string    | One or two sentences |
| status       | enum      | Active \| Seeking collaborators \| In review \| Archived |
| github_url   | string?   | Repository link |
| demo_url     | string?   | Live demo link |
| data_sources | string[]  | Cited sources — required for trust |
| contributors | string[]  | Additional contributor names |
| created_date | date      | YYYY-MM-DD |
| featured     | boolean   | Show on homepage / sport featured row |
| games        | enum[]    | Any of: Summer, Winter, Olympics, Paralympics |

New submissions arrive with `status: In review`; a maintainer changes it on merge.
