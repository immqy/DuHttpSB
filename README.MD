echo # DuHttpSB >> README.mdgit init
git add README.mdgit commit -m "first commit"
git remote add origin https://github.com/immqy/DuHttpSB.git
git push -u origin master


--push
git remote add origin https://github.com/immqy/DuHttpSB.git
git push -u origin master


在你的github分支上， 你需要保持你的主分支干净， 我说的干净就是没有任何改变，那么你可以在任何时候从你的主分支修建一个分支。每次， 你想提交一个补丁或者一个新特性时，你需要为它新建一个分支，而这个分支无论如何都会从你的主分支复制过来。
       当你要在一个分支做拉请求时， 你也能够继续在其他分支上工作，而且也能够在其它分支上做拉请求。
在你新建一个新分支从主分支上拉下来所有改变之前，你的主分支需要确保是最新的。
       在本地电脑新建一个分支： git branch <新分支名字>
       将新分支发布在github上： git push origin <新分支名字> [*如果边看边做，会出错，请往下看]
       切换到你的新分支: git checkout <新分支名字> [* 事实上切换到其它分支都是这个命令]
       当你想要在你的分支上提交内容，请确保是在你的那个分支上。[* 我的一篇博文上写到了在终端上显示当前分支以及显示当前分支是否做过修改即该分支是否干净]
       查看所有已存在的分支，你可以使用： git branch
它就会有如下显示：
approval_messages
       master
       master_clean
[* '·'代表了你现在所在分支]
       为你的分支加入一个新的远程端： git remote add <远程端名字> <地址>
[* 前文提到出错的地方就是缺少了这一步，如果你在github申请了帐号，可以新建一个仓库，这时就会有一个地址[git@github.com:用户名/项目名.git]， 远程段名字可以随便取，如上文的origin]
       通过提交将所有修改提交到你的分支上： git push origin <远程端分支> [* 原文有点问题，远程端分支一般是与本地分支是对应的，当然你也可以在本地一个分支提交到远程端分支的另一个分支如： git push origin master 提交到远程端的主分支上]
       在本地删除一个分支： git branch -d <本地分支>
      在github远程端删除一个分支： git push origin :<远程端分支>
唯一不同的就是冒号代表了删除


_______________________
对于这个问题，最好的解决方法就是按如下步骤：
1.到根目录下：git add .  ；("."是必须要的)
2.git commit -m "some word"
3.git push -u origin master 



______________________________
可以通过如下命令进行代码合并【注：pull=fetch+merge]
git pull --rebase origin master

