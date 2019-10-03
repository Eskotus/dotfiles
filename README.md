# dotfiles - Setting up a new Mac

## Install brew

´´´
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
´´´

## Clone dotfiles

´´´
git clone https://github.com/Eskotus/dotfiles.git ~/.dotfiles
´´´

## Run bundle

´´´
cd .dotfiles
brew bundle
´´´

## Run RCM

´´´
rcup rcrc
rcup -f
´´´

## Make GNU bash default shell

´´´
echo "/usr/local/bin/bash" | sudo tee -a /etc/shells
chsh -s /usr/local/bin/bash
´´´

## Add a ~/.extra to contain non-github stuff

´´´
# Git credentials
# Not in the repository, to prevent people from accidentally committing under my name
GIT_AUTHOR_NAME="Eero Saikku"
GIT_COMMITTER_NAME="$GIT_AUTHOR_NAME"
git config --global user.name "$GIT_AUTHOR_NAME"
GIT_AUTHOR_EMAIL="???"
GIT_COMMITTER_EMAIL="$GIT_AUTHOR_EMAIL"
git config --global user.email "$GIT_AUTHOR_EMAIL"
git config --global credential.helper osxkeychain
´´´

Dotfiles for sensible OS X life. Heavily influenced by
https://github.com/mathiasbynens/dotfiles.

Instructions copied and altered from [SirIle's blog](http://sirile.github.io/2015/01/26/setting-up-mac.html)
