

个人用户环境变量 ~/.profile
/usr/share/applications

Ubuntu 安装 fcitx 输入法

https://fcitx-im.org/wiki/Install_(Ubuntu)
sudo add-apt-repository ppa:fcitx-team/nightly 或者 sudo add-apt-repository ppa:fcitx-team/stable
sudo apt-get install fcitx fcitx-googlepinyin
在"系统管理"-"语言支持"里设置"键盘输入系统"为fcitx 或者 im-switch -s fcitx -z default 或者运行 im-switch -c 手动选择默认输入法
在"首选项"-"启动应用程序"添加fcitx,让它开机自启动:
名称: Fcitx
命令: /usr/bin/fcitx -d
注释: Fcitx startup
注意:这种情况下在konsole/kate等kde程序中无法调用fcitx输入法,这是因为ibus-qt4的问题,卸载该包即可.
sudo aptitude remove ibus-qt4
sudo aptitude install fcitx-frontend-qt4 # 这个包我没有安装,fcitx就能在kde程序中使用了.

fcitx默认快捷键
调用输入法: Ctrl+Space
中英文切换: 左Ctrl (我改为左Shift)
翻页:      -和= (我改为,.)
在窗口间共享: 设为"按程序"
修改配置后没有生效则建议重启输入法:先右击状态栏里的fcitx选择退出,然后按Alt+F2运行fcitx -d启动.


