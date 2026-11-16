# Experience Workspace diagrams

This repository contains architecture and workflow diagrams for the Experience Workspace ecosystem.

## Diagrams

- `ew-architecture-helix6.html` / `ew-architecture-helix6.json` — Experience Workspace architecture on Helix 6 (api.aem.live + Source Bus)
- `ew-architecture-helix5.html` / `ew-architecture-helix5.json` — previous Experience Workspace architecture on Helix 5 (da-admin + S3/R2 + KV)
- `experience-workspace-ecosystem.html` / `experience-workspace-ecosystem.json` — external ecosystem / dependency view
- `ew-ux-workflow.html` / `ew-ux-workflow.json` — Experience Workspace UX workflow diagram

## View in a browser

### GitHub Pages
Recommended for stable links. Pages is already enabled for this repo:

- [Main index](https://mhaack.github.io/ew-docs/)
- [ew-architecture-helix6.html](https://mhaack.github.io/ew-docs/ew-architecture-helix6.html)
- [ew-architecture-helix5.html](https://mhaack.github.io/ew-docs/ew-architecture-helix5.html)
- [experience-workspace-ecosystem.html](https://mhaack.github.io/ew-docs/experience-workspace-ecosystem.html)
- [ew-ux-workflow.html](https://mhaack.github.io/ew-docs/ew-ux-workflow.html)

### Quick preview
You can also render the HTML directly with RawGitHack-style preview URLs:

- `https://raw.githack.com/mhaack/ew-docs/main/ew-architecture-helix6.html`

Replace the filename as needed for the other diagrams.

## Editing

The `.json` files are the [Archify](https://github.com/tt-a1i/archify) sources (Archify 3.2+).
The `.html` files are generated artifacts.

After updating a JSON source, regenerate the matching HTML with Archify:

```bash
node bin/archify.mjs finalize <type> <diagram>.json <diagram>.html --quality showcase --json
```

`<type>` is the source's `diagram_type` (`architecture` or `workflow`).
Delivery receipts (`*.delivery.json`, `*.finalize*.json`, `*.browser-check.json`) and visual-check output are gitignored.
