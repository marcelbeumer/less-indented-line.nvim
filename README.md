# less-indented-line

Neovim plugin to jump to a less indented ancestor line that matches provided
lua matching pattern. Language agnostic. Helpful to for example jump to
containing object or function.

## Usage

```lua
vim.pack.add({ -- or other plugin manager
  "https://github.com/marcelbeumer/less-indented-line.nvim",
})

-- Example mappings.
vim.keymap.set("n", "gp", function()
  require("less-indented-line").jump("%S")
end, {})
vim.keymap.set("n", "gP", function()
  require("less-indented-line").jump("%s?func%s")
end, {})

```

See [helpfile](./doc/less-indented-line.txt) for more detail.
