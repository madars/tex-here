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
defaulting to `c1` for the shell and editor, and `c2` for the PDF viewer.

## Scripts

- **tex-here** — main launcher
- **latexrun** — vendored copy of [aclements/latexrun](https://github.com/aclements/latexrun) (MIT license) with local patches
- Internal helpers: `workspace-name-to-id`, `switch-pid-to-workspace`, `git-progress`

## Dependencies

- `tmux`, `wmctrl`, `jq`, `evince`
- `inotify-tools` (for `inotifywait`)
- `ghostscript` (for `gs` and `ps2pdf`)
- A LaTeX distribution (`pdflatex`, etc.)
- Python 3 (for `latexrun`)

## License

MIT — see [LICENSE](LICENSE).

`latexrun` is Copyright (c) 2013, 2014 Austin Clements and is also MIT licensed
(see header in the file).
