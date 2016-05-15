# NexT
> 精于心，简于形

为Ghost移植的NexT主题，移植自 [NexT for Hexo](https://github.com/iissnan/hexo-theme-next)

不要吐槽我在NexT原主题那里Copy来的句子（逃

##安装
鉴于Ghost在Production运行模式下更改主题的内容是要重启才能生效，所以为了避免修改配置而切换主题，我把NexT的三套样式分成了三个主题，切换主题只需要在后台全局设置中选择即可。

###无Git安装：

点击代码上方的 `Download ZIP`，并把三个子目录（next-mist/，next-muse/，next-pisces/）解压到 `ghost_path/content/themes` 目录下。

###Git安装

进入 `ghost_path/content/themes`，执行

	git clone https://github.com/microud/ghost-theme-next.git
	mv ghost-theme-next/* .
	
然后修改修改自己所需配置，重启Ghost。至于 `ghost-theme-next` 目录删除即可。

##必要配置

需要在 `ghost后台 -> 实验功能 -> 开放 API` 勾选此选项。

影响功能：

- [x] 侧边栏的文章数和标签数不能获取
- [x] 归档页面不能获取文章列表
- [x] 标签页面不能获取标签列表

##配置主题

在 `插入代码（code inject）` 页面的 `{{ghost_head}}` 中插入如下代码（DIV中是JSON文本）

link中的名字和链接任意，显示在侧边栏的链接位置。

参数说明：

- author_name: 显示在网站侧边栏上头像下的那个名字
- duoshuo\_name: 多说的short_name, 用来标识多说所有者的那个东东，如果不填js会弹一会儿alert，不过可以在主题中删掉多说的代码...
- links: 数组，理论上可无限添加，其中的每个元素对应的Json对象由name 和 link两个键值对构成，分别为链接名和地址，要加协议（http/https）
<pre>
	&lt;div id="site-config"&gt;
	{
	    "author_name": "云青陌",
	    "duoshuo_name": "xknow",
	    "links": [
	    {
	        "name": "认知",
	        "link": "http://xknow.net"
	    },
	    {
	        "name": "认知",
	        "link": "http://xknow.net"
	    },
	    {
	        "name": "认知",
	        "link": "http://xknow.net"
	    }
	    ]
	}
	&lt;/div&gt;
</pre>

###阅读数记录

待添加...


###归档页面

需要在Ghost后台添加一个静态页面，并设置url为 `records` 方可启用（archive和archives都是保留字不能使用，别再说我没文化了好伐（哭.）。

###标签页面

需要在Ghost后台添加一个静态页面，并设置url为 `tags` 方可启用。

###关于页面

也是需要在Ghost后台添加url为 `about` 的静态页面。

##待添加功能以及bugs

###待添加功能

- [ ] 搜索功能
- [ ] 添加第三方阅读次数统计插件
- [ ] 添加Muse主题
- [ ] 添加Pisces主题

###bugs

- [ ] tag页面最多只列5篇，考虑改用API实现

##贡献

接受各种形式的贡献，包括不限于提交问题与需求，修复代码。等待您的Pull Request。
