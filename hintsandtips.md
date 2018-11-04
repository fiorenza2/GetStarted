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

## Bash

Use aliases:

```bash
alias sublime="/mnt/c/Program\ Files/Sublime\ Text\ 3/sublime_text.exe ."
```

## vim

Some neat shortcuts:

|Command    | Outcome                       | Mode      |
| Esc       | Get back into command mode    | Insert    |

* i: Insert mode to actual make edits
* dd: Be in command mode to delete the line
* PgDown/PgUp: Quick traversal
* 0: Move cursor to the beginning of the line
* /: Search for text


## Markdown
This [cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) is pretty amazing

## tmux
We ought to customise this, as demonstrated [here](https://www.hamvocke.com/blog/a-guide-to-customizing-your-tmux-conf/)