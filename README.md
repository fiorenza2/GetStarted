# General Hints and Tips to Configure Stuff

This is a list for my own use to figure out how to set things up when I use a new computer, because knowing me I'll forget most of the cool stuff I've picked up along the way

## Python

Anaconda as always

Make a new environment 
```bash
conda env -n ENVNAME -python=3.6
```

## WSL

Use [WSLtty](https://github.com/mintty/wsltty)

This doesn't support stuff like tabbing, but has other neat features like powerline fonts and is themeable. It's also really lightweight and is apparently more customisable.

[This](https://dev.to/winebaths/getting-up-and-running-with-the-windows-subsystem-for-linux-8oc) is a general handy guide.

NB: Enable 'Ctrl+Shift+' Commands in the preference to make copy and pasting from the clipboard a lot less painful

## Bash

Use aliases:

```bash
alias sublime="/mnt/c/Program\ Files/Sublime\ Text\ 3/sublime_text.exe ."
```

## vim

Some neat shortcuts:

|Command    | Outcome                       | Mode      |
|---        |---                            |---:        |
| Esc       | Get back into 'Command' mode    | Insert    |
| i         | Get into 'Insert' mode to actual make edits| Command | 
| u         | Undo                          | Command   |
| Ctrl-r    | Redo                          | Command   |
|dd         | Delete the line               | Command |
| PgDown/PgUp| Quick traversal              | Command |
| 0         |Move cursor to the beginning of the line|Command | 
| /text2search| Search for text (forward)     | Command |
| n         | Next instance of word         | Search    |
| N         | Previous instance of word     | Search    |
| :wq       | Quit and save                 | Command |
| :q!       | Quit without saving           | Command | 

More help is [here](https://www.maketecheasier.com/vim-keyboard-shortcuts-cheatsheet/)

## Markdown
This [cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) covers the basics really well

## tmux
We ought to customise this, as demonstrated [here](https://www.hamvocke.com/blog/a-guide-to-customizing-your-tmux-conf/)

See the configs folder for the `.tmux.conf file`

## Font

Use [Fira Code](https://github.com/tonsky/FiraCode), or for NerdFonts, [Fura Code](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/FiraCode)

## IDE

Seems that PyCharm Professional offers it all:
* [Remote Debugging](https://www.jetbrains.com/help/pycharm/remote-debugging-with-product.html)
    * NB: If the variables are too large (i.e., large batches of image arrays), this will hang!
* [Remote Interpreter (via SSH)](https://www.jetbrains.com/help/pycharm/configuring-remote-interpreters-via-ssh.html)

Configure with [Monokai](https://github.com/spasserby/PyCharm-monokai) for a e s t h e t i c s

## Configs and DotFiles

We need to set this up like so, but basically clever symlinking and github backups (kinda like this file):

* [Getting Started with Dotfiles](https://medium.com/@webprolific/getting-started-with-dotfiles-43c3602fd789)
* [Git and Dotfiles](http://xxeo.com/archives/2010/02/16/dotfiles-in-git-finally-did-it.html)