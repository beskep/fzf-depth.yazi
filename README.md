# fzf-depth.yazi

A modified plugin of the builtin `fzf.lua` that adds search depth control (similar to `fd -d [depth] --no-ignore | fzf`).

## Requirements
- [`fd`](https://github.com/sharkdp/fd)
- [`fzf`](https://github.com/junegunn/fzf)

## Installation
```sh
ya pkg add beskep/fzf-depth
```

## keymap.toml example
```toml
[mgr]
prepend_keymap = [
  { on = ["z", "z"], run = "plugin fzf-depth -- --depth=1", desc = "fzf depth 1" },
  { on = ["z", "2"], run = "plugin fzf-depth -- --depth=2", desc = "fzf depth 2" },
  { on = ["z", "3"], run = "plugin fzf-depth -- --depth=3", desc = "fzf depth 3" },
  { on = ["z", "4"], run = "plugin fzf-depth -- --depth=4", desc = "fzf depth 4" },
  { on = ["z", "`"], run = "plugin fzf", desc = "Jump to a file/directory via fzf" },
  # OR
  # { on = ["z", "`"], run = "plugin fzf-depth -- --depth=0", desc = "Jump to a file/directory via fzf" },
]
```
