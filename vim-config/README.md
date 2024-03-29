# Setup on Ubuntu

1. Make symlinks for `~/.vim` and `~/.vimrc`

```
# run from within repo
ln -s `pwd`/.vim ${HOME}/.vim
ln -s `pwd`/.vimrc ${HOME}/.vimrc
```

2. If `coc` is supported, then install `node` >= `12.12` and install [desired extensions](https://github.com/neoclide/coc.nvim/wiki/Install-coc.nvim#install-extensions-for-programming-languages-you-use-daily). Install `coc` extensions using `:CocInstall`, including `coc-git` and `coc-pairs`.

3. Open `vim`, allow `vim-plug` to automatically install, then install plugins using `:PlugInstall`

4. [Install desired patched NERD font](https://github.com/ryanoasis/nerd-fonts#patched-fonts) and set in terminal

5. Install Universal Ctags (used by tagbar)

```
sudo apt install universal-ctags
```

6. [Prevent quotes from being concealed in JSON files](https://github.com/Yggdroot/indentLine/issues/140):

```
$ sudo vi
  :e $VIMRUNTIME/syntax/json.vim
  :g/if has('conceal')/s//& \&\& 0/
  :x!
```
