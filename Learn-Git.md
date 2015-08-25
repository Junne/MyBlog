title: "Learn Git"
date: 2015-08-19 09:20:42
tags: git
---
Git已然成为很多公司生产力工具之一，很有必要深入了解学习一下.  
由于Xcode已经集成了Git，所以不需要再安装.  
然后你需要设置一下本机的用户名和邮箱来区分不同的使用者:  


```
git config --global user.name "Your name" 
git config --global user.email "youremail@example.com"  
```


创建一个repository：进入你需要创建的目录下输入:  


```
git init  
```

       
查看当前repository的状态:  


```
git status  
```


       
查看有哪些变化:  


```
git diff
```


提交修改:  


```
git add .  
git commit -m "some describe"  
```

 
查看你的commit记录:  


```
git log  
```


也可以在后面加个参数:  


```
git log --pretty=oneline  
```

 
回退到上个commit:  


```
git reset --hard HEAD^  
```

  
回退到指定commit:  


```
git reset --hard fe9a4ddd  
```

 
查看命令记录:  


```
git reflog  
```


丢弃工作区的修改:  


```
git checkout -- somefile
```


撤销暂存区的修改:  


```
git reset HEAD somefile
```



从git中删除某个文件:  


```
git rm somefile
```



从远程库克隆一个本地库:  


```
git clone git@github.com:Junne/MyBlog.git
```


创建分支:  


```
git checkout -b newBranch
```


相当于:   


```
git branch newBranch 
git checkout newBranch
```


查看分支:  


```
git branch
```


切换回主分支后，将newBranch分支合并到主分支:


```
git merge newBranch
```



删除分支:  


```
git branch -d newBranch
```


查看分支合并情况:   


```
git log --graph --pretty=oneline --abbrev-commit
```


阅读资料:  
* [Git教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)  
* [Pro Git](http://git-scm.com/book/zh/v1)  

