
<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

* [1. 分屏启动Vim](#1-分屏启动vim)
	* [1.1 使用小写的o参数来上下分屏。](#11-使用小写的o参数来上下分屏)
	* [1.2 使用大写的O参数来左右分屏。](#12-使用大写的o参数来左右分屏)
* [2. 关闭分屏](#2-关闭分屏)
	* [2.1 关闭当前窗口](#21-关闭当前窗口)
	* [2.2 关闭当前窗口，如果只剩最后一个了，则退出Vim。](#22-关闭当前窗口如果只剩最后一个了则退出vim)
	* [2.3 取消其它分屏，只保留当前分屏](#23-取消其它分屏只保留当前分屏)
* [3. 分屏](#3-分屏)
	* [3.1 上下分割当前打开的文件。](#31-上下分割当前打开的文件)
	* [3.2 上下分割，并打开一个新的文件。](#32-上下分割并打开一个新的文件)
	* [3.3 左右分割当前打开的文件。](#33-左右分割当前打开的文件)
	* [3.4 左右分割，并打开一个新的文件。](#34-左右分割并打开一个新的文件)
	* [3.5 创建空白分屏](#35-创建空白分屏)
* [4. 移动光标](#4-移动光标)
	* [4.1 把光标移到右边的屏。](#41-把光标移到右边的屏)
	* [4.2 把光标移到左边的屏中。](#42-把光标移到左边的屏中)
	* [4.3 把光标移到上边的屏中。](#43-把光标移到上边的屏中)
	* [4.4 把光标移到下边的屏中。](#44-把光标移到下边的屏中)
	* [4.5 把光标移到下一个的屏中。.](#45-把光标移到下一个的屏中)
* [5. 移动分屏](#5-移动分屏)
	* [5.1 向右移动。](#51-向右移动)
	* [5.2向左移动](#52向左移动)
	* [5.3向上移动](#53向上移动)
	* [5.4 向下移动](#54-向下移动)
* [6. 屏幕尺寸](#6-屏幕尺寸)
	* [6.1 让所有的屏都有一样的高度和一样的宽度。](#61-让所有的屏都有一样的高度和一样的宽度)
	* [6.2 设置当前窗口的高度](#62-设置当前窗口的高度)
	* [6.3 增加高度](#63-增加高度)
	* [6.4 减少高度](#64-减少高度)
	* [6.5 设置当前窗口的宽度](#65-设置当前窗口的宽度)
	* [6.6 增加宽度](#66-增加宽度)
	* [6.7 减少宽度](#67-减少宽度)

<!-- /code_chunk_output -->

## 1. 分屏启动Vim

### 1.1 使用小写的o参数来上下分屏。

```
vim -on file1 file2 ...
```

### 1.2 使用大写的O参数来左右分屏。

```
vim -On file1 file2 ...
```

注释: n是数字，表示分成几个屏。



## 2. 关闭分屏 

### 2.1 关闭当前窗口

```
Ctrl+W c(close)
```

### 2.2 关闭当前窗口，如果只剩最后一个了，则退出Vim。

```
Ctrl+W q(quit)
```

### 2.3 取消其它分屏，只保留当前分屏 

```
:only 

或者 

ctrl+w o
```

## 3. 分屏

### 3.1 上下分割当前打开的文件。

```
Ctrl+W s(split)
```

### 3.2 上下分割，并打开一个新的文件。

```
:sp filename
```

### 3.3 左右分割当前打开的文件。 

```
Ctrl+W v(vsplit)
```

### 3.4 左右分割，并打开一个新的文件。

```
:vsp filename
```

### 3.5 创建空白分屏

```
:new
```

## 4. 移动光标

Vi中的光标键是h, j, k, l，要在各个屏间切换，只需要先按一下Ctrl+W

### 4.1 把光标移到右边的屏。

```
Ctrl+W l
```

### 4.2 把光标移到左边的屏中。

```
Ctrl+W h
```

### 4.3 把光标移到上边的屏中。

```
Ctrl+W k
```

### 4.4 把光标移到下边的屏中。

```
Ctrl+W j
```

### 4.5 把光标移到下一个的屏中。.

```
Ctrl+W w
```

## 5. 移动分屏

这个功能还是使用了Vim的光标键，只不过都是大写。当然了，如果你的分屏很乱很复杂的话，这个功能可能会出现一些非常奇怪的症状。

### 5.1 向右移动。

```
Ctrl+W L
```

### 5.2向左移动 

```
Ctrl+W H
```

### 5.3向上移动 

```
Ctrl+W K
```

### 5.4 向下移动 

```
Ctrl+W J
```


## 6. 屏幕尺寸

下面是改变尺寸的一些操作，但这可能需要最新的版本才支持。

### 6.1 让所有的屏都有一样的高度和一样的宽度。

```
Ctrl+W =
```

### 6.2 设置当前窗口的高度

```
:res[ize] [N]

CTRL-W [N]_        设置当前窗口的高度为 N (默认值为最大可能高度)。
```

### 6.3 增加高度

默认增加1

```
Ctrl+W [N]+ 

:res[ize] +[N]   #高度增加N（默认是1）
```

### 6.4 减少高度

```
Ctrl+W [N]-       

:res[ize] -[N]   #高度减少N（默认是1）
```


### 6.5 设置当前窗口的宽度

如果没有N，默认是最大宽度

```
CRTL-W [N]|

:vertical res[ize] [N]     
```

### 6.6 增加宽度

```
CTRL-W [N]>        使得当前窗口宽度加 N (默认值是 1)。

:vertical res[ize] +[N]
```

### 6.7 减少宽度

```
CTRL-W [N]<        使得当前窗口宽度减 N (默认值是 1)。                                
:vertical res[ize] -[N]
```