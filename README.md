# TestPulse Studio — documentation

Source of the TestPulse Studio documentation site (Mintlify project `testpulse-studio`).

## Two kinds of pages

| Pages | Source | Edit here? |
| --- | --- | --- |
| `en/` and `fr/` sub-folders (`getting-started/`, `user-guide/`, `settings/`, `reference/`) and `changelog.mdx` | **Generated** from the in-product help (`packages/extension/src/data/doc-content.ts`) and `docs/CHANGELOG.md` of the TestPulse Studio repository | **No** — fix the help, then regenerate |
| `en/index.mdx`, `en/quickstart.mdx`, `en/security-and-ai.mdx` and their `fr/` twins | Written by hand | Yes, EN and FR together |

## Regenerating at each release

From the TestPulse Studio repository:

```bash
npm run docs:mintlify -- --out <empty folder>
```

Then copy `en/` and `fr/` over this repository, and replace `navigation.languages` in `docs.json` with the content of the generated `navigation.json`, keeping the three hand-written pages at the head of the first group of each language.

## Preview

```bash
npm i -g mint
mint dev
```
