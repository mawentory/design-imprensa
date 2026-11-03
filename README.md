# Press — design reference

**Newsprint and double rules**

One page showing every component in this design, rendered from its own design
tokens. No build step, no dependencies: open `index.html`.

**[View the component gallery →](https://mawentory.github.io/design-imprensa/)**

![Press](preview.png)

## What is here

| File | Purpose |
| --- | --- |
| `index.html` | Component gallery — every component on one page |
| `DESIGN.md` | The design notes: origin, palette, type, shape, measured contrast |
| `theme.css` | The 66 design tokens, plus derived accessibility values |
| `design.css` | Component styles, written against tokens only |
| `fonts.css` | `@font-face` declarations for the fonts this design uses |
| `fonts/` | Latin-subset woff2 files, self-hosted |

`design.css` contains no colour, radius or font literal. That is deliberate: the
same stylesheet drives all ten designs and only `theme.css` differs, so the
gallery doubles as a test that the token set is complete.

## The design

Letterpress newspaper: newsprint cream, dense serif text, and the double rule that separates a masthead from the body.

**Type** — Bitter for body text and Playfair Display at 900 for headlines — a genuine editorial pairing rather than one family doing both jobs.

**Shape** — Square-ish geometry, 1px rules, and borders that do the work of boxes. Rules carry structure; shadows do not.

**Signature moves**

- Headlines set in italic Playfair Display at weight 900.
- 4px double rules above section headings.
- Warm paper stock, never pure white.

## Colour

| Token | Value | Role |
| --- | --- | --- |
| `--paper` | `#f4f1e8` | Page ground |
| `--sheet` | `#fbfaf4` | Raised surfaces |
| `--ink` | `#16130f` | Primary text |
| `--signal` | `#b3271e` | Action |
| `--signal-text` | `#b3271e` | Action, when it has to be read |
| `--focus-ring` | `#b3271e` | Focus indicator |

## Accessibility

Every colour pair this design can render as text is checked against WCAG 2.1
when the repo is generated — page surfaces, panel surfaces, and the tinted fills
of badges and diff lines. The full table is in
[DESIGN.md](DESIGN.md#contrast-measured); the gallery is separately audited in a
real browser for heading order, duplicate ids, unlabelled controls and
horizontal overflow at 1280px and 390px.

## Using it

Set the theme attribute on your root element and load the two stylesheets:

```html
<html data-theme="imprensa">
  <link rel="stylesheet" href="fonts.css" />
  <link rel="stylesheet" href="theme.css" />
  <link rel="stylesheet" href="design.css" />
</html>
```

Because the tokens are namespaced by attribute, this theme can sit alongside
another one in the same page.

## The rest of the set

[Placa](https://github.com/mawentory/design-placa), [Blueprint](https://github.com/mawentory/design-blueprint), [Phosphor](https://github.com/mawentory/design-fosforo), [Swiss](https://github.com/mawentory/design-suico), [Neon](https://github.com/mawentory/design-neon), [Brutalist](https://github.com/mawentory/design-brutalista), [Botanical](https://github.com/mawentory/design-botanico), [Bauhaus](https://github.com/mawentory/design-bauhaus), [Vidro](https://github.com/mawentory/design-vidro).

---

Part of the MarvinRouter design set. Generated from a single template; see
`DESIGN.md` for the values behind it.
