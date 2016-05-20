# Python-crawler-exercise
 小白入坑python之旅，以云课堂上[这门爬虫课](http://study.163.com/course/courseMain.htm?courseId=1002794001)为学习素材
 学习要求是：记录课程学习笔记，完成里面的练习、小作业和结课大作业
 
##第二周才开始用github记录，所以week1的笔记暂时不补充了

###Week2.1
 - pycharm 注释多行代码快捷键  ctrl+/ (我为什么记录这么奇怪的知识点）

 - 连接mongo的库的语法:

    import pymongo
    client = pymongo.MongoClient('localhost',27017)

- 在mongo中筛选函数用for...i..加find，例子：

 >>for i in house_info.find():
    if i['price'] >= 500:
        print(i)

[pymongo 常用语法](http://www.myexception.cn/go/2011934.html)

###week2.2
这节课的任务是是爬取58同城的大规模的数据，工作流（workflow）分为两个：

- 设计爬虫1爬取58同城所有频道的列表页，储存在Mongo里面
- 设计爬虫2爬取每个二手物品的详情页，储存在mongo
- 观察网页看看整个网站有没有什么和别的频道异常的频道，比如二手手机号的频道和别的子频道不一样，我们需要在抓取的列表里删除他；在详情页里有未填写地区的，我们要做个if else函数去判断他；有已经删除过的商品，要判断404页；每个频道的有多少页码，也要判断函数去识别...

否则你就会陷入报错的汪洋大海中。

*难怪说数据的清洗整理是爬虫最繁复的部分*





 


