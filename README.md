# dotvimrc
My .vimrc file

## Deprecation Notice
This repository is no longer maintained in favour of the much easier to setup and maintain [dotfiles](https://github.com/tomwhross/dotfiles) repo, but I am leaving it up as it is still instructive and serves as a bit of history in my journey to get my dotfiles under control. 

## Instructions
My .vimrc starts with a copy of MIT's Missing Semester [.vimrc file](https://missing.csail.mit.edu/2020/files/vimrc).

First download it, then move it to the home directory and rename it from `vimrc` to `.vimrc`, e.g.

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
 
 It's a good idea to add the above to `~/.bash_profile`
 
 Install ack and optionally install rg, or the silver searcher (ag)
  - If rg is available, the `:Ack` command in vim will use it
    - Otherwise it will default to ack
  - Uncomment the ag lines if want to use ag over rg
 
 ```
 $ brew install ack
 $ brew install the_silver_searcher
 $ brew install ripgrep
 ```
 
 Finally, open vim and install the plugins (using vim-plug)
 
 ```
 $ vim
 :PlugInstall
 ```
 
 ### TODOs
 
 - [ ] Install [black for vim](https://black.readthedocs.io/en/stable/editor_integration.html#vim) and configure it to format on save
   - Current requires python3.6+ support which macos does not ship with
   - Also does not work easily inside a virtual environment
 - [ ] Install some sort of jump-to-definition tool
 - [ ] Build a custom [status line](https://shapeshed.com/vim-statuslines/)
 - [x] ~Customize ignore for ag (the silver searcher)~
    - By default it will ignore files in .gitignore
    - If needed, use a .ignore file to ignore files that you don't want git to ignore
    - No longer needed, rg takes care of this
 
