# 0003. 修改编辑器的字体

## 📝 summary

在 Windows 上想要使用 Fira Code 字体时发现没生效，这篇文档记录了如何解决在 VSCode 中配置 Fira Code 的操作流程。

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

## 📝 notes - 配置步骤

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

## 📝 notes - Windows 设备，查看本地已经安装的字体

- 按 `Win + R` 打开运行对话框。
- 输入 `control` 并按回车键，打开控制面板。

![](md-imgs/2024-10-12-17-22-46.png)

![](md-imgs/2024-10-12-17-23-39.png)

如果没有找到 Fira Code，则需要先安装。

## 📝 notes - Windows - firacode 下载 + 安装步骤

https://github.com/tonsky/FiraCode/releases/tag/6.2

下载 Fira_Code_v6.2.zip

![](md-imgs/2024-10-12-17-41-50.png)

可以安装常规的 Regular 版本。

![](md-imgs/2024-10-12-17-42-27.png)

![](md-imgs/2024-10-12-17-42-43.png)

检查是否安装成功。

![](md-imgs/2024-10-12-17-43-58.png)

如果已经看到了 Fira Code，则说明已经安装成功。接下来就是重启 VSCode，查看最终效果。

## 💻 demo - 测试

随便新建一个 1.txt 文件，输入以下内容：

```text
!=
==
===
---
```

最终看到的效果如下。

![](md-imgs/2024-10-12-17-47-55.png)

## 🤖 ai - Windows 设备，如何检查 fira code 是否已经安装？

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