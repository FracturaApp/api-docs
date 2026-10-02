# Fractura developer documentation

The developer portal can be found at [frta.dev/docs](https://frta.dev/docs)

## Structure

- Each folder is a section of the sidebar. The folder name is the section label.
- `order` in the frontmatter sorts the pages. A section uses the smallest `order` of its pages.
- `sidebarTitle` is optional. It replaces `title` in the sidebar.
- Links between pages use `/docs/<file name without .mdx>`. File names must be unique across folders.

## Components

The portal provides these components. Do not import them.

- `<CodeGroup>` shows fenced code blocks as tabs. Use `javascript`, `python`, and `curl` blocks. The selected language applies to all groups.
- `<Endpoint method="POST" path="/channels/:channelId/messages" />` shows one HTTP route.
- `<Note>` and `<Caution>` show callouts. Put a blank line after the opening tag and before the closing tag.


Field tables use `Field | Type | Description` columns. Put `?` after a field name when the field is optional or can be absent (`name?`). Put `?` before a type when the value can be `null` (`?string`). The legend is in `resources/http.mdx` under "Field notation".

## Code examples

- JavaScript examples run on Node.js 22 or later, or Bun.
- Python examples use `asyncio` and `aiohttp`.
- Short examples use the `api` helper from the HTTP API page (`resources/http.mdx`).
