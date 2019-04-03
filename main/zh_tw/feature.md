
# 特色簡介

## 按鍵設定

目前有幾個開頭的按鍵

| 按鍵 | 說明 | 注意事項 |
| --- | --- | --- |
| `\` | 次常用 | 系統預設的「leader」，我沒有更改 |
| `,` | 常用 | 注意「,」原本是有功能的) |
| `t` | TabPage 相關功能 | 注意「t」原本是有功能的 |

> 關於「,」和「t」，原本的功能是「t」，「f」，「T」，「F」，「;」，「,」這組的功能。

> 可以執行「:help normal-index」，

> 可以執行「:help ,」，

> 可以執行「:help t」，

> 閱讀相關的說明。

### Normal Mode

主要對「Buffer」，「Window」，「TabPage」增加了一些「按鍵」，來便利操作。

#### 快速切換

| 按鍵 | 對應 | 說明 |
| --- | --- | --- |
| `<Backspace>` | C-w W | 切換到上一個 Window |
| `<Tab>` | C-w w | 切換到下一個 Window |
| `<Ctrl+j>` | :bprevious | 切換到上一個 Buffer |
| `<Ctrl+k>` | :bnext | 切換到下一個 Buffer |
| `<Ctrl+h>` | :tabprevious | 切換到上一個 TabPage |
| `<Ctrl+l>` | :tabnext | 切換到下一個 TabPage |

#### 離開

> 以下「q」或「z」會是「單一」。

> 以下「x」或「c」會是「全部」。

離開 Window 或 TabPage 並且*刪除*目前顯示的 Buffer，

若只剩最後一個 Window，會離開「vim」。

| 按鍵 | 對應 | 說明 |
| --- | --- | --- |
| `\q` | :q | 單一離開 (若未存檔，會有提示訊息) |
| `\x` | :qa | 全部離開 (若未存檔，會有提示訊息) |
| `\z` | :q! | 單一離開 (若未存檔，不存檔直接離開) |
| `\c` | :qa! | 全部離開 (若未存檔，不存檔直接離開) |

> 這組我最常使用的是「`\c`」，來離開「vim」，注意這個是沒有存檔的。

> 目前沒有對應「`:wqa`」，請直接下指令，或是採用「`\x`」，會有確認存檔提示出現。

#### 關閉 (刪除Buffer)

關閉 Window 或 TabPage 並且*刪除*目前顯示的 Buffer，

若只剩最後一個 Window，並不會離開「vim」。

| 按鍵 | 對應 | 說明 |
| --- | --- | --- |
| `,q` | :bdelete | 單一關閉 (若未存檔，會有提示訊息) |
| `,x` | :%bdelete | 全部關閉 (若未存檔，會有提示訊息) |
| `,z` | :bdelete! | 單一關閉 (若未存檔，直接關閉) |
| `,c` | :%bdelete! | 全部關閉 (若未存檔，直接關閉) |

平常改用這組來關閉，就不會常常離開「vim」。

#### 隱藏

關閉 Window 或 TabPage 並且*隱藏*目前顯示的 Buffer。

若只剩最後一個Window，並不會離開「vim」。

| 按鍵 | 對應 | 說明 |
| --- | --- | --- |
| `,h` | :hide | 全部關閉 (若未存檔，直接關閉) |

> 可以使用「`,b`」來觀看「Buffer 列表」。


#### 列表

| 按鍵 | 對應 | 說明 |
| --- | --- | --- |
| `,b` | :ls | Buffer 列表 |
| `,m` | :marks | Mark 列表 |
| `,r` | :registers | Register 列表 |


#### Only

| 按鍵 | 對應 | 說明 | 注意事項 |
| --- | --- | --- | --- |
| `,wa` | :only | 關閉其它 Window | 1. 被關閉的 Window，該顯示 Buffer 只是隱藏。 2.若有其他的「TabPage」，不會關閉其他「TabPage」的「Window」。 |
| `twa` | :tabonly | 關閉其他 TabPage | 1. 被關閉的 TabPage，該顯示 Buffer 只是隱藏。 |

> 可以使用「`,b`」來觀看「Buffer 列表」。

> 可以對照上面「`,x`」和「`,c`」以及「`,h`」的功能。

#### 存檔

| 按鍵 | 對應 | 說明 |
| --- | --- | --- |
| `,s` | :w | 目前視窗顯示的Buffer存檔 |

其他的存檔功能，目前我是直接下指令，例如「`:saveas `」或「`:w `」。


## 其他對應

還有其他的對應，暫時還沒寫說明文件，請先參考「[原始碼](https://github.com/samwhelp/tool-svim-core/blob/master/plugin/Svim.vim#L753)」。
