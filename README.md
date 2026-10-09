# zenfs-core

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/zenfs-core) [![KDE Eco](https://img.shields.io/badge/KDE%20Eco-certified-brightgreen?logo=kde&logoColor=white&style=flat-square)](https://eco.kde.org/) [![Blue Angel](https://img.shields.io/badge/Blue%20Angel-DE--UZ%20215-0055a4?style=flat-square)](https://www.blauer-engel.de/en/certification/criteria)


<!-- AI:start:what-it-does -->
_Description pending._
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
_Architecture documentation pending._
<!-- AI:end:architecture -->

## Install

<!-- Add installation instructions here. This section is yours — the AI will not modify it. -->

```bash
git clone https://github.com/Interested-Deving-1896/zenfs-core.git
cd zenfs-core
```

## Usage


> [!IMPORTANT]
> **[Check out the ZenFS docs!](https://zenfs.dev/start/usage/)**

```js
import { fs } from '@zenfs/core'; // You can also use the default export

fs.writeFileSync('/test.txt', 'You can do this anywhere, including browsers!');

const contents = fs.readFileSync('/test.txt', 'utf-8');
console.log(contents);
```

A single `InMemory` backend is created by default, mounted on `/`. To use different backends, and to
mount more than one, configure ZenFS with `configure`. This mounts a zip file to `/mnt/zip`,
in-memory storage to `/tmp`, and IndexedDB to `/home`:

```js
import { configure, InMemory } from '@zenfs/core';
import { IndexedDB } from '@zenfs/dom';
import { Zip } from '@zenfs/archives';

const res = await fetch('mydata.zip');

await configure({
	mounts: {
		'/mnt/zip': { backend: Zip, data: await res.arrayBuffer() },
		'/tmp': InMemory,
		'/home': IndexedDB,
	},
});
```

The `fs/promises` API is available from `@zenfs/core/promises`, as the `promises` export, or as
`fs.promises`.

For the full usage guide, see **[the documentation](https://zenfs.dev/start/usage/)**.
This includes mounting at runtime, contexts and permissions, devices, and the `node:*`module emulation.

## Configuration

<!-- Document configuration options here. This section is yours — the AI will not modify it. -->

## CI

<!-- AI:start:ci -->
_CI documentation pending._
<!-- AI:end:ci -->

## Mirror chain

<!-- AI:start:mirror-chain -->
This repo is maintained in [`Interested-Deving-1896/zenfs-core`](https://github.com/Interested-Deving-1896/zenfs-core) and mirrored through:

```
Interested-Deving-1896/zenfs-core  ──►  OpenOS-Project-OSP/zenfs-core  ──►  OpenOS-Project-Ecosystem-OOC/zenfs-core
```

Changes flow downstream automatically via the hourly mirror chain in
[`fork-sync-all`](https://github.com/Interested-Deving-1896/fork-sync-all).
Direct commits to OSP or OOC are detected and opened as PRs back to `Interested-Deving-1896`.
<!-- AI:end:mirror-chain -->

## Contributors

<!-- AI:start:contributors -->
| Contributor | Commits |
|---|---|
| [@james-pre](https://github.com/james-pre) | 1654 |
| [@perimosocordiae](https://github.com/perimosocordiae) | 112 |
| [@lavelle](https://github.com/lavelle) | 67 |
| [@mcandeia](https://github.com/mcandeia) | 27 |
| [@bpowers](https://github.com/bpowers) | 26 |
| [@hrj](https://github.com/hrj) | 23 |
| [@emeryberger](https://github.com/emeryberger) | 11 |
| [@terryluan12](https://github.com/terryluan12) | 9 |
| [@billiegoose](https://github.com/billiegoose) | 8 |
| [@yoursunny](https://github.com/yoursunny) | 6 |
| [@corhere](https://github.com/corhere) | 4 |
| [@DustinBrett](https://github.com/DustinBrett) | 4 |
| [@jvilk](https://github.com/jvilk) | 4 |
| [@snowyu](https://github.com/snowyu) | 4 |
| [@uncor3](https://github.com/uncor3) | 3 |
| [@fetsorn](https://github.com/fetsorn) | 3 |
| [@timdream](https://github.com/timdream) | 3 |
| [@Narazaka](https://github.com/Narazaka) | 3 |
| [@kkoreilly](https://github.com/kkoreilly) | 3 |
| [@1j01](https://github.com/1j01) | 3 |
| [@lvcabral](https://github.com/lvcabral) | 2 |
| [@db48x](https://github.com/db48x) | 2 |
| [@lyonbot](https://github.com/lyonbot) | 2 |
| [@atty303](https://github.com/atty303) | 2 |
| [@jcubic](https://github.com/jcubic) | 2 |
| [@DanielRuf](https://github.com/DanielRuf) | 2 |
| [@dreamlayers](https://github.com/dreamlayers) | 2 |
| [@linfaxin](https://github.com/linfaxin) | 1 |
| [@nzinfo](https://github.com/nzinfo) | 1 |
| [@matteo-cristino](https://github.com/matteo-cristino) | 1 |
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_Original project — no upstream influences recorded._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
_No additional resource files found._
<!-- AI:end:resources -->

## Accessibility

<!-- AI:start:accessibility -->
This repo uses automated accessibility auditing via `check-accessibility.yml`.

Checks include: CODEOWNERS ownership coverage, README screen-reader compatibility,
WCAG 2.1 AA HTML compliance, audio overview (espeak-ng), and Braille output (liblouis).




Run the [Check Accessibility](https://github.com/Interested-Deving-1896/zenfs-core/actions/workflows/check-accessibility.yml)
workflow to generate the first report and accessibility artifacts.
See the [W3C Web Content Accessibility Guidelines (WCAG)](https://www.w3.org/WAI/standards-guidelines/wcag/)
for the underlying accessibility reference.
<!-- AI:end:accessibility -->

## License

<!-- AI:start:license -->
[LGPL-3.0](https://github.com/Interested-Deving-1896/zenfs-core/blob/main/LICENSE.md) © 2026 [Interested-Deving-1896](https://github.com/Interested-Deving-1896)
<!-- AI:end:license -->
