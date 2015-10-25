# gitbook 生态圈

> Gitbook 相当于简书和百度文库的电子书生成和资源查找平台，不过比两种功能更加齐全和上手，按现在的发展模式来看已然形成了一个自产自销的社区，是一个不可多得的国外资源（计算机语言类偏多）获取渠道。分为两个大模块：
- **作者编撰模式**
- **读者阅读模式**

##一、认识Gitbook

- 使用markdown进行写作
- 使用git控制版本/轻易找回历史记录
- 全平台支持（除了网页打开，还可以直接生成epub、mobi和pdf格式。）
- 版权归自己所有
- 支持github
- 在线编辑
- 多人协作

###具体的看这两个网站吧，懒得说了：
 
- [*本书介绍如何借助gitbook，用markdown写一本自己的开源电子书*](http://www.open-open.com/lib/view/open1423636400311.html)
- [*gitbook中文解说*](https://wastemobile.gitbooks.io/gitbook-chinese/content/)
- 如果你英文好的话直接去：`HELP` 吧

##二、gitbook和github联动

两种方法

- 直接用github账号登陆直接——点击create a new book——弹出的对话框#第三个选项里就有github
- 如果一开始独立注册的前提下
[点击跳转教程](https://wastemobile.gitbooks.io/gitbook-chinese/content/github/transferring_to_github.html),如果右边栏的github里出现了你的github地址也就成功了。

##三、gitbook和github双推

- 





##四、添加DISQUS评论模块
>这是最考究耐心的，注册了两个账号才添加成功，第一次出现了issue里提到的那个官方显示的一行字错误。第二次重新注册了个账号就可以了。

###装机方法
gitbook中所有添加插件的方法都是更改 `book.json` 文件，也就是在其中键入代码。下面是流程

####1.注册DISQUS
- 注册`disqus`
- 点击右上角的设置中的`Add disqus to site`
- 点击`Start Using ENgage`
- 认真填写你的`Site name`待会会用到
- 找到`Website URL`填写你的github地址

####2.添加/修改 `book.json`
- 首先看看你的gitbook中`files tree`区域中有没有`book.json`没有就新建一个
- 常规的添加plugin流程：打开右上角`设置`旁边的`下拉箭头`——找到`Plugins`点击`find Plugins`——现在你到了gitbook的插件库里，找到`搜索栏`查找关键词`disqus`——[点击进去](https://plugins.gitbook.com/plugin/disqus)把看到的那行代码复制粘贴到刚刚新建的`book.json`中。
      {
          "plugins": ["disqus"],
          "pluginsConfig": {
              "disqus": {
                  "shortName": "XXXXXXX"
              }
           }  
       }
- 把`shortName`后面的“XXXXXXX”替换成你刚刚在disqus写的`Site name`

####3.检查
- 点开gitbook里的`plugins`如果里面有`disqus`
- 预览该gitbook看看是否出现了评论，如果没有出现插件还出现了一行字，那就得重新好好检查检查了。