# tex-here

A live LaTeX compilation environment for X11 desktops. `tex-here` launches a
tmux session that watches your `.tex` source files and recompiles on change,
placing the editor, PDF viewer, and compilation output on separate workspaces.
This works best in tiling window manager environments such as xmonad.

## Usage

```
tex-here <document-name> [shell-workspace] [editor-workspace] [pdf-viewer-workspace]
```

Workspace arguments are X11 workspace names (as shown by `wmctrl -d`),
defaulting to `m1` for the shell, `c1` for the editor, and `c2` for the PDF
viewer.

## Scripts

- **tex-here** — main launcher
- Internal helpers: `workspace-name-to-id`, `switch-pid-to-workspace`, `git-progress`

## Dependencies

- `tmux`, `wmctrl`
- `latexmk`
- `ghostscript` (`ps2pdf`)
- A LaTeX distribution (`pdflatex`, etc.)

## License

MIT
