# dotvimrc
My .vimrc file

## Overview
My .vimrc starts with a copy of MIT's Missing Semester [.vimrc file](basic vimrc). First download it, then move it to the home directory and rename it from `vimrc` to `.vimrc`

```
$ mv ~/Downloads/vimrc ~/.vimrc
```

Next, install [ctrlp.vim](https://github.com/ctrlpvim/ctrlp.vim)

```
$ mkdir -p ~/.vim/pack/vendor/start
```

```
$ cd ~/.vim/pack/vendor/start; git clone https://github.com/ctrlpvim/ctrlp.vim
```

The .vimrc has configurations for the following:
 - To open ctrlp.vim, hit ctrl-p, then start typing
 - Has custom ignores so things like .swp files are ignored
   - Ignores from .gitignore are also enabled
