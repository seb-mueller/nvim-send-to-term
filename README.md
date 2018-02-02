# Neovim plugin to send text from a buffer to a terminal

This plugin aims to be simpler in design and easier to use than other similar
plugins like [neoterm](https://github.com/kassio/neoterm),
[vimcmdline](https://github.com/jalvesaq/vimcmdline),
[vim-slime](https://github.com/jpalardy/vim-slime),
[repl.nvim](https://gitlab.com/HiPhish/repl.nvim), etc. It does not care for
filetypes and REPLs. Instead, you go to an existing terminal and type
`:SendHere`. After that you can use the `s` operator from any buffer to send
text to the terminal. The behaviour of the `s` operator closely matches vim's
built-in `y` or `d` operators.

For multiline text, some REPLs (e.g. IPython) only receive the first line. For
them, try `:SendHere bracketed` in the terminal.

## Provided commands, functions, operators

```vim
:SendHere
:SendHere bracketed
[count]ss
<visual selection>s
s<motion>
S
```

## To do

1. Allow buffers/windows to have different target terminals.
2. Add motions for IPython-style cell-blocks (e.g. send all code between two
   comments), function, indent-level, etc.
3. Fix stuff in IPython: extra newlines, slowdown, etc.
