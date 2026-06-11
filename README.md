# StackBlitz SDK VM Demo

Demo of the [@stackblitz/sdk](https://www.npmjs.com/package/@stackblitz/sdk) — embed a live WebContainer editor into any web page and control it programmatically.

## What it does

- **Embed project** — embeds a live StackBlitz editor into the page
- **Open files** — programmatically switches open tabs in the editor
- **Write to files** — injects new content into files via `applyFsDiff()`

## Quick Start

```bash
npm install
npx vite        # or any bundler that supports TypeScript
```

Open `index.html` in a browser (requires a bundler — StackBlitz, Vite, etc.)

## Files

| File | Description |
|---|---|
| `index.ts` | SDK demo logic — embed, openFile, applyFsDiff |
| `index.html` | UI with 3 control buttons |
| `styles.css` | Layout styles |
| `types.d.ts` | CSS module type declaration |

## SDK API Used

```ts
sdk.embedProject(elementId, project, options) → VM
vm.editor.openFile([...files])
vm.getFsSnapshot() → Record<string, string>
vm.applyFsDiff({ create, destroy })
```

## License

MIT © 2026 ivanm696
