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
git reset --hard [版本号]

7、查看命令历史记录
git reflog           //查看以前执行的所有git命令

8、创建分支，再属于自己的分支上去开发项目
git branch [分支名称]
查看仓库的所有分支以及当前所在的分支：git branch

9、合并分支命令
git merge [分支名称]
eg:假如目前在dev分支上成功完善了一个功能，想要把dev分支的功能更新到master分支：1）首先切换到master分支；2）使用命令：git merge dev即可合并；
注: 1)合并分支是指的是将当前分支与指定的分支进行合并。
    2)合并分支时假如出现冲突，需要去手动处理冲突，处理完成后再进行提交和合并分支即可。

10、分支之间的切换命令
git checkout [分支名称]

11、分支的删除命令
git branch -d [分支名称]

12、远程仓库的运用
GitHub远程仓库的运用，将本地项目发布到GitHub对应的仓库命令：
git Push [GitHub的仓库地址] master    ----将当前分支推送到远程仓库的master分支
eg：git push https://github.com/xingqi8/test.git master 
拉取远程仓库：
git pull [GitHub的仓库地址] master    ----将指定仓库地址的master分支拉取到本地
eg：git pull https://github.com/xingqi8/test.git master
注：拉取之前本地必须初始化一个仓库
克隆远程仓库的命令：
git clone [远程仓库的地址]             ----这会直接将远程仓库的所有数据克隆到本地，一般第一次都会用此命令
eg：git clone https://github.com/xingqi8/test.git   
注：多次执行此命令的话会覆盖本地的数据内容