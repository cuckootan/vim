My Vim configuration bundle forked from guochunyang.

---

## 1 下载与安装

```shell
git clone git@github.com:cuckootan/vim.git ~/.vim
cp ~/.vim/vimrc ~/.vimrc
```

## 2 配置

### 2.1 配置主题颜色

由于在终端背景颜色为黑色的时候，用 vim 打开的文件中的注释看不清，因此需要将注释的颜色改成其他颜色：

打开 **~/.vimrc**，在最后添加如下： 

**hi Comment ctermfg = blue**

其中，blue 为蓝色，也可以修改成其他颜色。

### 2.2 配置 snippets

所有编程语言相关的 snippet 文件都在下面这个目录里：

**~/.vim/bundle/snipmate.vim/snippets/**

可以根据相应格式进行增删改。

需要用到的变量可以在 **~/.vimrc** 进行设置。比如：

```shell
" Snippets variables
let g:snips_author = 'Your Name'
let g:snips_email = 'Your Email'
set rtp+=~/.vim/bundle/snipmate.vim/snippets/''"
```

>   注意，需要设置 rtp 变量，有点类似于 Shell 中的环境变量。
