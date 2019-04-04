
# 特色簡介

## 前提

我操作「[vim](https://packages.ubuntu.com/bionic/vim)」的環境是「[Ubuntu 18.04](https://samwhelp.github.io/note-ubuntu-18.04/)」，桌面環境是「[lxqt](https://samwhelp.github.io/note-ubuntu-18.04/read/subject/lxqt/install-lxqt)」，使用的是「[gnome-terminal](https://packages.ubuntu.com/bionic/gnome-terminal)」或是「[qterminal](https://packages.ubuntu.com/bionic/qterminal)」。

## 按鍵設定

目前幾個開頭的按鍵

| 按鍵 | 說明 | 注意事項 |
| --- | --- | --- |
| `\` | 次常用 | vim預設的「[leader](https://vimhelp.org/map.txt.html#mapleader)」，我沒有更改，也就是「[backslash](https://vimhelp.org/intro.txt.html#backslash)」 |
| `,` | 常用 | 注意「[,](https://vimhelp.org/motion.txt.html#,)」原本是有功能的 |
| `t` | TabPage 相關功能 | 注意「[t](https://vimhelp.org/motion.txt.html#t)」原本是有功能的 |

> 關於「[,](https://vimhelp.org/motion.txt.html#,)」和「[f](https://vimhelp.org/motion.txt.html#f)」原本的功能，是「[f](https://vimhelp.org/motion.txt.html#f)」，「[F](https://vimhelp.org/motion.txt.html#F)」，「[t](https://vimhelp.org/motion.txt.html#t)」，「[T](https://vimhelp.org/motion.txt.html#T)」，搭配「[;](https://vimhelp.org/motion.txt.html#;)」和「[,](https://vimhelp.org/motion.txt.html#,)」這組的功能。

> 可以執行「:help [normal-index](https://vimhelp.org/index.txt.html#normal-index)」，

> 可以執行「:help [,](https://vimhelp.org/motion.txt.html#,)」，

> 可以執行「:help [t](https://vimhelp.org/motion.txt.html#t)」，

> 閱讀原本功能的相關說明。

而「,」和「t」，則是我配置用來當作開頭的按鍵。

### Normal Mode

主要對「Buffer」，「Window」，「TabPage」增加了一些「按鍵」，來便利操作。

> 以下都是在「Normal Mode」所做的按鍵操作。

> 若是在其他「Mode」可以使用 「Ctrl+[」 或 「[Esc](https://vimhelp.org/intro.txt.html#escape)」  來返回「Normal Mode」， 接著再操作下面的按鍵功能，

> 亦或是使用 <Ctrl+c> 也可以用來返回。

舉例：要找到在「Insert Mode」要返回「Normal Mode」的按鍵相關說明，

可以查詢
「:help [i_CTRL-\[ ](https://vimhelp.org/insert.txt.html#i_CTRL-[)」
「:help [i_CTRL-C ](https://vimhelp.org/insert.txt.html#i_CTRL-C)」
可以找到相關說明。


以下開始來說明我個人的按鍵配置

#### 快速切換

| 按鍵 | 對應 | 說明 |
| --- | --- | --- |
| `<Backspace>` | [C-w W](https://vimhelp.org/windows.txt.html#CTRL-W_W) | 切換到上一個 Window |
| `<Tab>` | [C-w w](https://vimhelp.org/windows.txt.html#CTRL-W_w) | 切換到下一個 Window |
| `<Ctrl+j>` | [:bprevious](https://vimhelp.org/windows.txt.html#:bprevious) | 切換到上一個 Buffer |
| `<Ctrl+k>` | [:bnext](https://vimhelp.org/windows.txt.html#:bnext) | 切換到下一個 Buffer |
| `<Ctrl+h>` | [:tabprevious](https://vimhelp.org/tabpage.txt.html#:tabprevious) | 切換到上一個 TabPage |
| `<Ctrl+l>` | [:tabnext](https://vimhelp.org/tabpage.txt.html#:tabnext) | 切換到下一個 TabPage |

#### 離開

> 以下「q」或「z」會是「單一」。

> 以下「x」或「c」會是「全部」。

離開 Window 或 TabPage 並且**刪除**目前顯示的 Buffer，

若只剩最後一個 Window，會離開「vim」。

| 按鍵 | 對應 | 說明 | 注意事項 |
| --- | --- | --- | --- |
| `\q` | [:q](https://vimhelp.org/editing.txt.html#:q) | 單一離開 | 若未存檔，會有確認訊息 |
| `\x` | [:qa](https://vimhelp.org/editing.txt.html#:qa) | 全部離開 | 若未存檔，會有確認訊息 |
| `\z` | [:q!](https://vimhelp.org/editing.txt.html#:q) | 單一離開 | 若未存檔，不存檔直接離開 |
| `\c` | [:qa!](https://vimhelp.org/editing.txt.html#:qa) | 全部離開 | 若未存檔，不存檔直接離開 |

> 這組我最常使用的是「`\c`」，來離開「vim」，注意這個是沒有存檔的。

> 目前沒有對應「`:wqa`」，請直接下指令，或是採用「`\x`」，會有確認存檔提示出現。

#### 關閉 (刪除Buffer)

關閉 Window 或 TabPage 並且**刪除**目前顯示的 Buffer，

若只剩最後一個 Window，並不會離開「vim」。

| 按鍵 | 對應 | 說明 | 注意事項 |
| --- | --- | --- | --- |
| `,q` | [:bdelete](https://vimhelp.org/windows.txt.html#:bdelete) | 單一關閉 | 若未存檔，會有確認訊息 |
| `,x` | [:%bdelete](https://vimhelp.org/windows.txt.html#:bdelete) | 全部關閉 | 若未存檔，會有確認訊息 |
| `,z` | [:bdelete!](https://vimhelp.org/windows.txt.html#:bdelete) | 單一關閉 | 若未存檔，直接關閉 |
| `,c` | [:%bdelete!](https://vimhelp.org/windows.txt.html#:bdelete) | 全部關閉 | 若未存檔，直接關閉 |

平常改用這組來關閉，就不會常常離開「vim」 。

#### 隱藏

關閉 Window 或 TabPage 並且**隱藏**目前顯示的 Buffer。

若只剩最後一個Window，並不會離開「vim」。

| 按鍵 | 對應 | 說明 | 注意事項 |
| --- | --- | --- | --- |
| `,h` | [:hide](https://vimhelp.org/windows.txt.html#:hide) | 單一關閉 | 若未存檔，直接關閉，並且**隱藏**目前顯示的 Buffer|

> 可以使用「`,b`」來觀看「Buffer 列表」。


#### 列表

| 按鍵 | 對應 | 說明 |
| --- | --- | --- |
| `,b` | [:ls](https://vimhelp.org/windows.txt.html#:ls) | Buffer 列表 |
| `,m` | [:marks](https://vimhelp.org/motion.txt.html#:marks) | Mark 列表 |
| `,r` | [:registers](https://vimhelp.org/change.txt.html#:registers) | Register 列表 |

其他還有「[:jumps](https://vimhelp.org/motion.txt.html#:jumps)」,「[:changes](https://vimhelp.org/motion.txt.html#:changes)」,「[:tags](https://vimhelp.org/tagsrch.txt.html#:tags)」，不過我還沒設定按鍵就是了。

#### Only

| 按鍵 | 對應 | 說明 | 注意事項 |
| --- | --- | --- | --- |
| `,wa` | [:only](https://vimhelp.org/windows.txt.html#:only) | 關閉其它 Window | 1. 被關閉的 Window，該顯示 Buffer 只是隱藏。 2.若有其他的「TabPage」，不會關閉其他「TabPage」的「Window」。 |
| `twa` | [:tabonly](https://vimhelp.org/tabpage.txt.html#:tabonly) | 關閉其他 TabPage | 1. 被關閉的 TabPage，該顯示 Buffer 只是隱藏。 |

> 可以使用「`,b`」來觀看「Buffer 列表」。

> 可以對照上面「`,x`」和「`,c`」以及「`,h`」的功能。

#### 存檔

| 按鍵 | 對應 | 說明 |
| --- | --- | --- |
| `,s` | [:w](https://vimhelp.org/editing.txt.html#:w) | 目前視窗顯示的 Buffer 存檔 |

其他的存檔功能，目前我是直接下指令，例如「[:saveas ](https://vimhelp.org/editing.txt.html#:saveas)」或「[:w ](https://vimhelp.org/editing.txt.html#:w_f)」。


## 其他對應

還有其他的對應，暫時還沒寫說明文件，請先參考「[原始碼](https://github.com/samwhelp/tool-svim-core/blob/master/plugin/Svim.vim#L753)」。


## 後續建議

若對「Vim」裡的「Buffer」，「Window」，「TabPage」的相關概念，尚未釐清，

建議可以閱讀「[usr_07.txt](https://vimhelp.org/usr_07.txt.html#usr_07.txt)」和「[usr_08.txt](https://vimhelp.org/usr_08.txt.html#usr_08.txt)」，來了解。

在「shell」執行下面指令

``` sh
$ vim -c ':help usr_07.txt | :only'
```

在「shell」執行下面指令

``` sh
$ vim -c ':help usr_08.txt | :only'
```

也可以進到「vim」，執行下面指令

``` vim
:help usr_07.txt
```

和

``` vim
:help usr_08.txt
```

## 連結

此頁的內容也可以連到「[GitHub](https://github.com/samwhelp/tool-svim-doc/blob/master/read/zh_tw/feature.md)」上觀看。
