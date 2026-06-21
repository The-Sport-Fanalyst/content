# Sports

One file per sport hub. Frontmatter fields:

| field        | type      | notes |
|--------------|-----------|-------|
| name         | string    | Display name, e.g. "Athletics" |
| slug         | string    | URL slug, e.g. "athletics" |
| icon         | string    | A single glyph/emoji used as the hub icon |
| description  | string    | One or two sentences |
| olympic      | boolean   | Appears in the Olympic programme |
| paralympic   | boolean   | Appears in the Paralympic programme |
| disciplines  | string[]  | List of disciplines/classes |
| la28Venue    | string?   | Optional LA28 venue |
| featured     | boolean   | Show on the homepage |
| order        | number    | Sort order in the directory |

The body (below the frontmatter) is Markdown shown on the sport page.
