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
git add ./      将所有文件进行添加，不用一个一个敲文件名称
(2)提交文件到仓库
git commit -m "对提交的文件进行一个说明介绍"

4、查看当前仓库的状态
git status

5、直接将文件提交到仓库
git commit --all -m "添加的一些说明"        （--all表示将所有文件提交到仓库）

6、版本回退相关的命令
git reset --hard head~0      0是回退到上一个版本;1是上上一个以此类推
git reset --hard head^       也可以这样写^符号的数量表示回退的次数与上一个命令类似
利用版本号回退：
git reset --hard （版本号）