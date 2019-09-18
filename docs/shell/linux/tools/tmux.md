# 简介

本文用于记录`tmux`的相关用法。

## 指令集合

本文主要介绍以下分类:

* attach session
* detach session
* create pane
* manage session
    * create session
    * kill session
* resize pane

### attach session

与`attach session`有关的指令如下:

| 指令   |   介绍  |
|-------|---------|
| `tmux ls` |  显示目前所有的`session` |
| `tmux attach -t [sessionNumber]`  | 根据*session number*链接session|

### detach session

| 指令    |  介绍  |
|---------|--------|
| `tmux detach` |  与当前的`session`断开连接 |
| `"Ctrl+b"` -> d  | 使用快捷键断开`session`连接，先按`Ctrl+b`,松开后按`d`  |

### manage session

| 指令     | 介绍   |
|----------|--------|
| `tmux kill-server`  | kill server,删除所有的`session` |
|在默认终端中输入`tmux`  | 创建一个新的session |
| `tmux rename-session -t 0 mysession` |  将session 0重命名为`mysession` |

### create pane

在一个`session`中，我们可以创建多个`pane`来同时进行工作

| 指令      |  介绍    |
|----------|-----------|
| `"Ctrl+b"` -> %  | 垂直切分window |
| `"Ctrl+b"` -> "  | 水平切分window  |
| `"Ctrl+b"` -> arrow | 在多个`pane`中切换焦点 |

### resize pane

1. 按住`Ctrl+b`的同时，快速按`左键`或`右键`调节宽度

> 这里必须是按住`Ctrl+b`的同时按`左键`或`右键`

## 参考文档

* [Easy guide to tmux](https://www.hamvocke.com/blog/a-quick-and-easy-guide-to-tmux/)