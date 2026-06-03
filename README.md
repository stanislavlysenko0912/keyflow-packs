# Keyflow Packs

Community hotkey packs for [Keyflow](https://thelysenko.dev/keyflow).

## Catalog Format

Each catalog entry points to one exported Keyflow profile:

```json
{
  "id": "com.example.App",
  "version": 1,
  "profileSchemaVersion": 1,
  "title": "Example App",
  "summary": "Starter shortcuts for Example App.",
  "category": "productivity",
  "app": {
    "name": "Example App",
    "bundleIdentifier": "com.example.App"
  },
  "path": "packs/example-app.json"
}
```

- `id` is stable and should usually match the app bundle identifier.
- `version` is incremented when the pack content changes.
- `profileSchemaVersion` is the exported Keyflow profile schema used by the pack file.
- `path` is relative to the repository root.
- Pack files use Keyflow's exported JSON profile format.

## Contributing

You can contribute in two ways:

1. Open a pack request issue if you want someone else to create or verify a pack.
2. Open a pull request with a new or updated file in `packs/` and the matching `catalog.json` entry.

## Exporting a Pack from Keyflow

1. Open Keyflow.
2. Go to `Settings`.
3. Find `Cheatsheets` and click `Export`.
4. Choose `JSON`.
5. Select exactly one app profile.
6. Click `Export`.
7. Save the file and add it to `packs/`.

Each pack should contain one app profile. Do not export multiple apps into one file for this catalog.

Before opening a pull request:

- Export the profile from Keyflow as JSON with exactly one selected app.
- Keep one app profile per file.
- Use a lowercase slug file name, for example `packs/example-app.json`.
- Increment the catalog entry `version` when updating an existing pack.
