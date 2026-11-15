---

jupyter:
  jupytext:
    text_representation:
      extension: .md
      format_name: markdown
      format_version: '1.3'
      jupytext_version: 1.19.6
  kernelspec:
    display_name: Python 3
    language: python
    name: python3
---

# Keymaps

`<localleader>`: ,
`<leader>`: ñ

## Molten 
Plugin for running code interactively with the jupyter kernel (Renders images, plots, and LaTeX in nvim :D!).

- n + `<localleader>os`: Open Output Window.
- n + `<localleader>oh`: Hide/close the output window.
- n + `<localleader>e`: Evaluate Operator.
- n + `<localleader>rr`: Re-evaluate the current cell.
- v + `<localleader>r`: Execute the selected code.
- n + `<localleader>md`: Delete the current Molten cell.
- n + `<localleader>mx`: Open the output in a browser.

## Quarto (running code)
"An open-source scientific and technical publishing system" (It's useful for running code in .md tbh).

- n + `<localleader>rc`: Run the current cell.
- n + `<localleader>ra`: Run the current cell and all cells above it.
- n + `<localleader>rA`: Run all cells.
- n + `<localleader>rl`: Run the current line.
- v + `<localleader>r`: Run the selected code range.
- n + `<localleader>RA`: Run all cells in all languages.

## Quarto (code navigation and selection)

- n + `<localleader>]c`: Jump to the next code cell.
- n + `<localleader>[c`: Jump to the previous code cell.
- v + `<localleader>ib`: Select inside a code block.
- v + `<localleader>ab`: Select around a code block.

## Quarto LSP (Language Server Protocol)
Autocomplete, go to definition, etc.

- n + `K`: Show hover information.
- n + `gd`: Go to definition.
- n + `<leader>rn`: Rename symbol.
- n + `gr`: Find references.
- n + `<leader>gf` – Format code.

## Hydra
Keymaps! For Quarto! 

n + `<localleader>j` to activate the navigator
- `j`: Move down to the next cell.
- `k`: Move up to the previous cell.
- `r`: Run the current cell.
- `l`: Run the current line.
- `R`: Run the current cell and everything above it.
- `Esc or q`: Exit the navigator.

# Setup

<https://github.com/benlubas/molten-nvim/blob/main/docs/Not-So-Quick-Start-Guide.md>
<https://github.com/benlubas/molten-nvim/blob/main/docs/Notebook-Setup.md>

!! array_to_latex adds a \\ at the end that pnglatex does NOT like..., needs custom function to fix it

!! It's important to change the render markdown because if not it'll break the latex rendered
```{lua}
  { -- DO NOT ERASE IMGS WILL OVERLAP
    "MeanderingProgrammer/render-markdown.nvim",
    opts = {
      code = {
        border = "none",
        style = "normal",
      },
    },
  },
```

