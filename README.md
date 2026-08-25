# settings

The forms pattern: grouped controls, each bound to a signal, with a
`derive()`-computed summary line.

Concepts demonstrated:

- **`<checkbox label bind-checked>`** - box + caption in one tag;
  clicking anywhere on the row toggles.
- **`<radio group value label>`** - exclusive groups; the selected value
  lives in the signal named by `group` (here `density`). Arrow keys move
  the selection; the group is one Tab stop.
- **`<dropdown bind-value>` + `<option>`** - select widget; `Escape` or
  an outside click dismisses the panel.
- **`<slider min max step bind-value>`** - keyboard-drivable numeric
  input.
- **`derive(name, deps, fn_name)`** - the summary recomputes when any dep
  changes; one declaration replaces seven callbacks. candela references the
  recompute body by function name, and its parameters arrive as the current
  dep values in `deps` order.
- **State pseudo-classes** - `checkbox:checked`, `radio:selected`,
  `:focus` outlines, all in CSS.

Run it:

```sh
lumenc run .
```
