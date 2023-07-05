
# V2LESS
Make V2EX Beautiful again.

## Get Started

> ### 注意
>  - 如果您在 Firefox 使用，您必須先在 `about:config` 將 `layout.css.has-selector.enabled` 設置為 `true`，否則暗色模式將不能正常工作。
>  - 由於 V2EX 內置的「自定義 CSS」功能限制大小需為 8 KB 以下，因此您修改後有可能需要使用其他方式引入，如瀏覽器插件等。

### 安装
在使用 V2LESS 之前，您必須先安装

- [Git](https://git-scm.com)
- [Node.js](https://nodejs.org)

並使用 npm 安裝以下「全局」依賴：

- less
- less-plugin-clean-css

接著開啟您的終端輸入

```cmd
git clone https://github.com/wuxian425/V2LESS
```

從 GitHub 上克隆 V2LESS 項目，然後就可以開始修改樣式了。

### 項目結構
```
|   package.json                       // Node.js 包信息文件
|   README.md                          // README 文件
|
+---dist
|       v2.css                         // 打包產出文件   
|               
\---src
    |   customize.less                 // 變量調節文件（基本上您只需要編輯此文件）
    |   index.less                     // 用於引入組件的根文件
    |   
    +---components
    |       box.less                   // 基礎容器
    |       button.less                // 按鈕
    |       cell.less                  // 基礎容器內的小容器
    |       count_livid.less           // 首頁文章回覆數計數器
    |       footer.less                // 頁腳
    |       header.less                // 頁首
    |       input.less                 // 輸入框
    |       member_activity.less       // 用戶能量條
    |       page_button.less           // 分頁按鈕
    |       page_content_header.less   // 部分頁面主容器的頭部內容（如設置、收藏等）
    |       search.less                // 搜尋框
    |       select.less                // 下拉選擇
    |       switch.less                // 開關
    |       tab.less                   // Tab 分頁（如首頁主容器頂部等）
    |       tag.less                   // 標籤
    |       topic_button.less          // 文章內容主容器底部功能按鈕欄
    |       
    +---global
    |       background.less            // 背景
    |       font.less                  // 字體
    |       link.less                  // 鏈接
    \
```

## 自定義樣式
本項目所有修改的動作皆在 `customize.less` 中進行。

### 變量
變量後方皆帶有註釋，主要分為兩種：

- 標註「亮」者表示亮色模式
- 標註「暗」者表示暗色模式

### Mixin
前綴標註 Mixin 者是可以自定義樣式的進階功能，可以使用 Less 中大部分的功能。

例如想自定義 `.button.normal` 的樣式，你可以寫成：
```less
.mixin-button () {
	&.normal {
		// 你的樣式代碼
	}
}
```
以此類推。

---
###### 2023 BobYang.
