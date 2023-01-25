# macOS for a Linux refugee

## Keyboard

- Keys are in the wrong place (`@~` etc) - [this keymap](http://liyang.hu/osx-british.xhtml) worked best for me; easy to switch between keymaps as-required
- Command vs ctrl is something I got used to; there are keyboard remap utilities if desperately required

## Trackback

- In settings use "Secondary click: Click in Bottom-Right corner"
- Uncheck "Natural scrolling" to get PC-consistent scroll direction
- Turn up scroll speed

## Mouse

- With a Magic Mouse: in settings use "Secondary click: Click Right side"
- Uncheck "Natural scrolling" to get PC-consistent scroll direction
- Turn up pointer speed, possible scroll speed. Most obvious with a Magic Mouse.

## Terminal

- In settings change the default profile (I like "pro")
- Can also change the default shell from zsh to bash but not essential

## VSCode

- People don't seem to use it as an IDE, just a glorified editor
- Probably best avoided

## Vim

- Expect lots of snark and the odd backhanded-compliment `:-(`
- Set some basics (below) in `~/.vimrc` to make it sane
- Use [ALE](https://github.com/dense-analysis/ale) for linting
- Consider [YouCompleteMe](https://github.com/ycm-core/YouCompleteMe) if you want code-completion

```
syn on
set ts=4
set expandtab
```

## Development tools

- The stock python is probably fine
- You'll need to install nodejs; you may wish to `sudo corepack enable` if you want Yarn, but `npm` is probably sufficient
