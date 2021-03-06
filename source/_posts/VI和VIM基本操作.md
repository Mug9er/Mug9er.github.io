---
title: VI和VIM基本操作
categories: [Linux 学习笔记]
tags: [Vim]
abbrlink: a67e3062
date: 2021-04-29 00:21:54
img: https://cdn.jsdelivr.net/gh/Mug-9/imge-stroage@master/cover/wallhaven-o3gmw9.2q0klcmfizw0.png
---

VI和VIM基本操作

<!-- less-->

# Vi和Vim 基本操作

## Vi的插入

| 按键 |          功能          |
| :--: | :--------------------: |
| `a`  |  光标位置右边插入文字  |
| `i`  | 光标位置当前处插入文字 |
| `o`  |  光标位置下方开启新行  |
| `O`  |  光标位置上方开启新行  |
| `I`  |  光标所在行首插入文字  |
| `A`  |  光标所在行尾插入文字  |

## Vi 的退出

|      按键       |                     功能                     |
| :-------------: | :------------------------------------------: |
| `ZZ(shift+z+z)` |                   保存退出                   |
|      `:wq`      |                   保存退出                   |
|      `:x`       |                   保存退出                   |
|  `:w filename`  |                保存在指定文件                |
|      `:q`       | 退出，如果文件修改但没有保存，会提示无法退出 |
|      `:q!`      |                 退出，不保存                 |
|    `:!命令`     |            暂时离开`vi`，执行命令            |

## Vi的删除和修改功能

|  按键   |                             功能                             |
| :-----: | :----------------------------------------------------------: |
| `[n]x`  |                     删除光标后`n`的字符                      |
| `[n]X`  |                     删除光标前`n`的字符                      |
|   `D`   |                删除光标所在开始到此行尾的字符                |
| `[n]dd` | 删除从当前行开始的`n`行（准确来说，是剪切，剪切不粘贴即为删除） |
| `[n]yy` |              复制从当前行开始的`n`行，向下复制               |
|   `p`   |                 把粘贴板上的内容插入到当前行                 |
|  `dG`   |              删除光标所在开始到文件尾的所有字符              |
|   `J`   | 合并两行，将光标所在行和下一行进行合并，在两行中间加入一个空格 |
|   `.`   |                       执行上一次的操作                       |
|   `u`   |                        撤销前一个命令                        |

##   Vi的行定位功能

|   按键    |              功能               |
| :-------: | :-----------------------------: |
| `ctrl+f`  |        向前滚动一个屏幕         |
| `ctrl+b`  |        向后滚动一个屏幕         |
|   `gg`    |        到文件第一行行首         |
|    `G`    | 到文件最后一行行首，`G`必需大写 |
|   `:$`    |     到文件最后一行（行首）      |
| `mG或mgg` |     到指定行，`m`为目标行数     |
|  `/内容`  |          查找指定内容           |

## Vi的文本查找功能

|    按键    |           功能           |
| :--------: | :----------------------: |
| `/字符串`  |      查找指定字符串      |
|    `n`     |        寻找下一个        |
|    `N`     |        回到前一个        |
|    `?`     |        查找上一个        |
| `/^字符串` |   查找以字符串开始的行   |
| `/字符串$` |   查找以字符串结尾的行   |
|   `/a.b`   | 查找字符串`a`任意字符`b` |

## Vi的替换功能

|        按键        |                功能                |
| :----------------: | :--------------------------------: |
|        `r`         |          替换当前光标字符          |
|    `:r 文件名`     | 在光标当前位置下一行载入另一个文件 |
|    `:s/p1/p2/g`    |   将当前行中所有`p1`均用`p2`替代   |
|  `:g/p1/s//p2/g`   |    将文件中所有`p1`均用`p2`替代    |
| `:n1,n2 s/p1/p2/g` | 将`n1`到`n2`行中所有`p1`用`p2`替代 |

## Vi的`set`指令

|    按键     |        功能        |
| :---------: | :----------------: |
|  `:set ic`  |  搜寻是忽略大小写  |
| `:set noic` | 搜寻是不忽略大小写 |
|  `:set nu`  |      显示行号      |
| `:set nonu` |     不显示行号     |

