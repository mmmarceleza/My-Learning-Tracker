# TMUX

[![HOME](../../img/button_home.png)](https://github.com/mmmarceleza/My-Learning-Tracker#marcelos-learning-tracker) &nbsp; &nbsp; [![MY ARTICLES](../../img/button_article.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/my-articles.md#my-articles) &nbsp; &nbsp; [![PORTFOLIO](../../img/button_portfolio.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/portfolio.md#portfolio) &nbsp; &nbsp; [![LEARNING LOG](../../img/button_log.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/learning-log.md#learning-log)

***

Tmux is a terminal multiplexer. You can run many command line programs at the same time. After you start a session, it is possible to manipulate it using prefix key (`control + b`).
## Terms used on Tmux
| **TERM** | **DESCRIPTION** |
|:---|:---|
| Client |	Attaches a tmux session from an outside terminal such as xterm(1) |
| Session |	Groups one or more windows together |
| Window 	| Groups one or more panes together, linked to one or more sessions |
| Pane | Contains a terminal and running program, appears in one window |
| Active pane | The pane in the current window where typing is sent; one per window |
| Current window |	The window in the attached session where typing is sent; one per session |
| Last window |	The previous current window |
| Session name	| The name of a session, defaults to a number starting from zero |
| Window list |	The list of windows in a session in order by number |
| Window name	| The name of a window, defaults to the name of the running program in the active pane|
| Window index	| The number of a window in a session's window list |
| Window layout |	The size and position of the panes in a window |


## Basic Sessions Commands

Start a session:
```bash
$ tmux
```
or
```bash
$ tmux new
```
```bash
$ tmux new-session
```
 If you are inside a session, 
Start a session with a specific name:
```bash
tmux new -s [SESSION NAME]
```




## References

- [Tmux customization ](https://github.com/gpakosz/.tmux)
- [Tmux Cheat Sheet](https://tmuxcheatsheet.com/)