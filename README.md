## [nvm](https://github.com/nvm-sh/nvm)
1. use curl to install nvm
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
```
or wget 
```
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
```

2. 在根目录创建(.bash_profile ｜  ~/.zshrc ｜ ~/.profile文件)。本章以.zshrc为例。
```
touch .zshrc
vim .zshrc
```
在.zshrc文件中添加下面的脚本，以配置nvm环境变量。
```
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh" # This loads nvm
```
保存后，在根目录下输入```source .zshrc```，用以重新执行初始化的文件。

3. 验证nvm是否安装成功。
```
nvm -v
```

## [node](https://nodejs.org/en/)
```
nvm ls-remote // 列出nvm下可以安装的node版本列表
nvm use v10.11.0  // 安装10.11.0版本的node, 该版本下对应的npm为6.4.1。
```

## cnpm
由于npm的服务器部署在国外，有时候下载可能会较慢，推荐使用 nrm来安装cnpm或者tnpm。
```
npm install --global nrm --registry=https://registry.npm.taobao.org
```
## [vscode](https://code.visualstudio.com/)
1. 官网下载安装。
2. 默认快捷键
- 快速打开文件 command + o
- 快速定位文件 command + p
- 分割编辑窗口 command + \
- 关闭当前窗口 command + w
- 隐藏二级菜单 command + b
- 放大 command + =
- 缩小 command + -
- 插入表情 ctrl + command + space
- 列编辑 option + shift 然后使用鼠标点选即可，也算是比较实用
- 跳转行 ctrl + g
- 当前文档里搜索 command + F
- 所有文档里搜索 shift + command + F
  
3. 修改键盘快捷键
```
shift + cmd + p  // 打开keybingds.json文件。
```
keybings.json添加以下配置，以覆盖系统配置。
```
[
    { "key": "cmd+1", "command": "workbench.view.explorer" },
    { "key": "cmd+2", "command": "workbench.view.search" }, 
    { "key": "cmd+3", "command": "workbench.view.scm" }, 
    { "key": "cmd+4", "command": "workbench.view.debug" },
]
```
4. 在path中安装code命令
```
shift ＋ cmd ＋ p 
install code 
```
至此，今后就可在终端下执行```code <filePath fileName>```即可使用vscode打开当前项目。








