# testPyinstaller
学习一下打包，对一些Python程序进行打包练习。

### 安装Pyinstaller

```python
pip install pyinstaller
```

### 命令行执行

```shell
pyinstaller -F E:\youdao\youdaotranslation.py  
```

文件位置是绝对路径

**注意**：当程序用到了自己额外安装的库文件的时候，需要找到那些库文件，和你想打包的py文件放到同一个目录下，确保目录的路径中没有中文。

这个`youdaotranslation.py`，因为用到了`urlib.request`，以及自带的标准库文件，所以就把python安装目录下的C:\Users\Administrator\AppData\Local\Programs\Python\Python36的DLLs文件夹和用到的C:\Users\Administrator\AppData\Local\Programs\Python\Python36\Lib\site-packages目录下的urllib3文件夹全部拷贝到youdao的目录下。

然后在执行上面的打包命令，产生的exe文件在dist文件夹下。

查看`pyinstaller`命令使用帮助

```shell
pyinstaller -h 
```

常用如下：

-F 表示生成单个可执行文件

-w 表示去掉控制台窗口，这在GUI界面时非常有用。不过如果是命令行程序的话那就把这个选项删除吧！

-i 表示可执行文件的图标

### 参考链接

http://www.manongjc.com/article/14130.html