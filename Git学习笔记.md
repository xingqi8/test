Git学习笔记(Windows)

1、自报家门
git config --global user.name  XXXXX
git config --global user.email XXXXX

2、自建仓库的初始化
新建要存项目的文件，并在文件夹中右击鼠标打开"Git Bash Here";
初始化仓库命令：
git init

3、具体使用的命令
(1)添加文件到仓库
git add "文件名称"  （注意文件的路径）
(2)提交文件到仓库
git commit -m "对提交的文件进行一个说明介绍"

4、查看当前仓库的状态
git status