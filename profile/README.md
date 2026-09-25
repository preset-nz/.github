# preset.nz

A one-person software studio in New Zealand. I make desktop tools for image processing, mapping,
colour and sound, and the odd instrument. There is no flagship and no fixed plan. Each new app
connects to what already exists: a shared library, a file format, a technique borrowed from the app
before it. Built with agents, finished by hand.

The apps and the writing live at **[preset.nz](https://preset.nz)**. This organisation holds the
parts that are worth sharing.

---

## What you'll find here

The libraries the apps are built on, pulled out once a second app needed them. Each was copied
between two codebases before it became a package. Browse the
[repositories](https://github.com/orgs/preset-nz/repositories) for what's current; npm packages
publish under the [`@preset.nz`](https://www.npmjs.com/org/preset.nz) scope.

---

## Rhizome

The studio's full name is rhizomatic preset, after Deleuze and Guattari's rhizome: a root system
with no centre, where any point can connect to any other. Four ideas from it shape the work.

**No centre**
No app sits at the top. Any app can pick up any library here, and the apps pass work to each other
through files and the operating system rather than through each other's internals. One rule holds
the tangle together: a library never depends on an app.

**Maps, not blueprints**
Every project has a written design, and I redraw it when the build shows something new. A feature
that looked small turns out to need its own library; a planned library turns out to be unnecessary.
The map follows the ground.

**Mixed inputs**
Print processes, colour science, cartography, synthesis and language models all feed the same
toolbox. A technique built for one app turns up in the next.

**Growth through connection**
The studio grows by linking what exists, not by getting bigger. The seams between apps get as much
care as the apps: panels, settings and file formats are described as plain data, so a new app plugs
into them instead of rebuilding them.

---

## How the apps behave

The desktop apps are native apps built with [Tauri](https://tauri.app) and React, not web pages in a
window. Every command lives in the menu bar with its shortcut. Undo works on everything you do.
Quit and reopen, and the app is where you left it. Settings open on <kbd>⌘</kbd><kbd>,</kbd>.

---

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

---

## Issues and contributions

Issues are welcome: bug reports, rough edges, questions about the design. These libraries are
shaped by the apps that use them, so a pull request that pulls a package towards a different app's
needs may be declined. Open an issue first and we can talk it through.

There's no support contract and no SLA. Things get fixed when they get fixed.

---

<sub>Made in Aotearoa New Zealand · [preset.nz](https://preset.nz)</sub>
