# Vi
## Installing with ruby and python support
Tip found via <http://iamnearlythere.com/installing-vim-python-ruby-support-homebrew>

- The standard Macosx vi, does NOT have support for ruby and python.
- Simplest way to install is via homebrew
- Homebrew does not include vim by default
- You can use a formula from [Homebrew-Alt](https://github.com/adamv/homebrew-alt/blob/master/duplicates/vim.rb)

        $ brew install mercurial
        $ brew install https://raw.github.com/adamv/homebrew-alt/master/duplicates/vim.rb

## 256 color terminal support
Tip found via <http://kevin.colyar.net/2011/01/pretty-vim-color-schemes-in-iterm2/>

* The standard Macosx Terminal does not support 256 color schemes
* You can make this work by installing [Iterm2](http://www.iterm2.com/#/section/home)
* This also has awesome support like:
 * Alt-Enter :full screen
 * Alt-(Arrows) : navigate tabs
 * Alt-Command-E : expose
* Change in preferences (xterm to xterm-256)
* Install dessert color scheme: <https://github.com/mbadolato/iTerm2-Color-Schemes>

## Plugins

# Finder
## Solid dark background color
Tip found at <http://www.slashdotdash.net/2006/12/19/mac-os-x-desktop-black-background-wallpaper/>

- Standard finder desktop , has no black/dark solid color background
- Copy a file in `/Library/Desktop Pictures/Solid Colors/` and change it's color

# Brew
## Installation
Just find the latest at <https://github.com/mxcl/homebrew/wiki/installation>
<http://mxcl.github.com/homebrew/>

# Bash
## install profile
    ln -s `pwd`/dot-bash_profile $HOME/.bash_profile
## Activate autocompletion in bash

    $ brew install bash-completion

Add to your .bash_profile:

    if [ -f `brew --prefix`/etc/bash_completion ]; then
      . `brew --prefix`/etc/bash_completion
    fi

## Add ls colors
Tip found at <http://www.napolitopia.com/2010/03/lscolors-in-osx-snow-leopard-for-dummies/>

    export LS_OPTIONS='--color=auto'
    export CLICOLOR='Yes'
    export LSCOLORS=''

## Display rvm , git in prompt
Tip found at - <http://collectiveidea.com/blog/archives/2011/08/02/command-line-feedback-from-rvm-and-git/>
# Git
## Use the files
    ln -s `pwd`/dot-gitconfig $HOME/.gitconfig
## Enable color in git in terminal
Tip found at <http://stackoverflow.com/questions/1156069/how-to-configure-term-on-mac-os-x-with-color>

    $ git config --global color.ui true

## Pretty log listing
in alias section of .gitconfig

    ll = log --all --graph --oneline --date-order --format='%C(yellow)%h%Creset %C(green)(%cr)%Creset %C(red)%d%Creset %an - %    s'
