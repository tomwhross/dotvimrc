# dotvimrc
My .vimrc file

## Instructions
My .vimrc starts with a copy of MIT's Missing Semester [.vimrc file](basic vimrc). First download it, then move it to the home directory and rename it from `vimrc` to `.vimrc`

```
$ mv ~/Downloads/vimrc ~/.vimrc
```

Next, install [ctrlp.vim](https://github.com/ctrlpvim/ctrlp.vim)

```
$ mkdir -p ~/.vim/pack/vendor/start
$ cd ~/.vim/pack/vendor/start; git clone https://github.com/ctrlpvim/ctrlp.vim
```

The .vimrc has configurations for the following:
 - To open ctrlp.vim, hit ctrl-p, then start typing
 - Has custom ignores so things like .swp files are ignored
   - Ignores from .gitignore are also enabled

Install [vim-plug](https://github.com/junegunn/vim-plug)

```
$ curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

Install the [Solazized8]() colourscheme

```
$ git clone https://github.com/lifepillar/vim-solarized8.git \
    ~/.vim/pack/themes/opt/solarized8
```

The vimrc is already set up to use the default dark Solarized8 colourscheme.

If the colours look wrong (see the repo for details), do the following:
 - In iTerm2, ensure the terminal colourscheme is set to Solarized dark
 - execute the script Solarized8 ships with:
 
 ```
 $ sh ~/.vim/pack/themes/opt/solarized8/scripts/solarized8.sh
 ```
 
 Install ack and optionally install the silver searcher (ag)
  - If ag is available, the `:Ack` command in vim will use it
    - Otherwise it will default to ack
 
 ```
 $ brew install ack
 $ brew install the_silver_searcher
 ```
 
 Finally, open vim and install the plugins (using vim-plug)
 
 ```
 $ vim
 :PlugInstall
 ```
 
 ### TODOs
 
 - [ ] Install [black for vim])(https://black.readthedocs.io/en/stable/editor_integration.html#vim) and configure it to format on save
  - Current requires python3.6+ support which macos does not ship with
  - Also does not work easily inside a virtual environment
 - [ ] Install some sort of jump-to-definition tool
 
 
 
 
