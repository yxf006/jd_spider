# jd_spider

用scrapy框架写的京东爬虫，可以抓取京东商品信息和评论

# 1、目的：
<li>1、爬取京东的商品信息（以电子烟为例）</li>
<li>2、爬取商品的评论信息</li>

#2、抓取到的数据属性如下所示
商品数据
![image](http://img.blog.csdn.net/20160706175045922)

评论数据
![image](http://img.blog.csdn.net/20160706174754513)

#3、使用说明：
##(1)抓取商品信息和抓取评论分别写在了两个不同的爬虫里

<p>抓取商品信息代码在jd_home.py中，数据库在setting.py中修改ITEM_PIPELINES，使用MySQLPipeline</p>
<p>抓取评论代码在jd_comment.py中，数据库在setting.py中修改ITEM_PIPELINES，使用CommentPipeline</p>

##(2)setting.py文件
<p>默认开启了代理IP，因为IP的存活期的限制，要定期更新PROXIES中IP信息，可从网站：http://www.xicidaili.com/ 中找免费的代理IP</p>

<p>如果不想使用代理IP，可以将DOWNLOADER_MIDDLEWARES代码注释掉</p>

<p>数据库的配置：<p>
<li>setting.py中可以配置数据库的主机，端口，用户名，密码和数据库名信息</li>
<li>pipeline.py中在sql语句中配置你要存入的表的名称。</li>

<br>
<p>更多爬虫的细节可以参考我的博客文章：</p>
<li>http://blog.csdn.net/xiaoquantouer/article/details/51840332</li>

<li>http://blog.csdn.net/xiaoquantouer/article/details/51841016</li>

<br>
##有问题欢迎留言

