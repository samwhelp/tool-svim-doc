
# Feature

## Key Binding

* [Leader Key](#leader-key)
* [Quick Switch](#quick-switch)
* [Window Resize](#window-resize)
* [Delete Buffer](#delete-buffer)
* [Quit](#quit)
* [Hide](#hide)
* [Only](#only)
* [Buffer List](#buffer-list)
* [Save](#save)
* [TabPage](#tabpage)


## Leader Key

| Key | Map | Notice |
| --- | --- | --- |
| `,` | for main use | vim [,](https://vimhelp.org/motion.txt.html#,) orginal had function |
| `\` | for sub use | vim [leader](https://vimhelp.org/map.txt.html#mapleader) default is [backslash](https://vimhelp.org/intro.txt.html#backslash) |
| `t` | for TabPage  | vim [t](https://vimhelp.org/motion.txt.html#t) orginal had function |


> About orginal [,](https://vimhelp.org/motion.txt.html#,) and [t](https://vimhelp.org/motion.txt.html#t), please read vim [f](https://vimhelp.org/motion.txt.html#f), [F](https://vimhelp.org/motion.txt.html#F), [t](https://vimhelp.org/motion.txt.html#t), [T](https://vimhelp.org/motion.txt.html#T), [;](https://vimhelp.org/motion.txt.html#;), [,](https://vimhelp.org/motion.txt.html#,).


> Please read :help [normal-index](https://vimhelp.org/index.txt.html#normal-index)

> Please read :help [,](https://vimhelp.org/motion.txt.html#,)

> Please read :help [t](https://vimhelp.org/motion.txt.html#t)


I use (,) and (t) for my leader key.



## Quick Switch

| Key | Map | Description |
| --- | --- | --- |
| `<Backspace>` | [C-w W](https://vimhelp.org/windows.txt.html#CTRL-W_W) | To Previous Window |
| `<Tab>` | [C-w w](https://vimhelp.org/windows.txt.html#CTRL-W_w) | To Next Window |
| `<Ctrl+j>` | [:bprevious](https://vimhelp.org/windows.txt.html#:bprevious)&lt;CR&gt; |  To Previous Buffer |
| `<Ctrl+k>` | [:bnext](https://vimhelp.org/windows.txt.html#:bnext)&lt;CR&gt; | To Next Buffer |
| `<Ctrl+h>` | [:tabprevious](https://vimhelp.org/tabpage.txt.html#:tabprevious)&lt;CR&gt; | To Previous TabPage |
| `<Ctrl+l>` | [:tabnext](https://vimhelp.org/tabpage.txt.html#:tabnext)&lt;CR&gt; | To Next TabPage |


## Window Resize

| Key | Map |
| --- | --- |
| ` <S-Down>` | [&lt;C-w&gt;-](https://vimhelp.org/windows.txt.html#CTRL-W_-) |
| ` <S-Up>` | [&lt;C-w&gt;+](https://vimhelp.org/windows.txt.html#CTRL-W_+) |
| ` <S-Left>` | [&lt;C-w&gt;<](https://vimhelp.org/windows.txt.html#CTRL-W_<) |
| ` <S-Right>` | [&lt;C-w&gt;>](https://vimhelp.org/windows.txt.html#CTRL-W_>) |


## Delete Buffer

| Key | Map | Description | Notice |
| --- | --- | --- | --- |
| `,q` | [:bdelete](https://vimhelp.org/windows.txt.html#:bdelete)&lt;CR&gt; | delete current buffer | single |
| `,x` | [:%bdelete](https://vimhelp.org/windows.txt.html#:bdelete)&lt;CR&gt; | delete all buffer | all |
| `,z` | [:bdelete!](https://vimhelp.org/windows.txt.html#:bdelete)&lt;CR&gt; | force delete current buffer | single |
| `,c` | [:%bdelete!](https://vimhelp.org/windows.txt.html#:bdelete)&lt;CR&gt; | force delete all buffer | all |


## Quit

| Key | Map | Description | Notice |
| --- | --- | --- | --- |
| `\q` | [:q](https://vimhelp.org/editing.txt.html#:q)&lt;CR&gt; | quit | single |
| `\x` | [:qa](https://vimhelp.org/editing.txt.html#:qa)&lt;CR&gt; | quit all | all |
| `\z` | [:q!](https://vimhelp.org/editing.txt.html#:q)&lt;CR&gt; | force quit | single |
| `\c` | [:qa!](https://vimhelp.org/editing.txt.html#:qa)&lt;CR&gt; | force quit all | all |

> Please read :help ['confirm'](https://vimhelp.org/options.txt.html#'confirm').


## Hide

| Key | Map | Description | Notice |
| --- | --- | --- | --- |
| `,h` | [:hide](https://vimhelp.org/windows.txt.html#:hide)&lt;CR&gt; | hide current buffer | single |

> Compare with `,x`, `,c`, `\x`, `\c`, `,h`。

## Only

| Key | Map | Description |
| --- | --- | --- |
| `,wa` | [:only](https://vimhelp.org/windows.txt.html#:only)&lt;CR&gt; | to close other window, then all buffer will hide, if set [hidden](https://vimhelp.org/options.txt.html#'hidden'). |
| `twa` | [:tabonly](https://vimhelp.org/tabpage.txt.html#:tabonly)&lt;CR&gt; | wa to close other tabpage, then all buffer will hide, if set [hidden](https://vimhelp.org/options.txt.html#'hidden'). |


## Buffer List

| Key | Map | Description |
| --- | --- | --- |
| `,b` | [:ls](https://vimhelp.org/windows.txt.html#:ls)&lt;CR&gt; | Show all buffers. |


## Save

| Key | Map | Description | Notice |
| --- | --- | --- | --- |
| `<S-Tab>` | [:w](https://vimhelp.org/editing.txt.html#:w)&lt;CR&gt; | Write the whole buffer to the current file. | Work on Normal Mode and Insert Mode |


## TabPage

| Key | Map | Description |
| --- | --- | --- |
| `ts` | [:tab split](https://vimhelp.org/tabpage.txt.html#:tab)&lt;CR&gt; | Opens current buffer in new tab page |
| `tg` | [:tabnew](https://vimhelp.org/tabpage.txt.html#:tabnew)&lt;CR&gt; | New TabPage |
| `tf` | [:tabnew](https://vimhelp.org/tabpage.txt.html#:tabnew)&lt;CR&gt;[:edit](https://vimhelp.org/editing.txt.html#:edit)&lt;Space&gt; | New tabpage and wait for user input file path |
| `te` | [:tabedit](https://vimhelp.org/tabpage.txt.html#:tabedit)&lt;Space&gt; | Edit file on new tabpage. |



### Switch TabPage

| Key | Map | Description |
| --- | --- | --- |
| `tp` | [:tabprevious](https://vimhelp.org/tabpage.txt.html#:tabprevious)&lt;CR&gt; | To Previous TabPage |
| `tn` | [:tabnext](https://vimhelp.org/tabpage.txt.html#:tabnext)&lt;CR&gt; | To Next TabPage |


| Key | Map | Description |
| --- | --- | --- |
| `th` | [:tabprevious](https://vimhelp.org/tabpage.txt.html#:tabprevious)&lt;CR&gt; | To Previous TabPage |
| `tl` | [:tabnext](https://vimhelp.org/tabpage.txt.html#:tabnext)&lt;CR&gt; | To Next TabPage |
| `tj` | [:tabfirst](https://vimhelp.org/tabpage.txt.html#:tabfirst)&lt;CR&gt; | To First TabPage |
| `tk` | [:tablast](https://vimhelp.org/tabpage.txt.html#:tablast)&lt;CR&gt; | To Last TabPage |

> Compare with [Quick Switch](#quick-switch) `<Ctrl+h>` and `<Ctrl+l>` .


### Tab Move

| Key | Map | Description |
| --- | --- | --- |
| `tu` | [:-tabmove](https://vimhelp.org/tabpage.txt.html#:tabmove)&lt;CR&gt; | Tab Move to Left |
| `ti` | [:+tabmove](https://vimhelp.org/tabpage.txt.html#:tabmove)&lt;CR&gt; | Tab Move to Right |


| Key | Map | Description |
| --- | --- | --- |
| `tmh` | [:-tabmove](https://vimhelp.org/tabpage.txt.html#:tabmove)&lt;CR&gt; | Tab Move to Left |
| `tml` | [:+tabmove](https://vimhelp.org/tabpage.txt.html#:tabmove)&lt;CR&gt; | Tab Move to Right |
| `tmj` | [:0tabmove](https://vimhelp.org/tabpage.txt.html#:tabmove)&lt;CR&gt; | Tab Move to First |
| `tmk` | [:$tabmove](https://vimhelp.org/tabpage.txt.html#:tabmove)&lt;CR&gt; | Tab Move to Last |
