# Homebrew Cask Zsh Completions

https://github.com/joshka/brew-cask-zsh-completions

## Deprecation

**Note:** This repo is now deprecated given that these changes were merged into Homebrew
at https://github.com/Homebrew/brew/pull/936.

## Overview

This script is a fork of the Zsh [Homebrew Cask completion plugin](https://github.com/robbyrussell/oh-my-zsh/blob/master/plugins/brew-cask/brew-cask.plugin.zsh)
from Oh My Zsh. It solves the following issues with the original code:

1. Many users use [Prezto](https://github.com/sorin-ionescu/prezto) rather than
Oh My Zsh.
2. The plugin worked by intercepting the brew command rather than the brew
completion calling this completion script. These changes require Homebrew to
merge [brew#407](https://github.com/Homebrew/brew/pull/407) before it will work.
3. It was missing a bunch of completions (mostly options).

## Installation

Symlink or copy the completion script to a directory in your fpath. Homebrew
installs its completions into `$(brew --prefix)/share/zsh/site-functions` which
is in the default fpath for the version of zsh installed by Homebrew.
```shell
$ git clone https://github.com/joshka/brew-cask-zsh-completions.git
$ ln -s brew-cask-zsh-completions/_brew_cask $(brew --prefix)/share/zsh/site-functions
```
