# coupon
这是一个还在进行中的项目。

# 目标
做一个个性化的促销信息的推荐系统。

# 进度
1.爬虫部分的core。√  
2.smzdm网站首页和评论的抓取。√  
3.使用jdk的httpServer提供服务。√  
4.~~建立web端项目，收集用户log。~~ (使用不便)  
5.开发了一个[chrome插件](https://github.com/dpy1123/CouponRecorder)，记录用户在浏览smzdm时的动作。√  
6.使用weka进行后续的数据处理。√  

# 训练集
按照view buy normal dislike分类，数据集不平衡，使用smote或cost-sensitive的方法感觉效果都不是很好；  
暂时按照view buy dislike分类。  
整理好的csv数据集在data目录下  
i148的最好结果是基于属性选择的决策树，正确率82%  
i244的最好结果是朴素贝叶斯，正确率77%

# TODO
1.sysout用log替换掉，否则影响性能。√  
2.提高分类准确度，大致从以下方面入手：  
	1.尽量使样本数达到500-1000.  
	2.title中的文本信息没有有效利用，需要str2wordvertex。  
	3.利用上评论信息。包括数量，正向和负向评论数，等。  
3.增加schedule定时执行。