# General Hints and Tips to Configure Stuff

This is a list for my own use to figure out how to set things up when I use a new computer, because knowing me I'll forget most of the cool stuff I've picked up along the way

## Fish

This seems a solid shell choice, although is not POSIX compliant. However out of the box, it just 'works'. Here's a [neat guide](https://github.com/jorgebucaran/fish-shell-cookbook).

Use this [theme](https://github.com/oh-my-fish/theme-bobthefish).

Since it's not POSIX, here's some common things which are different:

<table>
<tr>
<th>
Action
</th>
<th>
Commands
</th>
</tr>

<tr>

<td style="border-top: solid;">
Exports
</td>

<td style="border-top: solid;">
<pre>
set -gx PATH /home/fiorenza2/anaconda3/bin $PATH
set -x KUBECONFIG /mnt/c/kubeconfig.json
</pre>
</td>

</tr>
<tr>
<td>
Alias
</td>
<td>
<pre>
alias rmi="rm -i"
</pre>
</td>
</tr>
<tr>
<td>
Functions
</td>
<td>
<pre>
function rmi
    rm -i $argv
end
</pre>
</td>
</tr>
</table>

## Python

Anaconda as always

Make a new environment 
```bash
conda env -n ENVNAME -python=3.6
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
This [cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) covers the basics really well.

### MathJax

Note that when we are doing LaTeX equations in MathJax, always surround the ``\begin{equation} ... \end{equation}`` code with dollar signs like so:

``$$\begin{equation} ... \end{equation}$$``

If we dont' do this it won't render properly (well, it can, but then you need loads of escape characters to tell the file that it should render those in TeX).

## tmux
We ought to customise this, as demonstrated [here](https://www.hamvocke.com/blog/a-guide-to-customizing-your-tmux-conf/)

See the configs folder for the `.tmux.conf file`

We can automate tmux by using a session manager, such as [this one](https://github.com/tmux-python/tmuxp) written in Python.

Updating tmux is a bit of a faff, but [this guide](http://witkowskibartosz.com/blog/update-your-tmux-to-latest-version.html) walks us through it well enough.

## Docker

Here's a useful [cheatsheet](https://medium.com/statuscode/dockercheatsheet-9730ce03630d).

[NVidia Dockers](https://devblogs.nvidia.com/gpu-containers-runtime/):
* Install CUDA drivers on the host
* Install CUDA Library on the image

[Interactive Shell with Compose](https://stackoverflow.com/questions/36249744/interactive-shell-using-docker-compose)

Mounting host directories [on the image](https://docs.docker.com/compose/compose-file/#volumes)

## Font

Use [Fira Code](https://github.com/tonsky/FiraCode), or for NerdFonts, [Fura Code](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/FiraCode)

## Mac Specifics

We ought to use [iTerm](https://www.iterm2.com/).

Remember to enable ``Esc+`` option for the left ⌥ key in ``Profiles > Keys``. This means we can use the ⌥ key like the Alt modifier.

## IDE

Seems that PyCharm Professional offers it all:
* [Remote Debugging](https://www.jetbrains.com/help/pycharm/remote-debugging-with-product.html)
    * NB: If the variables are too large (i.e., large batches of image arrays), this will hang!
* [Remote Interpreter (via SSH)](https://www.jetbrains.com/help/pycharm/configuring-remote-interpreters-via-ssh.html)
* [WSL Support to run Ubuntu Python Environments](https://www.jetbrains.com/help/pycharm/2018.3/using-wsl-as-a-remote-interpreter.html)

Configure with [Monokai](https://github.com/spasserby/PyCharm-monokai) for a e s t h e t i c s

## WSL

Use [WSLtty](https://github.com/mintty/wsltty)

This doesn't support stuff like tabbing, but has other neat features like powerline fonts and is themeable. It's also really lightweight and is apparently more customisable.

[This](https://dev.to/winebaths/getting-up-and-running-with-the-windows-subsystem-for-linux-8oc) is a general handy guide.

NB: Enable 'Ctrl+Shift+' Commands in the preference to make copy and pasting from the clipboard a lot less painful

## Configs and DotFiles

We need to set this up like so, but basically clever symlinking and github backups (kinda like this file):

* [Getting Started with Dotfiles](https://medium.com/@webprolific/getting-started-with-dotfiles-43c3602fd789)
* [Git and Dotfiles](http://xxeo.com/archives/2010/02/16/dotfiles-in-git-finally-did-it.html)