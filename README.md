# dev-kit

Daily-use software engineering skills

## Installation

Add the marketplace, then install the plugin:

```bash
claude plugin marketplace add ritvikneu/dev-kit
/plugin install devkit@devkit
```

For local testing:

```bash
claude --plugin-dir /path/to/dev-kit
```

Once installed, skills are namespaced: `/devkit:html-render` and `/devkit:rca`.

## Skills

- **html-render** — Converts any content (markdown, diffs, Jira, code flows, chat) into a self-contained interactive HTML file. Say "make this HTML", "visualize this", or use `/html-render`. Inspired by [The unreasonable effectiveness of HTML](https://thariqs.github.io/html-effectiveness/)
- **rca** — Writes a Root Cause Analysis as an HTML file after a debugging session. Appends updates without overwriting history. Use `/rca` or say "write RCA".

## Contributing

1. Create `skills/<name>/` with `SKILL.md`, `evaluations/`, and optionally `references/`
2. `SKILL.md` needs `name` and `description` frontmatter — the description drives automatic invocation
3. Add at least one evaluation JSON (see `skills/html-render/evaluations/` for the format)
4. For HTML-rendering skills, symlink `references/TEMPLATES.md` from `html-render` instead of duplicating CSS
5. Branch per skill (`skill/<name>`), PR into `main`

---

*html-render 
