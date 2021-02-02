# dotfiles 
  dotfiles需要rcm插件管理

### 安装` rcm`
1. ##### `Alpine Linux`

  ```
  sudo apk add rcm
  ```

2. ##### `Manjaro`

  ```
  yay -S rcm
  ```

3. ##### `Ubuntu`

  ```
  sudo add-apt-repository ppa:martin-frost/thoughtbot-rcm
  sudo apt-get update
  sudo apt-get install rcm
  ```

### 下载动态files文件爱你
##### 需要先下载dotfiles到`~/.dotfiles`中
  ```
  mkdir ~/.dotfiles && git clone git@github.com:qiuyue77/dotfiles.git ~/.dotfiles
  ```
  
## 使用
### 4个命令

```bash
mkrc – 将文件转换为由 rcm 管理的隐藏文件
lsrc – 列出由 rcm 管理的文件
rcup – 同步由 rcm 管理的隐藏文件
rcdn – 删除 rcm 管理的所有符号链接
```

### 快速使用，以`zsh`为例：

将`.zshrc`文件转换成由`rcm`管理文件,`-t`是将此次文件放到标签文件`zsh`中,`-v`显示详情

```bash
mkrc -v -t zsh ~/.zshrc
```

查看是否转换成功，需要配置`rcrc`文件，且只显示`TAGS`中包含的`tags`和未打标签的文件

```bash
lsrc
```

将`rcm`管理的`zsh`标签文件同步出来

```bash
rcup -v -t zsh
```

删除`rcm`管理的相关符号链接

```bash
rcdn -v -t zsh
```
