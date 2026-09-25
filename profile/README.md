# preset.nz

A small, independent software studio in New Zealand, making desktop tools for people who make
things: image processing, mapping, sound, and the odd instrument. Built with agents, finished by
hand. No roadmap promises, just things that ought to exist.

The apps and the writing live at **[preset.nz](https://preset.nz)**. This organisation holds the
parts of them that are worth sharing.

## What you'll find here

The libraries the apps are built on, extracted once a second app needed them. Each one earned its
place by being copied between two codebases first. Browse the
[repositories](https://github.com/orgs/preset-nz/repositories) for what's current; npm packages
publish under the [`@preset.nz`](https://www.npmjs.com/org/preset.nz) scope.

## How the apps are built

**Native apps, not web pages in a window.** The desktop apps use [Tauri](https://tauri.app) and
React, but React is only how the interface gets drawn. The test is whether an app feels at home on
a Mac to someone who never learns what it's made with:

- Every command lives in the menu bar, with its shortcut beside it.
- Fewer buttons, more shortcuts.
- Undo and redo work on everything you do, and a drag is one step.
- Quit and reopen, and the app is where you left it.
- Settings open on <kbd>⌘</kbd><kbd>,</kbd>.

**Schema as data.** Panels, preferences and settings are described as plain data and rendered by
the host. A feature contributes a description; nothing else couples to it.

**Small surfaces.** A library does one job and stays out of the way of the app that uses it.

## Conventions across the packages

- **Ship source, not builds.** npm packages export TypeScript source, and your Vite or `tsc`
  compiles it. No `dist/` unless there's a reason.
- **Peers stay peers.** React, `@tauri-apps/api` and the UI primitives come from your app, not
  from the package. Each README lists what your bundler and Tailwind config need.
- **Pre-1.0 versioning.** A breaking change bumps the minor (`0.1.x` → `0.2.0`); everything else
  is a patch. Pin with `^0.x.y`.
- **Rust and TypeScript in lockstep.** Where a package has both a crate and an npm half, one tag
  covers both and the versions always match.
- **MIT licensed**, everywhere.

## Issues and contributions

Issues are welcome: bug reports, rough edges, questions about the design. These libraries are
shaped by the apps that use them, so a pull request that pulls a package towards a different app's
needs may be declined. Opening an issue first saves everyone the time.

There's no support contract and no SLA. Things get fixed when they get fixed.

---

<sub>Made in Aotearoa New Zealand · [preset.nz](https://preset.nz)</sub>
