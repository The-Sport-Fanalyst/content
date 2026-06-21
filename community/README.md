# Community board

One file per board post. Frontmatter fields:

| field         | type     | notes |
|---------------|----------|-------|
| title         | string   | Post title |
| type          | enum     | Open Project \| Research Question \| Data Request \| Discussion |
| sport         | string?  | Optional related sport |
| author        | string   | Poster's display name |
| description   | string   | The ask or question |
| skills_needed | string[] | Skills sought (for Open Projects) |
| status        | enum     | Open \| Claimed \| In progress \| Resolved |
| contributors  | string[] | People who joined |
| posted_date   | date     | YYYY-MM-DD |
