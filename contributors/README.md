# Contributors

One file per person. Frontmatter fields:

| field           | type   | notes |
|-----------------|--------|-------|
| name            | string | Display name |
| handle          | string | GitHub login (used to match sign-ins) |
| role            | enum   | Admin \| Maintainer \| Contributor \| Member |
| bio             | string | Short bio |
| avatar_initials | string | 2 letters for the avatar |
| github          | string?| GitHub profile URL |
| focus           | string[]| Areas of focus |
| joined          | date   | YYYY-MM-DD |

`handle` must match the person's GitHub login so their signed-in profile links up.
Role here is descriptive; actual permissions are granted via repo access + the
app's role list.
