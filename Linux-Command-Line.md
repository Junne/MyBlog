title: "Linux Command Line"
date: 2015-08-27 09:25:45
tags: linux
---

常用的Linux命令:   

Tab键用来补全命令.  
Ctrl+C退出当前操作.   
pwd显示当前目录.  
mkdir+目录名,新建文件夹.  
rmdir+目录名,删除空的文件夹.  


Vim使用:  
三种模式: 命令模式、插入模式、编辑模式.用Esc或i来切换.  
  
* set number  显示行号  
* set nonumber 隐藏行号  
* /abc 查找abc 按n跳到下一个，shift+n上一个  
* i在当前位置插入  
* I在当前行首插入  
* A在当前行尾插入  
* o在当前行之后插入一行  
* O在当前行之前插入一行  
* ?abc 查找abc反向查找  
* set ignorecase 忽略大小写查找  
* set noignorecase 不忽略大小写查找  
* set hlsearch 高亮显示搜索结果  
* set nohlsearch 关闭高亮搜索显示  
* ra 将光标所在字符替换成a  
* s/old/new 替换当前行第一个匹配,old换为new  
* s/old/new/g 替换当前行所有匹配  
* %s/old/new 替换所有行第一个匹配  
* %s/old/new/g 替换整个文件的所有匹配  
* 1,3 s/^/  /g 第一、三行每行前面加两个空格  
* kjhl 上下左右移动 前面可加行数 移动行数  
* w向后移一个单词,位于单词首字母 前面可加数字   
* b向前移动一个单词  前面可加数字  
* e同w,光标在单词末尾  
* ge同b,光标在词尾  
* ^移动到本行第一个非空白字符处  
* 0移动到本行第一个字符上  
* $移动到行尾 前面可加数字  
* gg移动到文件头  
* G移动到文件尾  
* f+字符 移动到光标后第一个为该字符的位置 5fa跳到第五个为a的位置   
* F同f反向查找  
* :行数 跳到指定行  
* 行号+G 跳到该行  
* Ctrl+e 向下滚动一行  
* Ctrl+y 向上滚动一行 
* Ctrl+d 向下滚动半屏  
* Ctrl+u 向上滚动半屏  
* Ctrl+f 向下滚动一屏  
* Ctrl+b 向上滚动一屏  
* u 撤销  
* U 对整行撤销  
* Ctrl+r 重做  
* x删除当前字符  
* 4x删除当前光标后4个字符  
* X删除当前字符的前一个字符 dh  
* dl 相当于x   
* dh 同X    
* dd 删除当前行  
* dj 删除下一行  
* dk 删除下一行  
* 10d 删除当前行开始的10行  
* D删除当前字符到行尾  
* d$ 删除当前字符之后的所有字符，当前行  
* jdG 删除当前行之后所有行  
* :1,10d 删除1-10行  
* :2,$d 删除第2行后所有行  


[文章来源](http://www.cnblogs.com/softwaretesting/archive/2011/07/12/2104435.html)   