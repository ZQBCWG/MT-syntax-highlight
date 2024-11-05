# ChangeLog | 变更日志

这里是本项目文件的变更日志，不过由于本项目仓库并不是仅发布某个单独的发行版项目，所以与[通用变更日志](https://common-changelog.org)的规范会有所不同。

> [!IMPORTANT]
> **变更日志特殊规范**
> 版本号前增加文件名作为标题： `文件名 - 版本号 - 更新日`  
> <details>
> <summary>标题合并规范</summary>
>
> 如果某一天进行了多次更新，且为同一类型，则合并至同一个标题下。其下属标题根据情况会产生不同的变化，以下为部分示例：
>
> 仅更新一个语法时：  
> `## 语法 - 日期`  
> `### 版本1`  
> `### 版本2`  
> …
>
> 更新多个语法时：  
> `## 日期`  
> `### 语法 - 版本`  
> …</details>
## 2024-11-5
### Haskell - 1.0.0
#### New | 新语法

+ 新增语法高亮：[GoLang(冷色调)](mtsx/haskell.mtsx)
___
## 2024-10-28
### dotenv - [1.0.1](https://github.com/guobao2333/MT-syntax-highlight/commit/30140d2)
#### Fixed | 修复

1. 修复了未正确高亮的注释

### GoLang Ice - [1.0.0](https://github.com/guobao2333/MT-syntax-highlight/commit/fcfbc92)
#### New | 新语法

感谢该语法的贡献者：**[@Love-Kogasa](https://github.com/Love-Kogasa)**

+ 新增语法高亮：[GoLang(冷色调)](mtsx/golang.mtsx)

虽然已有内置golang语法，但此语法高亮作者写了一个冷色调的配色以及匹配模式，不过只有亮色，而我为此语法补充了暗色的风格。

___
## gitignore - [1.2.4](https://github.com/guobao2333/MT-syntax-highlight/commit/9ab909d) - 2024-10-15
### Fixed | 修复

1. 使后缀只会在匹配为文件时高亮

### Added | 新增

+ 为 `.dockerignore` 文件提供高亮

___
## JavaScript (内置) - [1.1.0](https://github.com/guobao2333/MT-syntax-highlight/commit/39b8409) - 2024-9-21
### Added | 新增

+ 为部分符号/关键字/方法增加高亮
  但是由于存在一些bug，所以仅添加小部分高亮

___
## 2024-9-19
### gitignore - [1.2.3](https://github.com/guobao2333/MT-syntax-highlight/commit/ecdac20) & dotenv - [1.0.1](https://github.com/guobao2333/MT-syntax-highlight/commit/2f99ad9)
#### Added | 新增

+ 新增指定语法支持的最低MT版本
+ 新增支持快捷注释

### JavaScript (内置) - [1.0.1](https://github.com/guobao2333/MT-syntax-highlight/compare/40d8dea...cbf4404)
#### Fixed | 修复

1. 修复因MDN文档导致高亮的语法错误的~~语法错误~~拼写错误：`SynatxError` -> `SyntaxError`

### Added | 新增

+ 为语法添加了预览图

___
## JavaScript (内置) - [1.0.0](https://github.com/guobao2333/MT-syntax-highlight/commit/f177cd7) - 2024-9-2
### New | 新语法

+ 新增内置语法高亮：[JavaScript](mtsx/builtin/JavaScript.mtsx)

**优化内容：**
1. 为error类型添加高亮
2. 为部分全局属性添加高亮

___
## dotenv - [1.0.0](https://github.com/guobao2333/MT-syntax-highlight/commit/b6cdf7b) - 2024-8-31
### New | 新语法

+ 新增语法高亮：[环境变量配置](mtsx/dotenv.mtsx)
  > 5个语法，写了3天😂

___
## github_markdown - [3.2.0](https://github.com/guobao2333/MT-syntax-highlight/commit/1888619) - 2024-8-22
### Added | 新增

+ 为引用块单独添加背景，以匹配github样式
+ 新增html标签高亮(从内置语法扒出来的🤣)

### Changed | 变化

* 调整短代码的配色
* 调整注释语法的实现(合并到HTML标签)
* 调整了数学公式
- 去掉了引用块的背景渲染

___
## 2024-7-22
### gitignore - [1.2.2](https://github.com/guobao2333/MT-syntax-highlight/commit/5f7ec22)
#### Fixed | 修复

1. 修复上个版本导致的一些后缀不渲染问题  
   但是上个版本要实现的效果就没了……

### gitignore - [1.2.1](https://github.com/guobao2333/MT-syntax-highlight/commit/c432cd3)
#### Fixed | 修复

1. 现在只会高亮文件夹和最后一个文件的后缀

### github_markdown - [3.1.0](https://github.com/guobao2333/MT-syntax-highlight/commit/212151f)
#### Fixed | 修复

1. 修复缩进代码块可能出现的一个错误

#### Changed | 变化

* 优化了数学公式的渲染性能
* 分割线现在可以包含若干空格了
* 调整了代码块和引用块背景色的渲染机制
* 优化了部分配色

#### Removed | 移除

- 移除了所有`lineBackground`属性  
  改为使用性能更好的新语法代替原有实现

___
## github_markdown - [3.0.0](https://github.com/guobao2333/MT-syntax-highlight/commit/0ae9664) - 2024-7-19
**使用`2.16.0`版本新增语法重构了代码！！**
### Fixed | 修复

1. 修复链接中如果嵌套图片，会导致提前结束渲染的问题
2. 修复引用块无法渲染其他语法的问题
3. 修复setext标题的渲染错误
4. 修复代码块背景色的一些渲染错误

### Changed | 变化

* **重构了链接的匹配规则**
* 优化部分配色，使整体更加统一，观感提升~

### Added | 新增

+ 添加了新的字体样式，包括粗体、斜体、下划线等
+ 为部分语法添加了非整行背景颜色
+ 添加了光标旁的括号对高亮

___
## vimscript - [1.0.1](https://github.com/guobao2333/MT-syntax-highlight/commit/ef4551a) - 2024-7-12
### Fixed | 修复

1. 修复冒号命令的渲染错误

#### Changed | 变化

* 文件更名：`vim.mtsx` -> `vimscript.mtsx`

___
## 2024-7-11
### vimscript - [1.0.0](https://github.com/guobao2333/MT-syntax-highlight/commit/b6c0af2)
#### New | 新语法

感谢该语法的贡献者：**[@danicaStarR](https://github.com/danicaStarR)**

+ 新增语法高亮：[vim脚本](mtsx/vim.mtsx)  
  有关vimscript的文档请看这里：[VimScript - VimDoc](https://vimdoc.sourceforge.net/htmldoc/usr_41.html)

### github_markdown - [2.1.2](https://github.com/guobao2333/MT-syntax-highlight/commit/8477c47)
#### Changed | 变化

* 将`title`重命名为`heading`以遵守英文规范
  > 明明都叫标题，title代表整个页面的标题，而heading代表某个部分的标题……我英语不好，在学了在学了😣

___
## gitignore - [1.2.0](https://github.com/guobao2333/MT-syntax-highlight/commit/d7ff1ec) - 2024-7-3
### Fixed | 修复

1. 修复 `?` 前面如果是 `*` 则不会渲染的问题

### Changed | 变化

* 将`包含`语法的 _行_ 背景改为 _文本_ 背景
* 优化配色，观感提升~
* 优化逻辑，性能提升~

### Added | 新增

+ 新增文件后缀渲染

___
## gitignore - 2024-6-25
### [1.1.1](https://github.com/guobao2333/MT-syntax-highlight/commit/ca80ab9)
#### Changed | 变化

* 调整 `包含` 语法的背景色，让其不会影响文字清晰度。

### [1.1.0](https://github.com/guobao2333/MT-syntax-highlight/commit/ca80ab9)
#### Fixed | 修复

1. 通配符 `*` 在多于两个时，现在不会渲染。

#### Changed | 变化

- 移除 `包含` 语法的斜体。  
  不过作为交换，为其添加了背景色。

* 调整配色，观感提升~

___
## gitignore - [1.0.0](https://github.com/guobao2333/MT-syntax-highlight/commit/6299c9a) - 2024-6-24
### New | 新语法

+ 新增语法高亮：[git提交忽略](mtsx/gitignore.mtsx)  
  有关gitignore的文档请看这里：[Git - gitignore Documentation](https://git-scm.com/docs/gitignore)

___
## github_markdown - [2.1.1](https://github.com/guobao2333/MT-syntax-highlight/commit/156ec0c) - 2024-6-8
> [!IMPORTANT]
> 仅适用于MT管理器 `2.16.0` 及以上版本！
### Changed | 变化

* _**改为使用推荐的属性名**_
`color(s)` -> `style(s)`

* _**调整语法名称**_
`GitHub Flavored Markdown` -> ` Markdown(GFM)`

___
## github_markdown - [2.1.0](https://github.com/guobao2333/MT-syntax-highlight/commit/73d9f05) - 2024-5-27
### Added | 新增

+ 新增缩进代码块渲染

### Fixed | 修复

1. 修改短代码逻辑，间接修复了它的所有bug……
  > 现在感觉之前自己想的太复杂了，所以说接下来会吸取教训，先实现功能，而不是先想着优化，这是不对滴🤣

2. 修复了链接先于脚注渲染时，导致的渲染错误

### Changed | 变化

_**调整了历史版本号，使其遵守版本控制规范**_
1. `1.0.5` -> `1.2.0`
2. `1.0.4` -> `1.1.0`

* 调整部分命名，消除歧义
* 将代码块主体从`contains`移动至`defines`

### Refactored | 优化

* 支持了制表符缩进`\t`，而不只有空格
* 调整了部分配色，观感提升~
* 清除了部分无用冗(rǒng)余代码

___
## github_markdown - [2.0.0](https://github.com/guobao2333/MT-syntax-highlight/commit/792634d) - 2024-5-16
**此版本进行了代码重构。**

### Removed | 移除

- 移除了引用的内置匹配器：`#ESCAPED_CHAR#`
  > 根据GFM的解释，`\`只会将ASCII字符转义为普通字符

- 删除了不常见的文件后缀
- 删除了短代码的转义规则

### Changed | 变化

* 将语法列表中显示的名称从`github_markdown`改为`GitHub Flavored Markdown`
* 将部分`match匹配器`移动至`defines`属性块中

* 列表现在能够渲染其他语法(例如脚注)
* 将有/无序列表统一合并为`list`
* 将标题统一合并为`title`
* 将警报提示块和引用块统一合并为`quote`
* 调整部分配色，观感大幅提升~
* 优化代码结构，可读性提升~

### Added | 新增

+ 新增github的脚注渲染
+ 新增github的数学公式渲染
+ 新增`ASCII`字符转义渲染

___
## github_markdown - 2024-5-7
### [1.2.0](https://github.com/guobao2333/MT-syntax-highlight/commit/ddf18a0)
#### Fixed | 修复

1. 修复因上个版本导致的列表前无空格会不渲染

#### Added | 新增

+ 新增github的提示引用块渲染

### [1.1.0](https://github.com/guobao2333/MT-syntax-highlight/commit/39a1506)
#### Changed | 变化

* 如果分割线`<hr/>`上一行也是分割线，现在都将会渲染

#### Added | 新增

+ 新增setext标题渲染

___
## github_markdown - 2024-5-2
### [1.0.3](https://github.com/guobao2333/MT-syntax-highlight/commit/76c1f9a)
#### Fixed | 修复

1. 将上个版本修改处回退至1.0.0版本，以修复上个版本导致的代码块内容不渲染

### [1.0.2](https://github.com/guobao2333/MT-syntax-highlight/commit/f3f0913)
#### Fixed | 修复

1. 修复了上个版本导致的标题渲染失效

### [1.0.1](https://github.com/guobao2333/MT-syntax-highlight/commit/4411307)
#### Fixed | 修复

1. 修复了引用块背景渲染与字体渲染不一致的错误

#### Changed | 变化

* 将预览图调整至 `preview/` 目录下
* 更新和优化了文档

### [1.0.0](https://github.com/guobao2333/MT-syntax-highlight/commit/cf23fc0)

**创建了此项目仓库**👍🏻

#### New | 新语法

+ 新增语法高亮：[github 风格和规范的 markdown](mtsx/github_markdown.mtsx)
  有关GFM的文档请看这里：[GitHub Flavored Markdown Spec](https://github.github.com/gfm)

+ 新增许可证
+ 新增`README.md`说明文档
+ 新增Markdown(GFM)预览图
