## Introduction
This document contains frequently used command and the corresponding used cases for terminal multiplexer tmux. For simplification, all the variables are written in parenthesis, e.g. (name).

&nbsp;
## Table of Content
* [Installation](#installation)
* [Session Operations](#session-operations)
* [Window Operations](#window-operations)
* [Pane Operations](#pane-operations)
* [Miscellaneous](#miscellaneous)

&nbsp;
## Installation
<sub>[Back to Top](#introduction)</sub>
#### Install tmux on Mac
```
brew install tmux
```
#### Install tmux on Linux (RHEL)
```
sudo yum install tmux
```
#### Install tmux on Linux (Debian)
```
sudo apt install tmux
```

&nbsp;
## Session Operations
<sub>[Back to Top](#introduction)</sub>
#### Start tmux session
```
tmux
```
#### Start tmux session with custom session name
```
tmux new -s (name)
```
#### Detach tmux session
```
Ctrl+b, d
```
#### Show all tmux sessions
```
tmux ls
```
#### Attach tmux session in the background
```
tmux attach-session -t (name)
```
#### Kill tmux session
```
tmux kill-session -t (name)
```

&nbsp;
## Window Operations
<sub>[Back to Top](#introduction)</sub>
#### Create new window
```
Ctrl+b, c
```
#### Kill window
```
Ctrl+b, &
```
#### Select the window to switch to
```
Ctrl+b, w
```
#### Switch to specific window
```
Ctrl+b, (number)
```

&nbsp;
## Pane operations
<sub>[Back to Top](#introduction)</sub>
#### Create vertical split
```
Ctrl+b, "
```
#### Create horizontal split
```
Ctrl+b, %
```
#### Close pane
```
Ctrl+b, x
```
#### Switch to specific pane
```
Ctrl+b, (arrow button)
```
#### Switch to next pane
```
Ctrl+b, o
```
#### Switch to next layout
```
Ctrl+b, (space)
```

&nbsp;
## Miscellaneous
<sub>[Back to Top](#introduction)</sub>
#### Enable scrolling
```
Ctrl+b, [
```
#### Quit scrolling
```
q
```