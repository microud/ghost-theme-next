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

	git clone git@github.com:microud/ghost-theme-next.git .

或者直接执行

	git clone git@github.com:microud/ghost-theme-next.git ghost_path/content/themes
	
然后修改修改自己所需配置，重启Ghost。

##配置主题

###友情链接

打开 `sidebar.hbs` 鼠标拖滚动条直接到底，然后在注释block包裹的区间复制 span 标签并修改即可增删、编辑友情链接，如果是production模式下，需要重启Ghost才能生效。

###多说

待添加...

###阅读数记录

待添加...

##必要配置

###归档页面

需要在Ghost后台添加一个静态页面，并设置url为 `records` 方可启用（archive和archives都是保留字不能使用，别再说我没文化了好伐（哭.）。

###标签页面

需要在Ghost后台添加一个静态页面，并设置url为 `tags` 方可启用。

###关于页面

也是需要在Ghost后台添加url为 `about` 的静态页面。

##待添加功能以及bugs

###待添加功能

- 搜索功能
- 还未设置/tag/页面的样式
- 添加多说评论插件
- 添加第三方阅读次数统计插件
- 添加Muse主题
- 添加Pisces主题

###bugs

- 加载页面在动画前显示内容
- 改一下Pagination的表现方式
- ...

大家有什么好的想法欢迎留issues，如果有大神跟我说一下bugs的解决方案...感激不尽
