# BASH

[![HOME](../../img/button_home.png)](https://github.com/mmmarceleza/My-Learning-Tracker#marcelos-learning-tracker) &nbsp; &nbsp; [![MY ARTICLES](../../img/button_article.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/my-articles.md#my-articles) &nbsp; &nbsp; [![PORTFOLIO](../../img/button_portfolio.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/portfolio.md#portfolio) &nbsp; &nbsp; [![LEARNING LOG](../../img/button_log.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/learning-log.md#learning-log)

***

## Bash Customization with Powerline

This is a simple guide to install `Powerline` to make your terminal look beautiful

Useful links:
* [Powerline GitHub](https://github.com/powerline/powerline)
* [Powerline Documentation](https://powerline.readthedocs.io/en/latest/)
* [Powerline for Bash](https://earlybyte.medium.com/powerline-for-bash-6d3dd004f6fc)
* [Making Powerline Work In Visual Studio Code Terminal](https://dev.to/mattstratton/making-powerline-work-in-visual-studio-code-terminal-1m7)

## Instalation 

### Manjaro
```bash
$ sudo pacman -S powerline
```
### Ubuntu
```bash
$ sudo apt install powerline
```
## Configure Bash
Just to assure the correct path of installation `{powerline_root}`, use this command:
```
$ pip3 show powerline-status
```
It's important to pay attention to result of the previous command to use the correct path in your `.bashrc` file. To configure Powerline for bash, add the following lines to your `$HOME/.bashrc` file:
```bash
# Powerline configuration
if [ -f /usr/share/powerline/bindings/bash/powerline.sh ]; then
  powerline-daemon -q
  POWERLINE_BASH_CONTINUATION=1
  POWERLINE_BASH_SELECT=1
  source /usr/share/powerline/bindings/bash/powerline.sh
fi
```  
To apply the changes to your current terminal:
```bash
$ source ~/.bashrc
```
After running the previous command or restarting your terminal, the Powerline segments appear in your prompt.

## Git Status for Bash
Install the following package: 
- `powerline-gitstatus`

Open the following file and add the lines after the “attached_clients” entry:
- `{powerline_root}/powerline/config_files/colorschemes/default.json`

```
"gitstatus":                 { "fg": "gray8",           "bg": "gray2", "attrs": [] },
"gitstatus_branch":          { "fg": "gray8",           "bg": "gray2", "attrs": [] },
"gitstatus_branch_clean":    { "fg": "green",           "bg": "gray2", "attrs": [] },
"gitstatus_branch_dirty":    { "fg": "gray8",           "bg": "gray2", "attrs": [] },
"gitstatus_branch_detached": { "fg": "mediumpurple",    "bg": "gray2", "attrs": [] },
"gitstatus_tag":             { "fg": "darkcyan",        "bg": "gray2", "attrs": [] },
"gitstatus_behind":          { "fg": "gray10",          "bg": "gray2", "attrs": [] },
"gitstatus_ahead":           { "fg": "gray10",          "bg": "gray2", "attrs": [] },
"gitstatus_staged":          { "fg": "green",           "bg": "gray2", "attrs": [] },
"gitstatus_unmerged":        { "fg": "brightred",       "bg": "gray2", "attrs": [] },
"gitstatus_changed":         { "fg": "mediumorange",    "bg": "gray2", "attrs": [] },
"gitstatus_untracked":       { "fg": "brightestorange", "bg": "gray2", "attrs": [] },
"gitstatus_stashed":         { "fg": "darkblue",        "bg": "gray2", "attrs": [] },
"gitstatus:divider":         { "fg": "gray8",           "bg": "gray2", "attrs": [] }
```

Open the following file and change the lines:
- `{powerline_root}/powerline/config_files/themes/shell/default.json`

Change line from:

```
"function": "powerline.segments.shell.jobnum",
"priority": 20
```

To:
```
"function": "powerline_gitstatus.gitstatus",
"priority": 40
```

You must copy the configurations to the user’s home to ensure that the configuration persists even when update change things in the background.

Create the directory structure in your user's home:

```
mkdir ~/.config/powerline
mkdir ~/.config/powerline/colorschemes   
mkdir ~/.config/powerline/themes
mkdir ~/.config/powerline/themes/shell
```

Copy the configuration files:

```
cp {powerline_root}/powerline/config_files/colorschemes/default.json ~/.config/powerline/colorschemes/
cp {powerline_root}/powerline/config_files/themes/shell/default.json ~/.config/powerline/themes/shell/
```

## Configure Vim
To configure Powerline for Vim, add the following lines to your `$HOME/.vimrc` file:
```bash
python3 from powerline.vim import setup as powerline_setup
python3 powerline_setup()
python3 del powerline_setup

set laststatus=2
```
## Configure tmux
To configure Powerline in tmux, add the following to your `~/.tmux.conf` file:
```bash
set -g default-terminal "screen-256color"
source "/usr/share/powerline/bindings/tmux/powerline.conf"
```
## Other options

[Starship](https://starship.rs/)
