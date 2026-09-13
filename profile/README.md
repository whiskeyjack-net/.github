# Whiskeyjack

A Tauri-first design system, and the apps built on it.

One web codebase, delivered to the browser, the desktop, and mobile. The design
system is the product here; the apps are how it gets hardened.

## Packages

Published on npm under `@whiskeyjack-net`, MIT licensed.

| Package | What it does |
| --- | --- |
| [`design-system`](https://www.npmjs.com/package/@whiskeyjack-net/design-system) | Thumb-first React components, Metro-style pivot navigation, and a Style Dictionary token pipeline with runtime accent theming. |
| [`tauri`](https://www.npmjs.com/package/@whiskeyjack-net/tauri) | The Tauri app-shell layer: per-platform window controls, OS accent integration, updater UX, and desktop/mobile guards. |
| [`i18n`](https://www.npmjs.com/package/@whiskeyjack-net/i18n) | A react-i18next bootstrap with `<html lang>` / `dir` RTL sync. |
| [`create-whiskeyjack`](https://www.npmjs.com/package/create-whiskeyjack) | Scaffolds a new app with all of the above wired. |

One Rust crate ships beside them, on crates.io:

| Crate | What it does |
| --- | --- |
| [`whiskeyjack-tauri`](https://crates.io/crates/whiskeyjack-tauri) | The backend half of the Tauri layer: the window-control layout a Linux desktop reports, the OS accent colour, and the desktop's own window-button icons. |

## Start here

```bash
npm create whiskeyjack@latest my-app
```

That produces [whiskeyjack-starter](https://github.com/whiskeyjack-net/whiskeyjack-starter):
app shell, theming, i18n, and Tauri window chrome wired from the first commit.

Components are also available one at a time, shadcn-style, so you can take a
piece without adopting the system:

```bash
npx shadcn add https://whiskeyjack.net/r/tab-bar.json
```

Every component and hook ships as readable source through that registry. The
catalog, with live demos you can touch, is at
[whiskeyjack.net/components](https://whiskeyjack.net/components/).

## A worked example

[Icon Stack](https://github.com/whiskeyjack-net/icon-stack) generates a complete
app-icon set for every platform from one source image. It is built on the
published packages and scaffolded from `create-whiskeyjack`, the same way anyone
else would start, which keeps it an honest test of whether the packages work
outside the workshop.

## Status

The packages are in daily use across the apps in this org, from habit trackers
to menu bar utilities, and a handful of apps built on the published packages
live in their own repos here. The 0.x line is managed with changesets, so a
minor version can add API. Interfaces are settling ahead of a 1.0.

More at [whiskeyjack.net](https://whiskeyjack.net).
