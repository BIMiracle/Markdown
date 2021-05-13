## 软件无法使用

“某些软件的最新版本在 macOS Mojave 10.14 及以上系统会出现报错无法使用的情况，可在终端输入以下代码即可运行：  
sudo codesign –force –deep –sign – 文件位置（直接将应用拖进去即可）  
（注意最后一个 - 与 文件位置 中间有一个 空格）”

## launchpad残留图标

defaults write com.apple.dock ResetLaunchPad -bool true;killall Dock

## 前往桌面

~/desktop
~/桌面

## MacOS 打开原生自带NTFS读写功能1

1. 点击桌面，快捷键shift+command+G打开“前往”，输入/etc，敲回车

2. 复制hosts文件到桌面，把它重命名为fstab  
   右键fstab文件—>打开方式—>文本编辑->写入如下内容
   
   ```
   LABEL=移动硬盘1 none ntfs rw,auto,nobrowse
   ```

3. 把<mark>移动硬盘1</mark>改成自己的硬盘名字

4. command+S保存文件,复制到/etc目录下,输入系统密码

5. shift+command+G打开“前往”,进入/Volume目录,即可看到硬盘,拖动移动硬盘，固定到Finder侧边栏

## MacOS 打开原生自带NTFS读写功能2

 1、首先关闭SIP系统完整性保护  

方法是，重启电脑，按住command+r进入恢复模式，在最上面的实用工具里，打开终端，输入关闭sip的命令  

csrutil disable  

系统会给你一个提示，表示关闭成功。然后重启电脑。  

ps：mac电脑添加了连root用户都无法修改的系统完整性保护，再操作完后，记得开启保护。  

2、官网下载最新版Fuse for MacOS，是个dmg镜像，安装时候3个选项要全部安装。（这是让mac使用第三方挂载工具的一个工具）  

3、为电脑安装homebrew  

安装方法，百度一下homebrew的官网就有，不过网速奇慢无比。  

我这里提供一个方法（联通网络才能打开git）  
在github上搜索homebrew，然后在install分支里，下载install.sh文件。  
（网上的教程都是下载install，现在已经升级了）  
下载完成打开，把里面的下载源改为我们中国清华的源。  
BREW_REPO="https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/brew"  
（新版本不需要更改core，只改一个主源就够了）  

然后用bash安装：  

bash -c ./install.sh  
一会儿就安装完了，速度很快，也不会有网上说的“显示tapping时退出，再到对应目录git一下core……“这些步骤。（升级了，可以直接安装完成，速度很快）  

安装完成后，我安装了gcc编译器，大概300MB的样子。  
brew install gcc  
需要另外安装依赖包，brew会自动替你装好。文件有点大，下载速度2MB/s，可以等一下。  

4、装好后，安装我们的关键模块：ntfs-3g！  

由于我懒得编译了，就直接brew了一个，休息一下。  
brew install ntfs-3g  
需要另外安装gettext编程语言包，大约280MB，耐心等一下。  
安装完成后，会提示你安装的内容和mac自带的BSD包不可以放到一起，会冲突。（原文说会让安装的软件们产生疑惑～）  

不过毕竟我们不是专业搞开发需要天天用，不管他也就是了。默认是分开装的，不会对我们有什么影响。  

5、接下来，我们把根目录改为可读写模式（mac很鸡贼，你关了sip，照样不能用，打开发现是只读模式……）  

sudo mount -uw /  

如果这里不操作这一步，就会提示：Read-only file system  

6、接下来，把原本Mac的mount_ntfs，在/sbin里的软连接给他改个名字备份一下  

（为了保险，我还给他上了个chmod 755）  
sudo mv "/Volumes/Macintosh HD/sbin/mount_ntfs" "/Volumes/Macintosh HD/sbin/mount_ntfs.orig"  
系统很奇怪。按理说，这个命令是可以执行的，但是不知道为什么，用这种方式会提示没有找到该目录或文件。  

于是乎，我改了一下方式。我cd进去sbin，直接给他mv了，很成功。  

sudo mv mount_ntfs mount_ntfs.orig  

7、倒数第二步：把我们安装的ntfs-3g的软连接给他放进/sbin里  
（linux里的名字叫做ntfs-3g，在Mac里是叫做mount_ntfs，名字都直接给你改好了）  

sudo ln -s /usr/local/sbin/mount_ntfs /sbin/mount_ntfs  

操作完成后，插上ntfs的u盘试了一下，相当完美～～  

8、最后一步：开启sip保护。至于根目录读写不用担心，重启一下就失效了。  

csrutil disable  

9、enjoy your life～



## Charles报错Failed to install helper CFErrorDomainLaunchd error 9

1. 打开终端后，输入 `launchctl print-disabled system` 回车后查看com.xk72.charles.ProxyHelper 这一项后面是不是true，若是继续第二步
2. 输入 `sudo launchctl enable system/com.xk72.charles.ProxyHelper`