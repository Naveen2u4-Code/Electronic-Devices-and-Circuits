# Electronic Devices & Circuits

An animated, free-to-use lesson series on **Electronic Devices and Circuits**, by **Naveen Bokka**.

Each topic pairs a short animation with concise notes and key formulas, covering
semiconductor physics through diodes, transistors, amplifiers and oscillators.

## Units

1. Semiconductor Fundamentals
2. PN Junction Diode
3. Special Purpose Diodes
4. Rectifiers and Filters
5. BJT
6. Transistor Biasing and Stabilization
7. Small Signal BJT Analysis
8. Field Effect Transistors
9. Special Devices
10. Feedback Amplifiers and Oscillators

## Project structure

```
index.html              Home page with the unit grid
unit-1/index.html       Unit 1 topic list
unit-1/<slug>/index.html  Individual topic pages (added as they are built)
```

The site is plain HTML, CSS and JavaScript: no frameworks, no build step, no npm.
Every page carries its own inline styles and uses only relative links, so it works
on GitHub Pages (served from the `main` branch root) and straight from disk.

### Marking content as published

- **Units:** in `index.html`, add the unit number to the `builtUnits` array.
- **Topics:** in `unit-1/index.html`, add the topic slug (e.g. `"1-1-what-is-a-semiconductor"`)
  to the `builtTopics` array at the top of the file once `unit-1/<slug>/index.html` exists.

Anything not listed shows as "Coming soon".

## Viewing locally

The simplest option is to open `index.html` in a browser by double-clicking it.

To view it the way GitHub Pages serves it, run a local static server from the repo root:

```sh
# Python 3
python -m http.server 8000
```

Then open <http://localhost:8000/>.

## Design system

| Token       | Value     | Use                     |
|-------------|-----------|-------------------------|
| Background  | `#0f1420` | Page background         |
| Panel       | `#1a2132` | Cards and panels        |
| Text        | `#e6e9ef` | Body text               |
| Muted       | `#9aa4b8` | Secondary text          |
| Electron    | `#4fc3f7` | Electrons, links, accent |
| Hole        | `#ff8a65` | Holes                   |
| Energy      | `#ffd54f` | Energy                  |
| Success     | `#81c784` | Published / success     |

Fonts: **Inter** for text and **JetBrains Mono** for code and formulas, both from Google Fonts.

Animation source files (`.blend`) and rendered video (`.mp4`, `.mov`, `renders/`) are
kept out of the repository via `.gitignore`.

## License

© 2026 Naveen Bokka. Built with open-source tools.
