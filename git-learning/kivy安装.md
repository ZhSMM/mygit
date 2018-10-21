# Python Kivy 中文教程：安装（Windows）
-----
Kivy 是一套用于跨平台快速应用开发的开源框架，只需编写一套代码，便可运行于各大桌面及移动平台上（包括 Linux, Windows, OS X, Android, iOS, 以及 Raspberry Pi） Kivy 采用 Python 和 Cython  编写，在国外已经十分火爆，受关注程度甚至一度超越了老牌的 Python GUI 工具 PyQt。
## 准备工作
1. 安装最新版本python，并保证pip和wheel为最新；即在cmd命令行窗口输入：`python -m  pip install --upgrade pip wheel setuptools  `
2. 安装kivy依赖，执行以下命令:`python -m pip install docutils pygments pypiwin32 kivy.deps.sdl2 kivy.deps.glew`和`python -m pip install kivy.deps.gstreamer`
## 安装kivy及示例
1. 安装kivy：`python -m pip install kivy`
2. 安装kivy示例：`python -m pip install kivy_examples`
## 验证kivy安装
在 Python IDLE 中，依次输入下面的代码（注意缩进）：
<pre name="code" class="python">
from kivy.app import App
from kivy.uix.button import Button

class TestApp(App):
    def build(self):
        return Button(text='ZhangSong')

TestApp().run()
</pre> 
## 打包kivy
官方指导：[https://kivy.org/doc/stable/guide/packaging-android.html#packaging-your-application-into-apk](https://kivy.org/doc/stable/guide/packaging-android.html#packaging-your-application-into-apk  )  

1. 安装VirtualBox：[https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)；
2. 下载虚拟机：[https://txzone.net/files/torrents/kivy-buildozer-vm-2.0.zip](https://txzone.net/files/torrents/kivy-buildozer-vm-2.0.zip)或kivy官网下载[https://kivy.org/#download](https://kivy.org/#download)；
3. 打开VB并载入下载的虚拟机文件，然后运行，登录密码（kivy）；
4. 进入系统配置环境；
5. 首先我们先在该系统中添加一个共享文件夹，这样可以和windows共享文件，在VB的设备->共享文件夹选项中有配置；
6. 然后我们使用固定分配，在windows下某个路径新建一个文件夹后将其选择为共享文件夹，并选择自动挂载；
7. 在虚拟系统中打开File System，找到共享文件夹，并把复制到共享文件夹的main.py复制到桌面上；
8. 右键打开Teminal，cd到桌面，然后运行buildozer init，会生成buildozer.spec文件；
9. 使用命令gedit buildozer.spec来编辑文件，如果没有gedit可以sudo apt-get install gedit来安装；
10. 基本不用改什么，那个source.dir 需要注意，这是刚刚我们放在桌面上的main.py的路径。然后运行buildozer android_new debug，接着就开始下载很多东西了，例如Android SDK,Android NDK之类，并且是需要访问外网的，自搭梯子。然后在它自动下载配置之后就会在桌面的bin文件夹下面生成了apk文件，可以安装在手机上试一下。然后基本流程大概如此^^，详细可以去官网了解，我就是按照官网的步骤完成的。
11. 最后再推荐一个MIT开发的快速制作安卓app的网站，[http://appinventor.mit.edu/explore/#](http://appinventor.mit.edu/explore/#)