# Ben's Dotfiles

In this repository you'll find my dotfiles. I don't expect anyone to actually use these directly (they are here more for reference than anything), but if you do, here's how you set it up.  Keep in mind that I am not liable for any damage you do to your computer or files if you use these files.

## Prerequisites

- Some version of ruby
- `rake` and the `colored` gems installed locally
- vim
- zsh and oh-my-zsh

## Installing dependencies

Run `./install_dependencies` to install any brew packages that are used by these files.

Currently these are:
* [neovim](https://github.com/dandavison/delta)
* [git-delta](https://github.com/dandavison/delta)

## Symlinking these files

Clone the directory somewhere (I chose `~/Dropbox/dotfiles` so it would be easily synced across my machines).

```
git clone https://github.com/subdigital/dotfiles.git
```

Then we need to symlink these into your home directory. Run:

```
rake symlink
```

This will symlink all of the dotfiles from the repo into your home folder.  It will prompt before overwriting files, so you
can skip existing ones if you want.

> I highly recommend you back up any existing dotfiles before trying this out.  Use at your own risk.


## Vim notes

* `/usr/local/bin/vim` will be symlinked to `nvim`.
* Vim-Plug is used to install plugins. Submodules have been removed.

> Vim writes back-up and temp files to [`~/.vim/`](https://github.com/subdigital/dotfiles/blob/master/.vimrc#L163-L164). If you encounter the error `E303: Unable to open swap file`, you might have to create those directories from the command line to fix the error: `mkdir ~/.vim/_backup/ && mkdir ~/.vim/_temp/`.


