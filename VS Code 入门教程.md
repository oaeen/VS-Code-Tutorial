---
title: VS Code入门教程
id: 0004v
tags:
  - VSCode
  - 新手向
categories: 教程
date: 2020-02-28 21:20:35
index_img: https://wewing.oss-cn-shanghai.aliyuncs.com/blog/index_0004.png
---

写一下 VS Code 的使用技巧? 

## 0. 为什么选择 VS Code

* 支持编程语言多
* 轻量：打开速度快
* 扩展丰富
* 涵盖应用程序整个生命周期：可以进行代码的编辑/调试/版本控制/发布

## 1. VS Code的安装、使用与美化

### 1.1下载安装

直接官网下载安装即可，[https://code.visualstudio.com/](https://code.visualstudio.com/)，略

### 1.2 设置界面语言为中文(可选)

1. 使用快捷键 `Ctrl Shift P` 输入 `configure display language`，回车， 选择 `install additonal languages... `
2. 在左边弹出的 `extension` 中安装中文包
3. 重复第一步操作，将语言设置为中文

### 1.2 打开项目

* 拖拽

  将项目文件夹直接拖入 VS Code 窗口即可

* 文件(File) 菜单栏

  打开文件夹/打开文件

* code 命令

  * `code 文件夹名称` 打开指定的文件夹
  * `code .` 打开当前目录
  * `code -h` 打开帮助

### 1.3 VSCode的美化

只给出VS Code的官方主题网站: [VS Code Themes](https://vscodethemes.com/) , 在该网站中选择一项自己喜欢的配色, 安装插件即可。



## 2. VS Code界面功能介绍

### 2.1 EXPLORER

* OPEN EDITORS

  常用`Close All Editors` 功能，关闭所有编辑器窗口，快捷键：`Ctrl K + Ctrl W`

* Folders

  * New File (新建文件)
  * New Folder (新建文件夹)
  * Refresh Explorer (刷新文件)
  * Collapse Folders in Explorer (折叠目录)

* OUTLINE (大纲)

  以树形式显示代码结构，方便在代码过长的情况下理解代码和进行代码的跳转和导航。

* TIMELINE



### 2.2 SEARCH

用于进行搜索和替换

* 搜索

  * Match Case (大小写敏感)  Alt C
  * Match Whole Word (单词匹配) 
  * 正则表达式

* 替换

  * preserve case 保留大小写，将替换的内容全部切换为小写

* ...

  * file to include

    包含某种格式的文件

  * file to exclude

    排除某种格式文件



### 2.3 SOURCE CONTROL

使用 Git GUI Tool 进行代码管理

#### 2.3.1 搭建 Git 环境

可参考 [Git使用教程](https://blog.oaeen.com/0003g/)

#### 2.3.2 在项目中启用 Git

* 打开项目文件后，在 SOURCE CONTROL 选择 init.

* 点击 `+` 进行`git add`，跟踪文件

* 输入提交信息后，点击 `√` 或者 使用快捷键 `Ctrl Enter` 进行提交

* 左下角可以选择和新建分支

* 在新分支修改提交完后，可以通过 `Ctrl Shift P` 或 在左下角设置处打开 `Command Palatte`, 搜索 `git merge`命令进行操作

* 如果遇到冲突，可以根据 VS Code 的提示进行修改

* 在 右上角的 `...` 可以查看更多的操作，如`stash` 和 `pop stash`

## 3. VS Code的键盘快捷键操作

暂仅收录 Windows 的快捷键

1. 命令面板:  **F1**或者: **Ctrl+Shift+P** 以下快捷键均可通过命令面板查询: 

   ![](https://wewing.oss-cn-shanghai.aliyuncs.com/blog/20200301213927-757448.png)

2. 界面概览: 

   ![](https://wewing.oss-cn-shanghai.aliyuncs.com/blog/20200323210349-452473.png)

3. 命令行的使用(通过命令行打开通过VS Code打开文件): 暂时用不到, 略过(可使用code --help查询

4. **光标移动:** 

   * **针对单词: Ctrl+← 或  Ctrl+→**
   * **行首: Home键**
   * **行尾: End**
   * **对于代码块(即大括号开头结尾): Ctrl + Shift + \\**  (注意 \方向, 即是Enter键上的\键
   * **文档的第一行或者最后一行: Ctrl+Home / Ctrl+End**
   * **开启下一行: Ctrl + Enter**
   * 开启上一行:  Ctrl + Shift + Enter

5. 代码行移动: Alt + ↑ 或 Alt + ↓

* 代码块移动:  Alt + Shift + ↑ 或 Alt + Shift + ↓ (选中后再进行操作

6. **文本选择:** 相应操作加上Shift键即可, 代码块等未提供快捷键的可以采用**命令面板**或者**自定义快捷键**的操作

7. **删除操作: **

   * **删除行: Ctrl + Shift+ K**
     * **Ctrl + X** 剪切当前行, 可以达到删除的作用
   * **删除上一个单词: Ctrl + BackSpace**

   * **删除光标前后一行: **
     * **Shift+Home+Delete / Shift+End+Delete** 或者
     * 命令面板运行: “删除左侧所有内容” / "删除右侧所有内容"
     * **通过自定义快捷键**
   * 删除光标前后的单词内字符: **Ctrl + Shift + ←  +Delete**   /   **Ctrl + Shift + →  +Delete**

8. **多光标特性:**

   * **在上方/下方添加光标: Ctrl + Alt + ↑ 或 Ctrl + Alt + ↓** 或按住Alt状态下 鼠标单击要添加的行
   * 代码块加光标: 选中后 Shift + Alt + I

9. 文件、符号、代码之间跳转

   * 切换文件: 

     * Ctrl+Tab (按住Ctrl不丢, 多次按Tab键达到切换的目的
     * Ctrl + P  (打开搜索最近打开文件的列表, Enter直接打开, Ctrl + Enter 在新的编辑器窗口打开

   * 跳转到特定行: Ctrl + G

   * 符号 (Symbols) 跳转: **Ctrl + Shift + O** 输入 “:”可将当前文件的所有符号进行分类

   * 部分语言如JavaScript支持多文件符号跳转:  **Ctrl+ T**

   * **定义 (Definition) 和实现 (implementation) 跳转**: 需要语言支持

     跳转到函数定义的位置: F12

     跳转到函数的实现的位置: Ctrl + F12

   * 引用 (Reference) 跳转: Shift + F12

10. **函数参数预览: Ctrl + Shift + Space**

11. **快速修复: Ctrl + .** 

12. **代码规整:** **Shift + Alt + F** (对整篇文章

    Ctrl + K 加 Ctrl + F 对选中部分进行代码规整

    Tips: 可在设置中修改代码风格, C++中修改为使用Google风格, 四字符缩进

![](https://wewing.oss-cn-shanghai.aliyuncs.com/blog/20200301222703-198396.png)

11. **添加注释: Ctrl + /**

12. **代码缩进: **，使用命令面板搜索缩进, 选择 “重新缩进行" 或“重新缩进选中行”

13. **光标处代码折叠:  Ctrl + Shift + [**

14. **光标处代码展开:  Ctrl + Shift + ]**

15. **对变量或函数重命名: 选择变量或函数后 键入F2**

16. **列（框）的选择: Shift + Alt 下拖动鼠标**

17. 消除尾随空格:  Ctrl+K 加 Ctrl+X

   或者在设置中更改, 现在好像已经默认配置好了

18. **打开和关闭侧栏: **Ctrl+B

19. **上移/下移复制行: Shift + Alt + ↑ 或  Shift + Alt + ↓**

20. **选定单词: Ctrl+ D** 多次单击会再次添加相同关键字, 可时间批量修改/删除等

21. **拆分编辑器: Ctrl + \ **

22. **自定义快捷键: **打开命令面板, 搜索**打开键盘快捷方式**即可进行修改和配置. 

23. 几个小功能: 未绑定快捷键, 可在命令面板查询或设置
    * **调换字符的位置**: 命令面板搜索转置游标处的字符
    * **调整字符的大小写: **命令面板里搜索“转换为大写”或 “转换为小写”
    * **合并代码行: **命令面板里搜索合并行
    * **行排序: **命令面板搜索 “按升序排列行” 或者 “按降序排列行” (代码行按照字母序进行重新排序
    * **撤销光标的移动和选择: **Ctrl + U



## 4. VS Code的鼠标操作

### 4.1 文本选择: 

* 文本上: 
  * 单击: 把光标移动到相应的位置
  * 双击: 选中当前光标下的单词
  * 三击: 选中当前这一行代码
  * 四击: 选中整个文档
* 行号: 
  * 单击: 选中该行
  * 在行号上上下移动: 选中多行代码

### 4.2 文本编辑--拖放功能（drag and drop）: 

* 选中文本后拖动移动位置(==剪切, 常见操作
* 按下Ctrl键同时拖放(==复制粘贴

### 4.3 多光标操作

* 按住Alt，鼠标左键点击, 
* Shift + Alt, 鼠标左键下拉, 添加多行光标

### 4.4悬停提示窗口: 

鼠标悬停在上面上时会显示一些信息
按住Ctrl + 左键可以追踪函数, 同时可以使用**Alt + ←** 回退



## 5. VS Code 相关开发环境搭建

### 5.1 C# & .NET Core With VS Code

参考[C# & .NET Core With VS Code Tutorial](https://www.youtube.com/watch?v=a6WPeTG1QEk)

1. 安装 .NET core SDK

   [https://dotnet.microsoft.com/](https://dotnet.microsoft.com/)

2. 搜索并安装 VSC C#插件

3. 打开要编写项目的文件夹

4. 在 VSC 终端中运行命令 `dotnet new console` 新建项目

5. ~~编写代码~~

6. 运行命令 `dotnet run` ，可以看到输出`Hello World!`

![](https://wewing.oss-cn-shanghai.aliyuncs.com/blog/image-20200723203003475.png)