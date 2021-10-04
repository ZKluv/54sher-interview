# 学习历程

---

---

## **声明与承诺：本文本全为个人手写，如有引用会使用引用命令标明**

---

---

## 一，git与github

***1，个人看法***：*git是一个本地文件管理助手，即不需要联网也可以管理本地文件，说白了就是可以看到你修改的某个文件之前的版本，使其不要丢失*   

​                       *而github则是一个需要联网的，可以上传开放文件的，支持git的网站，在这个网站上，经过git的本地上传后，大家都可以看见某个人上传的文件及其之前的版本，同时所有人都可以下载并进行修改之后在上传，最后进行合并，共同完成任务*

​                      所以，git与github是密不可分的，想要完成任务是缺一不可的

***2,过程及经历***：事实上，和大多数人可能不同，我是先了解git再了解github的，因为我开始时以为git和github是一个东西所以我将绝大多数时间和精力花在了git上  先是看了[廖雪峰git教程](https://www.liaoxuefeng.com/wiki/896043488029600)结果很遗憾，我认为他讲的很不清晰，且大多数内容是围绕Linux和mac操作系统展开的，结果就是越看越迷！所以我干脆放弃了文本阅读，转而直接看视频[Git 基础全套完整教程（从入门到精通）](https://www.bilibili.com/video/BV1tf4y1e7yt?p=14)真不愧为b站大学，讲的很清晰，但，一个人讲的终究是片面的，将视频看完后，依然有很多不懂得地方，所以我就看了另一个视频[【尚硅谷】Git与GitHub基础全套完整版教程（快速上手，一套搞定）](https://www.bilibili.com/video/BV1pW411A7a5?p=38&spm_id_from=pageDriver)但是很有意思，由于git的基础语法是用的Linux系统，即git中可以使用git自己的语法也能使用Linux的语法，所以导致一个人用的是Linux的语法，而另一人用的是git自己的语法，所以很多时候笔记要记两种语法，且有时还分不清楚所以经常会看到   cd  ls  pwd  tar  和git init  git log  git add  git commit  git push git pull git rebase master.......同时出现在一起，它们有时的作用是叠加的，很不友好。但秉持着有困难克服困难的原则，在军训结束后，抽出时间恶补并了解了它们的基本用法。

这里分享一下我遇见的几个错误和解决方法：git clone失败，提示fatal: unable to access 'https://github.com/0wuyan0/-.git/': OpenSSL SSL_read: Connection was reset, errno 10054

>感谢博客园岑惜的解决方法：
>
>把原来的指令 
>
>$ git clone https://github.com/cen-xi/express.git
>
>改成
>
>$ git clone git://github.com/cen-xi/express.git
>
>就行

git push失败，提示not....

>感谢csdn用户’歪歪100‘的方案[解决方案](https://blog.csdn.net/weixin_41646716/article/details/82454189

还有git commit使用时的错误，结果是由于没有注册git导致的

还有git pull由于冲突报错

> 感谢csdn用户PreciousLife[idea Git解决冲突 git pull失败解决（好文推荐）](idea Git解决冲突 git pull失败解决（好文推荐）)

还有很多错误由于解决后忘记了就不在这里赘述了

**从这么多错误与解决方案中，我越发认识到程序员之路并不是那么好走的，必须耐下心来，提升英语水平看懂那些报错说的是啥再对症下药，同时要用好百度和g.....**

### 附上学习git和GitHub的代码记录笔记（部分）

 git基本代码

1.git init    初始化（在想要的文件夹中打开git bush）注意：此时会创建.git文件是隐藏的，同时该要管的文件夹中的文件还没有被管理

2  git status    检测文件夹下面的文件状态（标红的还未被管理，标绿的已经被管理了）

3  git add example.html       想要管哪个文件   注意：一定要打.html

4  git add .    管理文件夹中的所有文件（常用）

5  git commit -m  '版本'       生成版本     注意：此时打git status后会发现什么也没有，即已经被gits收集起来生成版本

6  ls -ah  显示隐藏的.git文件

7  git log   查看版本（时间，写的人的昵称和邮箱）

8,touch 文件名加后缀       这是添加文件的命令（仅能在git管理的文件夹下创建）

9,git resst --hard 版本号     回滚，即回到之前的版本   

***备注：版本号就是用7的代码查看后的一长串序列***

如果不小心回滚了想再回滚回来，用git reflog 查看

再用git reset --hard 版本号即可（这里的版本号是短黄颜色的序列）

![git三大区域](https://img2018.cnblogs.com/i-beta/1583235/202002/1583235-20200217204046306-837609872.png)

***根据该图视，可以看出在三大区域间可以任意回滚（命令已在图上）***

10,分支

含义：分支可以在某个版本的基础上进行对该版本的改动，从而不影响主干流程

1  git branch 查看分支

2 git branch 加上分支名称     这是创建分支

3 git checkout 加上分支名称     这是切换到分支（不影响主干）

4 git merge 加上合并的分支名称      这是合并分支的命令（注意：一定要先切换到一个分支，在使用该命令，即谁合并谁）

5 git branch -d 加上分支名称     这是删除分支的命令

***至于实践，我已将这个文档上传到github啦***





## 二，markdown语法与typora

***1,写在前面***：对于我这样的新手，在未接触typora和markdown之前一直在使用记事本和word文档来记笔记，时至今日在我学习了typora和markdown后我依然觉得word的功能强大，他的强大之处在于用户不需要学习一种专门的写作语言，只需要使用鼠标在界面操作即可，极易上手，但其也有致命缺点：繁杂！此时markdown就登场了，虽然它拥有的功能可能不如word且需要掌握一门特定的语法，但，它的语法极其简单，且界面极其简单，看着十分舒适。

***2，学习经历***：因为我先学习的是git和GitHub，在学习过那么多的代码和语法后，markdown的学习简直不要太简单，从下载再到使用学习几乎没碰到什么报错，只有一个：在打开markdownpad2时，会给一个报错，需要转到他的官网去下载一个awesomium_v1.6.6_sdk_win来进行渲染修复（由于是某些不可抗力，下载速度极慢，基本等了3个小时）

> 参考资料：[文字资料](https://www.runoob.com/markdown/md-tutorial.html)
>
> [知乎文字资料](https://www.zhihu.com/question/20409634/answer/90728572)
>
> [b站视频资料](https://www.bilibili.com/video/BV1hJ411X75X?from=search&seid=18385142154540142448&spm_id_from=333.337.0.0)
>
> [b站视频资料2](https://www.bilibili.com/video/BV1Fg411j7CW?from=search&seid=8942837260513806948&spm_id_from=333.337.0.0)

***3，展示成果***

Markdown语法

一，标题

\# 一级标题

\## 二级标题

\### 三级标题

\#### 四级标题

\##### 五级标题

\###### 六级标题

注意:打完井号后一定一定一定要打空格键

二，字体

因为markdown是纯英文的，所以只有使用语法才能实现

在四个*之间打的字是加粗

在两个*之间打的字是倾斜

在六个*之间打的字是斜体加粗

在四个~之间打的字是加删除线的文字

例子

**这是加粗的文字**

*倾斜的文字*

***斜体加粗的文字***

~~加删除线的文字~~

三，引用

一个>后的内容为引用

**备注**

好像引用是可以叠加的，即可以在大的引用下在用小的引用

例子

> 内容1
>
> >内容2
> >
> >>内容3

四，分割线

三个或者三个以上的 - 或者 * 

例子

---

---

六，图片插入

分为两种

一，本地图片

![照片名称]()

直接点文件夹就行了

二，在线/网络图片

![名称](https://pic2.zhimg.com/80/412f50dcbe73ea0051a9bf97bb9db4ac_1440w.jpg?source=1940ef5c)

注:图片源于知乎用户***建国JIANGUOOO***

七，超链接

表达:和图片插入很像，不要感叹号即可

例子:[github](https://github.com/)

八，列表

存在两种:

1无序列表

短横杠”-“加需要写的内容

- 目录一

- 目录二

  

  2，有序列表

​          直接用”数字“后跟”."即可

（1）.目录一

（2）.目录二

九，表格

***注意***：***免费版typora没有表格，或者显示不出来，只有升级到pro时才能显示***

```
|  表头   | 表头  |
|  ----  | ----  |
| 单元格  | 单元格 |
| 单元格  | 单元格 |
```

十，代码块

 三个```再加上语言即可

比如：

```java
//java
```

```python
print("hello world")
```

***备注：由于资料来源不一样，这十个的顺序可能也与正常学习不一，声明：除去代码通用外，其余文字与图片都为手写***

## 3，未来展望

***啊，终于写到这里了，现在是凌晨2：03***

**在写加入程序部后想学习的内容前，我想先说说我为什么会想要加入程序部。**

​        *很多人都说大学，产学研脱节，毕业后找的工作很大一部分都需要重新学习，我不是社会学者，其中的道理我也不是很清楚，但我清楚的知道要在大学里努力与贴近社会，我的所学要与社会发展结合在一起，所以我认为升华工作室程序部是一个极其理想的地方，在这里我可以学习到很多有用的知识，结识很多和我志同道合的人提升自我表达能力。心理学家马斯洛曾提出需求层次结构，他认为“人能将理想与现实结合，超越需要（Transcendence needs）- 一个人的动机是超越个人自我的价值观”    所以我同时认为在这里我能找到自己的价值！*

## 回到主题

如果我能顺利加入程序部，我想学习linux操作系统的基本内容，学习java  python C++这三种最常用的语言，至于框架，很抱歉我之前并未有过了解，但我想程序部的工作内容是小程序的开发和网页的制作，所以能学习一些web前端就更好啦

## 4，总结

谢谢给位学长学姐给我这次机会让我参加二面

### 因为热爱，所以坚守