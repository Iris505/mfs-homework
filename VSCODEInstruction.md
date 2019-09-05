# Visual Studio Code常用功能说明
Visual Studio Code是一个轻量级但是十分强大的源代码编辑器，重要的是它在Windows, OS X 和Linux操作系统的桌面上均可运行。Visual Studio Code内置了对JavaScript, TypeScript和Node.js语言的支持，并且为其他语言如C++, C#, Python, PHP等提供了丰富的扩展库。
## 快捷键说明
>### 主命令框
F1 或 Ctrl+Shift+P : 打开命令面板。在打开的输入框内，可以输入任何命令，例如：
* 按一下 Backspace 会进入到 Ctrl+P 模式
* 在 Ctrl+P 下输入 > 可以进入 Ctrl+Shift+P 模式
* 在 Ctrl+P 窗口下还可以:

  -直接输入文件名，跳转到文件
   - ? 列出当前可执行的动作
   - ! 显示 Errors或 Warnings，也可以 Ctrl+Shift+M
   - : 跳转到行数，也可以 Ctrl+G 直接进入
   - @ 跳转到 symbol（搜索变量或者函数），也可以 Ctrl+Shift+O 直接进入
   - @ 根据分类跳转 symbol，查找属性或函数，也可以 Ctrl+Shift+O 后输入:进入
>### 常用快捷键
#### 编辑器与窗口管理
* 打开一个新窗口： Ctrl+Shift+N
* 关闭窗口： Ctrl+Shift+W
* 同时打开多个编辑器（查看多个文件）
* 新建文件 Ctrl+N
* 文件之间切换 Ctrl+Tab
* 切出一个新的编辑器（最多 3 个） Ctrl+\，也可以按住 Ctrl 鼠标点击 Explorer 里的文件名
* 左中右 3 个编辑器的快捷键 Ctrl+1 Ctrl+2 Ctrl+3
* 3 个编辑器之间循环切换 Ctrl+ `
* 编辑器换位置， Ctrl+k然后按 Left或 Right
#### 代码编辑
##### 格式调整
* 代码行缩进: Ctrl+[ 、 Ctrl+]
* Ctrl+C 、 Ctrl+V 复制或剪切当前行/当前选中内容
* 代码格式化： Shift+Alt+F，或 Ctrl+Shift+P 后输入 format code
* 上下移动一行： Alt+Up 或 Alt+Down
* 向上向下复制一行： Shift+Alt+Up 或 Shift+Alt+Down
* 在当前行下边插入一行: Ctrl+Enter
* 在当前行上方插入一行 Ctrl+Shift+Enter
* 根据名字查找 symbol，也可以 Ctrl+T
##### 光标相关
* 移动到行首： Home
* 移动到行尾： End
* 移动到文件结尾： Ctrl+End
* 移动到文件开头： Ctrl+Home
* 移动到定义处： F12
* 定义处缩略图：只看一眼而不跳转过去 Alt+F12
* 移动到后半个括号： Ctrl+Shift+]
* 选择从光标到行尾： Shift+End
* 选择从行首到光标处： Shift+Home
* 删除光标右侧的所有字： Ctrl+Delete
* 扩展/缩小选取范围： Shift+Alt+Left 和 Shift+Alt+Right
* 多行编辑(列编辑)：Alt+Shift+鼠标左键， Ctrl+Alt+Down/Up
* 同时选中所有匹配： Ctrl+Shift+L
* Ctrl+D 下一个匹配的也被选中 (在 sublime 中是删除当前行，*后面自定义快键键中，设置与 Ctrl+Shift+K 互换了)
* 回退上一个光标操作： Ctrl+U
* 选中所有匹配词批量编辑：鼠标高亮选中需要查找的词，按下 Ctrl + Shift + L键，即可快速选中当前文件中所有匹配的词，并在每一个词后面有一个编辑光标，可批量同步编辑
* 折叠所有区域代码 Ctrl+K Ctrl+0(零)
* 展开所有区域代码 Ctrl+K Ctrl+J
* 打开当前文件所在目录 Ctrl+K R
##### 重构代码
* 找到所有的引用： Shift+F12
* 同时修改本文件中所有匹配的： Ctrl+F12
* 重命名：比如要修改一个方法名，可以选中后按 F2，输入新名字，回车，则所有该方法的引用也都同步更新了
* 跳转到下一个 Error 或 Warning：当有多个错误时可以按 F8 逐个跳转
* 查看 diff： 在 explorer 里选择文件右键 Set file tocompare，然后需要对比的文件上右键选择 Compare with file_name_you_chose
##### 查找替换
* 查找 Ctrl+F
* 查找替换 Ctrl+H
* 整个文件夹中查找 Ctrl+Shift+F
##### 显示相关
* 全屏：F11
* zoomIn/zoomOut：Ctrl +/-
* 侧边栏显/隐： Ctrl+B
* 显示资源管理器 Ctrl+Shift+E
* 显示搜索 Ctrl+Shift+F
* 显示 Git Ctrl+Shift+G
* 显示 Debug Ctrl+Shift+D
* 显示 Output Ctrl+Shift+U
##### 其他
自动保存：File -> AutoSave，或者 Ctrl+Shift+P，输入 auto
>### 修改默认快捷键
* 打开默认键盘快捷方式设置：File -> Preferences -> Keyboard Shortcuts，或者：Alt+F -> p -> k
* 修改 keybindings.json：
```json
// Place your key bindings in this file to overwrite the defaults
[
    // ctrl+space 被切换输入法快捷键占用
    {
        "key": "ctrl+alt+space",
        "command": "editor.action.triggerSuggest",
        "when": "editorTextFocus"
    },
    // ctrl+d 删除一行
    {
        "key": "ctrl+d",
        "command": "editor.action.deleteLines",
        "when": "editorTextFocus"
    },
    // 与删除一行的快捷键互换
    {
        "key": "ctrl+shift+k",
        "command": "editor.action.addSelectionToNextFindMatch",
        "when": "editorFocus"
    },
    // ctrl+shift+/多行注释
    {
        "key":"ctrl+shift+/",
        "command": "editor.action.blockComment",
        "when": "editorTextFocus"
    },
    // 定制与 sublime 相同的大小写转换快捷键，需安装 TextTransform 插件
    {
        "key": "ctrl+k ctrl+u",
        "command": "uppercase",
        "when": "editorTextFocus"
    },
    {
        "key": "ctrl+k ctrl+l",
        "command": "lowercase",
        "when": "editorTextFocus"
    }
]
```
## 插件安装卸载
### 安装
点击下图中的<font color=red>红色按钮</font>，然后在输入框输入自己想要安装的插件名然后点击绿色<font color=#008000>安装（install）</font>按钮，安装完成后点击重新加载就可以了。
<img src = "https://work.mafengshe.com/static/upload/article/pic1567684730928.jpg" width="280" height="350">
### 卸载
点击下载图中蓝色的<font color=#005AB5>卸载（Uninstall）</font>按钮，就可以成功卸载安装的软件了。
![卸载](https://work.mafengshe.com/static/upload/article/pic1567684375161.jpg)
### 一些推荐插件
#### 1、Chinese Language
简体中文汉化插件，和我一样英文不好的童鞋可以安装这个插件进行汉化。这个插件重载之后还没有汉化成功的话，把编辑器关闭重新打开就行了。
#### 2、vscode-icons
让 vscode 资源树目录加上图标，有利于我们进行文件格式的判断。
#### 3、HTML Snippets
很实用的 HTML 代码提示插件。
#### 4、HTML CSS Support
HTML 标签上写class 智能提示当前项目所支持的样式。
#### 5、jQuery Code Snippets
jQuery 代码提示，用 jQuery 框架的必须装。
#### 6、Path Intellisense
自动路径补全，方便我们进行图片、CSS、JavaScript等文件的路径编写。
#### 7、Bootstrap 3 Sinnpet
Bootstrap 3 代码提示插件，常用的话需要下载一个。
#### 8、Atuo Rename Tag
修改 html 标签，自动帮你完成尾部闭合标签的同步修改。
#### 9、Bracket Pair Colorizer
给括号设置不同的颜色，有利于括号多的时候进行区分。
#### 10、小程序助手
#### 11、minapp
#### 12、wechat-snippet
这三个都是微信小程序的代码提示及自动补全插件，现在微信小程序这么火怎么可以不下载。
以上这些是个人常用并且感觉非常好用的，还有一些其他的插件，比如
#### 13、HTMLHint
HTML代码检测
#### 14、beautify
格式化代码插件，感觉编辑器自带的就够用了。
#### 15、Document this
js 的注释模板 （注意：新版的vscode已经原生支持,在function上输入/** tab）
#### 16、vscode-fileheader
顶部注释模板，可定义作者、时间等信息，并会自动更新最后修改时间
#### 17、Indent-Rainbow
使得对齐更加具有可读性
#### 18、IntelliSense for CSS class names in HTML
基于你的项目以及通过link标签引用的外部文件，该智能插件提供 HTML 中 CSS class 名字的补全。
#### 19、Trailing Spaces
高亮那些冗余的空格，可以快速删掉
#### 20、lit-html
在 JavaScript/TypeScript 的文件中，如果有使用到 HTML 标记，lit-html 提供语法高亮和相应的补全支持。
#### 21、CSS Peek
可以在 HTML 中通过 CSS id 或则 class 来定位到其定义。
## 在 VSCode 中使用 Git 
### 将代码放到码云
到码云里新建一个仓库，完成后码云会有一个命令教程按上面的来就行了

码云中的使用教程：

```c#
Git 全局设置:
 

git config --global user.name "ASxx" 

git config --global user.email "123456789@qq.com"

 

创建 git 仓库:

 

mkdir wap // 项目在本地的路径

cd wap

git init 

touch README.md 

git add README.md 

git commit -m "first commit" 

git remote add origin https://git.oschina.net/name/package.git  // 远程仓库地址

git push -u origin master
```
已有项目：

 
```c#
cd existing_git_repo

git remote add origin https://git.oschina.net/name/package.git

git push -u origin master
```
> 下面说下详细的本地操作步骤：
### 1、用vs打开你的项目文件夹
![](https://work.mafengshe.com/static/upload/article/pic1567690676164.jpg)
### 2、配置git
　　打开Git Bash输入以下命令

　　如果还没输入全局配置就先把这个全局配置输入上去
```c#
Git 全局设置:

 

git config --global user.name "ASxx" 

git config --global user.email "123456789@qq.com"
　　然后开始做提交代码到码云的配置

cd d:/wamp/www/mall360/wap //首先指定到你的项目目录下

git init

touch README.md

git add README.md

git commit -m "first commit"

git remote add origin https://git.oschina.net/name/package.git   //用你仓库的url

git push -u origin master  //提交到你的仓库
```
正常情况下上面的命令执行完成后，本地文件夹会有一个隐藏的.git文件夹，云端你的仓库里应该会有一个 README.md 文件。
### 3、在vscode中提交代码到仓库
　　回到 VSCode 打开 git工作区 （就是直接VSCode中 file -> open 项目所在文件夹），就会看到所有代码显示在这里

![](https://work.mafengshe.com/static/upload/article/pic1567691020445.jpg)
点击+号，把所有文件提交到暂存区。

然后打开菜单选择--提交已暂存的 ( Commit Staged )

![](https://work.mafengshe.com/static/upload/article/pic1567691045845.jpg)

然后按提示随便在消息框里输入一个消息，再按 ctrl + enter 提交

![](https://work.mafengshe.com/static/upload/article/pic1567691079163.jpg)

然后把所有暂存的代码 push 云端，

![](https://work.mafengshe.com/static/upload/article/pic1567691106062.jpg)

点击后，会弹出让你输入账号密码，把你托管平台的账号密码输入上去就行了。

不出问题的话你整个项目就会提交到云端上了。

在 vs 中每次更新代码都会要输入账号密码，可以配置一下让 GIT 记住密码账号：
```c#
git config --global credential.helper store   //在Git Bash输入这个命令就可以了
```
### 4、同步代码
#### push使用

　　随便打开一个文件，添加一个注释

![](https://work.mafengshe.com/static/upload/article/pic1567691319136.jpg)

可以看到git图标有一个提示，打开git工作区可以看到就是修改的这个文件

![](https://work.mafengshe.com/static/upload/article/pic1567691360012.jpg)

然后点击右侧的+号，把他暂存起来。
再在消息框里输入消息，按 ctrl + enter 提交暂存

![](https://work.mafengshe.com/static/upload/article/pic1567691384633.jpg)

再点击 push 提交，代码就提交到云端了。

![](https://work.mafengshe.com/static/upload/article/pic1567691401021.jpg)

打开 码云就可以看到了。
#### pull使用
比如当你在家里修改了代码提交到云端后，回到公司只需要用 vscode 打开项目点击菜单中的 pull 就可以同步过来了。

<img src = "https://work.mafengshe.com/static/upload/article/pic1567691579227.jpg" width="240" height="600">

### 5、克隆你的项目到本地
　回到家后想修改代码，但是电脑没有文件怎么办呢？  往下看
　　
首先你电脑还是的有 vscode 和  GIT，，然后用 git 把上面那些全局配置再执行一次，如下
```c#
git config --global user.name "ASxx"

git config --global user.email "123456789@qq.com"  

 

git config --global credential.helper store   

 

 

 

#然后打开Git Bash输入以下命令

 

cd d:/test   //指定存放的目录

git clone https://git.oschina.net/name/test.git   //你的仓库地址
```
![](https://work.mafengshe.com/static/upload/article/pic1567691755731.jpg)

下载成功，然后就可以用 vscode 打开项目修改了。修改后提交的步骤还是和上面一样：暂存-提交暂存-push提交到云端就ok了。