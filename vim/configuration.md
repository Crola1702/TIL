# Vim configuration

From [vimrc configuration guide](https://www.freecodecamp.org/news/vimrc-configuration-guide-customize-your-vim-editor/)

`~/.vimrc` saves the configuration for vim editor. It can set default vim flags. Most interesting that are mentioned are:

```
set tabstop=<x>  # Set tab width
set expandtab    # Spaces instead of tabs
set cursorline   # Show line cursor is in, highlighted
set number       # Show line numbers
```

Also, vim supports plugins and the installatin can be easier using plugin managers such as [vim-plug](https://github.com/junegunn/vim-plug).

To install a plugin, write inside `call plug#begin('path')` the plugins using `Plug '<plugin>'` E.g.,:

```
Plug 'dense-analysis/ale'
```

Also, to set colorschemes, you can install the `.vim` files in `~/.vim/colors`, and then apply them via `colorscheme <scheme>` in vimrc

Finally, there is the configuration of status bar. There is more information on how to configure it in [Learn vimscripting the hard way Chapter 17](https://learnvimscriptthehardway.stevelosh.com/chapters/17.html)


