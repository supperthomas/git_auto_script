# git_auto_script

第一次使用，需要安装以下软件和路径

## CPPCHECK

 STEP1: [官网](http://cppcheck.net/) 下载安装

STEP2: 环境变量path添加cppcheck路径

STEP3:命令行里面执行cppcheck命令，可以用即可



## ASTYLE

STEP1: [官网](https://sourceforge.net/projects/astyle/) 下载解压

STEP2: 环境变量path添加astyle路径

STEP3:命令行里面执行astyle命令，可以用即可



## formatting

这个是来自https://github.com/mysterywolf/formatting 的自动化脚本

STEP1: 直接clone[git_auto_script](https://github.com/supperthomas/git_auto_script.git)目录

STEP2: 将Windows_exe 添加到path环境变量中

STEP3: 命令行里面执行formatting 可以用即可





## pre-commit安装

将 pre-commit拷贝到`.git/hook` 文件夹下面，以后commit无需操作任何操作就可以直接commit 无需考虑formatting或者格式问题或者静态检查问题



## Linux

Linux 的formatting文件，如果有需要，大伙可以PR一个。