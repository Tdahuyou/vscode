# [README.md](./0001.%20region%20注释/README.md)<!-- !======> SEPERATOR <====== -->
# [0001. region 注释](https://github.com/Tdahuyou/vscode/tree/main/0001.%20region%20%E6%B3%A8%E9%87%8A)

<!-- region:toc -->
<!-- endregion:toc -->
- 介绍了 region 注释是什么，有什么作用。
- 介绍了在 vsocde 中编写 region 注释的基本语法。

## 📒 region 注释

- region 注释的格式非常简单，只需要在开始位置加上 region，结束位置加上 endregion 即可。
- region 注释的作用：
  - 如果一个模块中含有的代码量比较多（比如大于 100 行），可以考虑使用区域注释的方式，对代码进行分组，方便阅读。
  - 区域注释的内容可以被折叠，对于那些逻辑已经清晰的代码块或者不那么重要的代码块，都可以使用区域注释进行折叠，这样或许可以更好地集中精力关注核心的代码块。
- 下面以 js 为例：

```js
// #region 描述信息
// ...（这部分是代码）
// #endregion 描述信息
```

![](md-imgs/2024-10-09-22-46-18.png)

# [README.md](./0002.%20固定的标签换行展示/README.md)<!-- !======> SEPERATOR <====== -->
# [0002. 固定的标签换行展示](https://github.com/Tdahuyou/vscode/tree/main/0002.%20%E5%9B%BA%E5%AE%9A%E7%9A%84%E6%A0%87%E7%AD%BE%E6%8D%A2%E8%A1%8C%E5%B1%95%E7%A4%BA)

<!-- region:toc -->
<!-- endregion:toc -->
- 介绍了如何在 vsocde 中，将固定的 tab 和非固定的 tab 换行显示的配置，以及换行显示的应用场景。

## 📒 固定的标签换行展示

- 在配置中，找到 `Wrokbench > Editor: Pinned Tabs On Separate Row`，将其勾选上。这可以让固定的标签展示在非固定标签的上边，可以更方便地管理固定的标签。
  - ![](md-imgs/2024-10-09-22-50-28.png)
- 在阅读一些大型项目的源码时，通常会将一些比较重要的模块设置为固定标签，以防不小心被关闭掉。
- 如果想要将不重要的标签给关闭掉，可以使用快捷键 `cmd k cmd w` （macOS） `ctrl k ctrl w` （windows） 来关闭，这不会对固定标签有影响。
- **拖拽**：将非固定的标签拖到固定标签所在的行，非固定标签就自动转为固定标签。

# [README.md](./0003.%20修改编辑器的字体为%20Fira%20Code/README.md)<!-- !======> SEPERATOR <====== -->
# [0003. 修改编辑器的字体为 Fira Code](https://github.com/Tdahuyou/vscode/tree/main/0003.%20%E4%BF%AE%E6%94%B9%E7%BC%96%E8%BE%91%E5%99%A8%E7%9A%84%E5%AD%97%E4%BD%93%E4%B8%BA%20Fira%20Code)

<!-- region:toc -->
<!-- endregion:toc -->
- 在 Windows 上想要使用 Fira Code 字体时发现没生效，这篇文档记录了如何解决在 VSCode 中配置 Fira Code 的操作流程。
- 该笔记以配置 Fira Code 字体为例来介绍，其它类型的字体文件也可以按照相同的步骤进行配置。

## 🔗 links

- https://github.com/tonsky/FiraCode
  - github firacode
- https://github.com/tonsky/FiraCode/wiki/VS-Code-Instructions
  - firacode wiki
  - 在 VSCode 中安装 Fira Code
- https://github.com/tonsky/FiraCode/wiki/Installing
  - firacode wiki
  - 安装 Fira Code
- https://github.com/tonsky/FiraCode/releases/tag/6.2
  - firacode 下载

## 📒 配置步骤

下面以配置 Fira Code 字体为例。

方式1：临时的配置文件 - 新建一个临时的 .vscode/settings.json 文件，内容如下：

```json
{
  "editor.fontFamily": "'Fira Code'",
  "editor.fontLigatures": true, // 启用连字特性
  "editor.fontSize": 14,
}
```

方式2：通过设置页面配置

`ctrl + ,` 打开 VSCode 设置，搜索 `font family` 找到字体配置输入框，在输入框的最开始位置加上 `'Fira Code'`。

![](md-imgs/2024-10-12-17-19-35.png)

重启 VSCode，如果本地已经安装了 Fira Code 字体，可以通过输入 `!=` 来测试一下，看下最终展示的效果是一个叹号加一个等号，还是展示一个不等号。如果是展示一个不等号，意味着本地已经有 Fira Code 字体了。

## 📒 Windows 设备，查看本地已经安装的字体

- 按 `Win + R` 打开运行对话框。
- 输入 `control` 并按回车键，打开控制面板。

![](md-imgs/2024-10-12-17-22-46.png)

![](md-imgs/2024-10-12-17-23-39.png)

如果没有找到 Fira Code，则需要先安装。

## 📒 Windows - firacode 下载 + 安装步骤

https://github.com/tonsky/FiraCode/releases/tag/6.2

下载 Fira_Code_v6.2.zip

![](md-imgs/2024-10-12-17-41-50.png)

可以安装常规的 Regular 版本。

![](md-imgs/2024-10-12-17-42-27.png)

![](md-imgs/2024-10-12-17-42-43.png)

检查是否安装成功。

![](md-imgs/2024-10-12-17-43-58.png)

如果已经看到了 Fira Code，则说明已经安装成功。接下来就是重启 VSCode，查看最终效果。

## 💻 测试

随便新建一个 1.txt 文件，输入以下内容：

```text
!=
==
===
---
```

最终看到的效果如下。

![](md-imgs/2024-10-12-17-47-55.png)

## 🤖 AI - Windows 设备，如何检查 fira code 是否已经安装？

在 Windows 设备上，你可以通过以下几种方法来检查 Fira Code 字体是否已经安装：

### 方法 1: 使用控制面板
1. **打开控制面板**：
   - 按 `Win + R` 打开运行对话框。
   - 输入 `control` 并按回车键，打开控制面板。
2. **进入字体设置**：
   - 在控制面板中，选择“外观和个性化”。
   - 然后选择“字体”。
3. **查找 Fira Code 字体**：
   - 在字体列表中搜索 `Fira Code`。如果你看到 Fira Code 列表中的字体（如 Fira Code Regular, Fira Code Bold, Fira Code Italic 等），则说明该字体已安装。
### 方法 2: 使用文件资源管理器
1. **打开文件资源管理器**：
   - 按 `Win + E` 打开文件资源管理器。
2. **导航到字体文件夹**：
   - 在地址栏中输入 `C:\Windows\Fonts` 并按回车键。
3. **查找 Fira Code 字体**：
   - 在字体文件夹中搜索 `Fira Code`。如果你看到 Fira Code 的字体文件（如 `FiraCode-Regular.ttf`, `FiraCode-Bold.ttf` 等），则说明该字体已安装。
### 方法 3: 使用命令提示符
1. **打开命令提示符**：
   - 按 `Win + R` 打开运行对话框。
   - 输入 `cmd` 并按回车键，打开命令提示符。
2. **列出已安装的字体**：
   - 输入以下命令并按回车键：
     ```sh
     dir C:\Windows\Fonts\FiraCode*.*
     ```
   - 如果 Fira Code 字体已安装，你会看到相关的字体文件列表。
### 方法 4: 使用 PowerShell
1. **打开 PowerShell**：
   - 按 `Win + X`，然后选择 `Windows PowerShell` 或 `Windows PowerShell (管理员)`。
2. **列出已安装的字体**：
   - 输入以下命令并按回车键：
     ```powershell
     Get-ChildItem -Path "C:\Windows\Fonts" -Filter "FiraCode*.*"
     ```
   - 如果 Fira Code 字体已安装，你会看到相关的字体文件列表。

### 安装 Fira Code 字体
如果发现 Fira Code 字体没有安装，你可以从 [Fira Code GitHub 仓库](https://github.com/tonsky/FiraCode) 下载并安装它。下载完成后，双击字体文件并点击“安装”按钮即可。

### 检查 VSCode 设置
确保你在 VSCode 中正确配置了 Fira Code 字体。你可以在 `settings.json` 文件中添加或修改以下内容：
```json
{
  "editor.fontFamily": "'Fira Code', 'Courier New', monospace",
  "editor.fontLigatures": true // 如果你想启用连字特性
}
```

完成这些步骤后，重启 VSCode 以确保更改生效。如果问题仍然存在，请检查是否有其他设置或扩展影响了字体显示。

# [README.md](./0004.%20配置%20Confirm%20Delete/README.md)<!-- !======> SEPERATOR <====== -->
# [0004. 配置 Confirm Delete](https://github.com/Tdahuyou/vscode/tree/main/0004.%20%E9%85%8D%E7%BD%AE%20Confirm%20Delete)

<!-- region:toc -->
<!-- endregion:toc -->
- 需要知道删除文件时弹出的确认提示框如何配置是否开启。

## 📒 配置 Confirm Delete

- 在 vsocde 中删除文件，默认会弹出确认提示框，若有在 vsocde 中频繁删除文件的需求，可能会勾选【不再询问】，若勾选了，那么接下来每次删除内容的时候，就不会再弹出提示框了。
  - ![](md-imgs/2024-10-27-22-31-09.png)
  - 勾选上【不再询问】之后，如果是 macOS 系统，你只需要按下键盘上的 Del 键即可删除文件或者目录。在有频繁需要删除的内容的情况下，这可能确实提供了便利。但频繁删除文件可能仅仅是你某一时段的需求，后续也许就不再需要了，到时候不小心按下 Del 键的话，就会导致内容被误删了。
    - 虽然大多数时候可以通过 cmd z 撤销删除，找回文件，但有些时候是没法恢复的。
      - 有些时候当你意识到误删了，可能已经不知道应该撤销到之前的第几步了。
      - 编辑器重开，会导致撤销操作失效。
    - 这里写这么多，主要是个人在使用时遇到的问题，不小心删了比较重要的内容，找回的过程很费精力，还不如一开始就不关闭这个确认提示框嘞。
- 问题：如果还想恢复确认提示的话，应该怎么做？
  - 这东西是可以支持配置的，打开【设置】，搜索 delete，找到 Confirm Delete 选项，勾选上确认提示框即可。
  - ![](md-imgs/2024-10-27-22-31-12.png)

# [README.md](./0005.%20lake-editor%20插件/README.md)<!-- !======> SEPERATOR <====== -->
# [0005. lake-editor 插件](https://github.com/Tdahuyou/vscode/tree/main/0005.%20lake-editor%20%E6%8F%92%E4%BB%B6)

- 一款在 vsocde 中编写语雀文档的插件。

## 📒 lake-editor 插件简介

- lake-editor 插件
  - ![](md-imgs/2024-11-17-22-15-01.png)
- 问：lake-editor 有啥用？
  - 官方描述：use yuque editor edit local lake file and lakebook viewer
  - lake-editor 可以让你在本地能够使用语雀可视化编辑器，并且编写的内容能够直接搬运到语雀文档中，不会破坏原有的样式、格式。
- 使用流程：
  - 在 VSCode 中搜索 lake-editor 插件并安装好。
  - 在本地新建一个 .lake 文件，比如 `1.lake`。
  - ![](md-imgs/2024-11-17-22-16-24.png)
- 使用评价：
  - 功能阉割：有很多功能是不支持的，比如插入图片、附件……。
  - 使用场景：如果仅仅是处理一些简单的文本编辑需求，勉强还是可以用一下的。
