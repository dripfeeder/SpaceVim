---
title: "SpaceVim colorscheme 模块"
description: "colorscheme 模块为 SpaceVim 提供了一系列的常用颜色主题，默认情况下使用深色 gruvbox 作为默认主题。该模块提供了快速切换主题、随即主题等特性"
lang: cn
---

# [可用模块](https://spacevim.org/layers) >> colorscheme

<!-- vim-markdown-toc GFM -->

- [模块描述](#模块描述)
- [启用模块](#启用模块)
- [模块配置](#模块配置)

<!-- vim-markdown-toc -->

## 模块描述

colorscheme 模块为 SpaceVim 提供了一系列常用的颜色主题，默认情况为深色的 gruvbox 主题。

## 启用模块

默认情况下，这一模块并为启用，如果需要使用更多的颜色主题，可以启用该模块，在配置
文件内加入如下内容：

```toml
[[layers]]
  name = 'colorscheme'
```

## 模块配置

如果需要修改默认主题，可在配置文件中修改 colorscheme 选项，改为主题名称即可。

```toml
[options]
  colorscheme = "onedark"
```

**主题列表**

| 名称       | 深色主题 | 浅色主题 | 终端支持 | Gui支持 | 状态栏支持 |
| ---------- | -------- | -------- | -------- | ------- | ---------- |
| gruvbox    | yes      | yes      | yes      | yes     | yes        |
| one        | yes      | yes      | yes      | yes     | yes        |
| molokai    | yes      | no       | yes      | yes     | yes        |
| jellybeans | yes      | no       | yes      | yes     | yes        |
| nord       | yes      | no       | yes      | yes     | yes        |
| onedark    | yes      | no       | yes      | yes     | yes        |

部分主题提供了深色和浅色两系列的主题，可以通过设置主题背景色来切换这两种主题。
SpaceVim 支持在配置文件中通过 `colorscheme_bg` 这一选项来设置。


比如，设置默认主题为 onedark，并且使用其深色系列主题：

```toml
[options]
  colorscheme = "onedark"
  colorscheme_bg = 'dark'
```

这一模块提供了，在启动时随机选择主题，而不是使用默认的主题。这一特性可以很
大限度地消除视觉疲劳：

```toml
[[layers]]
  name = 'colorscheme'
  random-theme = true
```
