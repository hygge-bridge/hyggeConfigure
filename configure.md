## tmux

修改~/.tmux.conf：

```shell
# remap prefix from 'C-b' to 'C-a'
unbind C-b
set-option -g prefix C-a
bind-key C-a send-prefix

# split panes using | and s-
bind | split-window -h
bind - split-window -v
unbind '"'
unbind %

# switch panes using Ctrl-arrow without prefix
bind -n C-Left select-pane -L
bind -n C-Right select-pane -R
bind -n C-Up select-pane -U
bind -n C-Down select-pane -D
```

## shell

设置bash为vim模式：

``` shell

$ set -o vi
```

## vim

## git

设置git代理：

```shell
# 使用V2RayN时
$ git config --global http.proxy socks5//:127.0.0.1:10808
$ git config --global https.proxy socks5//:127.0.0.1:10808

# 使用clash时
$ git config --global http.proxy http//:127.0.0.1:<port>
$ git config --global https.proxy https//:127.0.0.1:<port>
```
取消代理：
```shell
git config --global --unset http.proxy
git config --global --unset https.proxy
```




