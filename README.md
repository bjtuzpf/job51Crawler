# job51Crawler

Crawler for http://www.51job.com/

(网站未找到robots.txt文件，如果有且个人代码有不合适之处，可联系我删除或者修改。)

目标是爬取51job网站的全部职位用于数据分析。

crawlerSpecial:
和特定爬虫有关的参数和函数，目前是和51job这个网站有关的一些参数和函数

data：
爬取的数据，目前主要是51job网站的“地图”--不同区域的名字、区域码以及一个和工作数有关的数字，具体见代码；

rscData:
资源文件夹，目前只有user-agent;代理存储在数据库，代理的维持项目有空会开源；

job51Crawler:

scrapy生成的主文件夹，各文件的作用见scrapy文档。

job_area.py基本完成，分区域保存区域码，方便构造不同区域的工作的url。

job_url.py是用于爬取工作url的爬虫，会很快更新；

保存的是job_id，通过简单的构造可以得到url，保存到数据库中还是建议保存id。

还有一个用于爬取具体工作的爬虫尚未添加。

Proxy和User-Agent部分暂时不介绍，具体可见代码注释。后期有时间再展开。

更多的细节暂时不讨论，因为可能会再变，后期会陆续添加。有需要可看代码注释，较为详细。

有任何建议或者问题请联系我：zperfet007@gmail.com


todo

1数据库添加

2job_num爬虫添加，用于更新每次工作数

如果可以增量爬取，则job_num可省略

3针对具体工作信息的爬虫

4待规范化：日志，注释等


说明：

area_code部分需要手动删除(已处理)

job_ids中是测试得到的北京部分的工作ids，并非全国

