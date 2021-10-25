# git_auto_script

## 简介

- 你是否会遇到过忘记使用formatting脚本来整理下代码，导致RTTHREAD PR不通过打回去重新修改？

- 你是否总是忘记整理那些astyle的格式问题，总是提交的代码不够美观？

- 你是否总是有些bug是因为没有经过，导致后面bug一大堆？

来看下这个软件吧，保证对你有一定帮助，而且在做其他项目的时候这个软件包也可以使用。

本软件包通过整合cppcheck（静态编译软件）， astyle(格式化代码)， formatting（RTTHREAD格式整理）

三款软件，将这三款软件整合到git的hook中，让你以后提交代码再也不要担心被CI的formatting检测出问题重新提交了。

本软件一次部署长期有效，只要你的git仓库没有更换，就一直有效。

当然如果有好的建议或者修改，欢迎PR，我们大家一起来维护。

当然也如果有更好的软件或者更好的需求，也欢迎在issue里面提出来。

## 如何使用

第一次使用可能会麻烦一点，不过我觉得这个就是一劳永逸的事情，后面就几乎无感了。

### CPPCHECK

 STEP1: [CPPCHECK官网](http://cppcheck.net/) 下载安装

STEP2: 环境变量path添加cppcheck路径

STEP3:命令行里面执行cppcheck命令，可以用即可

### ASTYLE

STEP1: [ASTYEL官网](https://sourceforge.net/projects/astyle/) 下载解压

STEP2: 环境变量path添加astyle路径

STEP3:命令行里面执行astyle命令，可以用即可

### formatting

这个是来自[formatting.py](https://github.com/mysterywolf/formatting) 的自动化脚本，这边我把这个python脚本整理成exe命令行的形式：



STEP1: 直接clone[git_auto_script](https://github.com/supperthomas/git_auto_script.git)目录

STEP2: 将Windows_exe 文件夹添加到path环境变量中

STEP3: 命令行里面执行formatting 可以用即可

生成exe采用命令(这一步通常不需要操作，如果需要更新的话执行下面操作)

```
pyinstaller --onefile --nowindowed formatting.py
```

### pre-commit安装

将 RTTHREAD_auto/pre-commit拷贝到你的工程的`.git/hook` 文件夹下面，以后commit无需操作任何操作就可以直接commit 无需考虑formatting或者格式问题或者静态检查问题

![image-20211025223018211](images/image-20211025223018211.png)

好了， 一切ready。

这个时候，只要你正常commit，你就会发现，你的代码格式已经经过astyle优化过了，如果代码静态检查有问题，会commit不过，并且提示你需要修改，同时也是经过formatting的修改了。之后再也不用担心PR会有格式上的问题了。

