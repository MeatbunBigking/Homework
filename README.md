# 第六次作业
- 代码：
>install.packages("gcookbook")
WARNING: Rtools is required to build R packages but is not currently installed. Please download and install the appropriate version of Rtools before proceeding:

https://cran.rstudio.com/bin/windows/Rtools/
试开URL’https://cran.rstudio.com/bin/windows/contrib/3.6/gcookbook_2.0.zip'
Content type 'application/zip' length 4012802 bytes (3.8 MB)
downloaded 3.8 MB

package ‘gcookbook’ successfully unpacked and MD5 sums checked

The downloaded binary packages are in
	C:\Users\Lenovo\AppData\Local\Temp\RtmpmIpk9v\downloaded_packages
> library(ggplot2)
错误: package or namespace load failed for ‘ggplot2’ in loadNamespace(i, c(lib.loc, .libPaths()), versionCheck = vI[[i]]):
 不存在叫‘colorspace’这个名字的程辑包
> install.packages("ggplot2")
WARNING: Rtools is required to build R packages but is not currently installed. Please download and install the appropriate version of Rtools before proceeding:

https://cran.rstudio.com/bin/windows/Rtools/
试开URL’https://cran.rstudio.com/bin/windows/contrib/3.6/ggplot2_3.2.1.zip'
Content type 'application/zip' length 3976166 bytes (3.8 MB)
downloaded 3.8 MB

package ‘ggplot2’ successfully unpacked and MD5 sums checked

The downloaded binary packages are in
	C:\Users\Lenovo\AppData\Local\Temp\RtmpmIpk9v\downloaded_packages
> library(ggplot2)
错误: package or namespace load failed for ‘ggplot2’ in loadNamespace(i, c(lib.loc, .libPaths()), versionCheck = vI[[i]]):
 不存在叫‘colorspace’这个名字的程辑包
> install.packages("colorspace")
WARNING: Rtools is required to build R packages but is not currently installed. Please download and install the appropriate version of Rtools before proceeding:

https://cran.rstudio.com/bin/windows/Rtools/
试开URL’https://cran.rstudio.com/bin/windows/contrib/3.6/colorspace_1.4-1.zip'
Content type 'application/zip' length 2550276 bytes (2.4 MB)
downloaded 2.4 MB

package ‘colorspace’ successfully unpacked and MD5 sums checked

The downloaded binary packages are in
	C:\Users\Lenovo\AppData\Local\Temp\RtmpmIpk9v\downloaded_packages
> library(ggplot2)
> setwd("~/")
> data <- read.csv("mennu.csv")
Error in file(file, "rt") : 无法打开链结
此外: Warning message:
In file(file, "rt") : 无法打开文件'mennu.csv': No such file or directory
> data <- read.csv("mennu.csv")
> View(data)
> library(gcookbook)
> ggplot(pg_mean, aes(x = Item, y = weight)) +
+ geom_col()
Error in FUN(X[[i]], ...) : 找不到对象'Item'
> install.packages("tidyverse")
WARNING: Rtools is required to build R packages but is not currently installed. Please download and install the appropriate version of Rtools before proceeding:

https://cran.rstudio.com/bin/windows/Rtools/

  There is a binary version available but the source version is later:

installing the source package ��tidyverse��

试开URL’https://cran.rstudio.com/src/contrib/tidyverse_1.3.0.tar.gz'
Content type 'application/x-gzip' length 712837 bytes (696 KB)
downloaded 696 KB

* installing *source* package 'tidyverse' ...
** 成功将'tidyverse'程序包解包并MD5和检查
** using staged installation
** R
** inst
** byte-compile and prepare package for lazy loading
** help
*** installing help indices
  converting help for package 'tidyverse'
    finding HTML links ... 好了
    tidyverse-package                       html  
    tidyverse_conflicts                     html  
    tidyverse_deps                          html  
    tidyverse_logo                          html  
    tidyverse_packages                      html  
    tidyverse_sitrep                        html  
    tidyverse_update                        html  
*** copying figures
** building package indices
** installing vignettes
** testing if installed package can be loaded from temporary location
** testing if installed package can be loaded from final location
** testing if installed package keeps a record of temporary installation path
* DONE (tidyverse)
Making 'packages.html' ... 好了

The downloaded source packages are in
	‘C:\Users\Lenovo\AppData\Local\Temp\RtmpmIpk9v\downloaded_packages’
> data <- read.csv("mennu.csv")
> data
> library(tidyverse)
Registered S3 methods overwritten by 'dbplyr':
  method         from
  print.tbl_lazy     
  print.tbl_sql      
-- Attaching packages --------------------------------------- tidyverse 1.3.0 --
�� tibble  2.1.3     �� dplyr   0.8.3
�� tidyr   1.0.0     �� stringr 1.4.0
�� readr   1.3.1     �� forcats 0.4.0
�� purrr   0.3.3     
-- Conflicts ------------------------------------------ tidyverse_conflicts() --
x dplyr::filter() masks stats::filter()
x dplyr::lag()    masks stats::lag()
> data <- data %>%
+   pivot_wider(-Item, names_to = "type", values_to = "value")
Error in pivot_wider(., -Item, names_to = "type", values_to = "value") : 
  参数没有用(names_to = "type", values_to = "value")
> data <- data %>%
+   pivot_longerr(-Item, names_to = "type", values_to = "value")
Error in pivot_longerr(., -Item, names_to = "type", values_to = "value") : 
  没有"pivot_longerr"这个函数
> data <- data %>%
+   pivot_longer(-Item, names_to = "type", values_to = "value")
错误: No common type for `Serving.Size` <factor<feac0>> and `Total.Fat` <integer>.
> data <- data %>%
+   pivot_longer(-(1:2), names_to = "type", values_to = "value")
> data
> ggplot(data) + 
+   geom_col(aes(value, type))
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type))
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   facet_grid(
+     ~ Item
+   )
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   facet_grid(~ Item, cols = 1`)
+ ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   facet_grid(~ Item, cols = 1)
+ ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   facet_grid(~ Item, cols = 1)
错误: Incomplete expression: ggplot(data) + 
  geom_col(aes(type, value, fill = type)) + 
  coord_flip() + 
  facet_grid(~ Item, cols = 1)
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   facet_wrap(~ Item)
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   facet_wrap(~ Item, ncol = 1)
> ```{r, fig.height=10}
错误: 不能用零长度变数名
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   facet_wrap(~ Item, ncol = 1)
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   facet_wrap(~ Item, ncol = 1)
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   facet_wrap(~ Item)
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   scale_fill_brewer("Set3")
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   scale_fill_brewer("Set3") + 
+   facet_wrap(~ Item)
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   scale_fill_brewer("Set1") + 
+   facet_wrap(~ Item)
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   scale_fill_brewer("Set2") + 
+   facet_wrap(~ Item)
Error in gsub("\\", "\\\\", s, fixed = TRUE) : 
  input string 1 is invalid in this locale
Error in gsub("\\", "\\\\", s, fixed = TRUE) : 
  input string 1 is invalid in this locale
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   scale_fill_brewer("Pastel2") + 
+   facet_wrap(~ Item)
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   scale_fill_brewer(palette = "Set1") + 
+   facet_wrap(~ Item)
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   scale_fill_brewer(palette = "Set1") + 
+   facet_wrap(~ Item) + 
+   theme_classic()
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   scale_fill_brewer(palette = "Set2") + 
+   facet_wrap(~ Item) + 
+   theme_classic()
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   scale_fill_brewer(palette = "Set3") + 
+   facet_wrap(~ Item) + 
+   theme_classic()
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   scale_fill_brewer(palette = "Accent") + 
+   facet_wrap(~ Item) + 
+   theme_classic()
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   scale_fill_brewer(palette = "Dark2") + 
+   facet_wrap(~ Item) + 
+   theme_classic()
> ggplot(data) + 
+   geom_col(aes(type, value, fill = type)) + 
+   coord_flip() + 
+   scale_fill_brewer(palette = "Set1") + 
+   facet_wrap(~ Item) + 
+   theme_classic()
> data <- read.csv("mennu.csv")
> data <- read.csv( mennu2.csv )
Error in read.table(file = file, header = header, sep = sep, quote = quote,  : 
  找不到对象'mennu2.csv'
> setwd("~/")
> data <- read.csv("mennu2.csv")
> library(ggplot2)
> View(data)
> setwd("~/")
> data <- read.csv("mennu2.csv")
> View(data)
> library(gcookbook)
> ggplot(mennu2, aes(x = Year, y = Amount, colour = supp)) +
+ geom_line()
Error in ggplot(mennu2, aes(x = Year, y = Amount, colour = supp)) : 
  找不到对象'mennu2'
> ggplot(data, aes(x = Year, y = Amount, colour = supp)) +
+ geom_line()
Error in FUN(X[[i]], ...) : 找不到对象'supp'
> ggplot(data, aes(x = Year, y = Amount)) +
+ geom_line()
> +geom_point()
错误: Cannot use `+.gg()` with a single argument. Did you accidentally put + on a new line?
> ggplot(data, aes(x = Year, y = Amount)) +
+ geom_line()
> ggplot(data, aes(x = Year, y = Amount)) +
+ geom_point()
> geom_point()
geom_point: na.rm = FALSE
stat_identity: na.rm = FALSE
position_identity 
> ggplot(data, aes(x = Year, y = Amount)) +
+ geom_line()
> geom_line()+
+ geom_point()
错误: Cannot add ggproto objects together. Did you forget to add this object to a ggplot object?
> ggplot(data, aes(x = Year, y = Amount)) +
+ geom_line()
> ggplot(data, aes(x = Year, y = Amount)) +
+ geom_line()+
+ geom_point()
Error in `Encoding<-`(`*tmp*`, value = "UTF-8") : 需要字符矢量参数
>
![图1](https://github.com/MeatbunBigking/Homework/blob/master/crime%20suspect%20under%2018.png)


＃ 第五次作业
- 题目：《青少年犯罪的背后————不可忽视的心理建设》
- 10月份发生的“大连女童之死”案引发了国内对于未成年人保护和未成年人犯罪行为的又一次大规模讨论。遇害的女童年仅十岁，而凶手更是只有13岁。除了谴责凶手的残忍和思考法律制度问题等常规角度以外，作为以未成年人为事件中心的案件，我认为从凶手的角度出发，可以研究未成年人刑事案件与心理医疗条件的关系。
- 我先从国家数据中找到了2008-2017年青少年刑事案件的数量表，接着通过镝数的线上图表生成工具，制作了该表格的折线统计图。（如下图）
![刑事案件](https://github.com/MeatbunBigking/Homework/blob/master/xingshianjian.jpg)
- 从中我们可以发现，尽管青少年刑事案件从2008年以来整体的数量呈下降趋势，但整体数量仍然很高。其中，在2016-2017年的时间里，嫌疑人不满18岁的刑事案件的占比甚至呈增大趋势。案件整体的数量下降不仅得益于我国在青少年教育工作及法律方面的重视，更与近些年来未成年人口数量不断下降，以及针对未成年人案件“少捕、慎诉、附条件不起诉”的原则有关。2003 年至 2015 年，全国检察机关经审查不批准逮捕未成年犯罪嫌疑人 16 万余人，不捕率为 14.8% ；不起诉 5 万余人，不诉率为 4.4% 。而在 2017 年前 11 个月，全国对未成年犯罪嫌疑人不捕、不诉率已上升至 33.4% 和 18.4% （数据来源：最高检）。
- 心理健康与青少年犯罪的关系引发过长久且大规模的讨论。一般而言，关注青少年心理健康与否和青少年的犯罪行为数量存在一定关系。通过世界卫生组织官网提供的数据，我利用Tableau制作出了截止2017年世界各国心理医疗设施的配备情况图（见链接）。从中我们可以看出，对比世界其他发达国家，我国作为一个人口基数较大的国家，心理医疗设施并不完备。
<https://public.tableau.com/profile/li.jia.hao#!/vizhome/13372/1?publish=yes>
- 尽管通过研究心理设施分布的角度并不能直接影响未成年人保护和未成年人犯罪等相关问题的解决，也不能直接控制犯罪行为的发生频率，但是心理健康关注的不足，多少也算是引发犯罪的原因之一。通过这一角度，希望可以引起读者的重视，对青少年犯罪行为防患于未然，及时关注心理健康。
- 使用工具：Tableau、镝数
- 数据来源：国家数据、《司法大数据专题报告》、世界卫生组织
- 存在问题：许多有关未成年人犯罪的报道均属于禁区，获得详细的数据非常困难。

＃ 第四次作业
- 题目：《“麦辣鸡腿堡”的包装进化史》
- 在大城市面对垃圾分类问题纷纷跃跃欲试的同时，以麦当劳为首的国际快餐品牌也在餐厅里开始着食品包装垃圾的分类。在北京的麦当劳餐厅，按照包装材质分类的垃圾桶已经投入了使用。抛开尚未开始实施的大规模全民垃圾分类政策，麦当劳产品中的食物包装问题同样引发了消费者的好奇心。

![麦辣鸡腿堡](https://github.com/MeatbunBigking/Homework/blob/master/mailajituibao.jpg)
- 在这幅图片中，我通过Kaggle和麦当劳官网两个平台得到了数据。首先我介绍了北京目前的麦当劳门店数量情况，其次根据官网给出的“麦辣鸡腿堡每秒钟销售四个”的数据，自行计算得出了北京地区麦当劳每小时卖出的麦辣鸡腿堡数量，进而可以基本得出“一小时内北京地区麦当劳售卖的麦辣鸡腿堡”产生的汉堡包装纸数量。其次，在图片的下半部分，我通过查阅好奇心日报、麦当劳官网的数据和资料，了解到了中国麦当劳在汉堡包装材料上的变化情况，用图片更直观地体现了出来。从中我们可以看到，虽然每天麦当劳的食物包装产生的垃圾很多，但商家在包装的改良上依然费尽心思，不断推陈出新。
- 食物包装所产生的垃圾算是垃圾的一种，然而既然是广义的“垃圾”二字，被人戏称“垃圾食品”的，以麦当劳为代表的西式快餐产品也可以作为“垃圾”的一个新的角度。我从Kaggle上选取了麦当劳8种主要汉堡产品的部分营养成分含量，并制作成了条形图，配上汉堡的图例，简单表述出“一个汉堡含有多少脂肪/糖分/热量”的信息，供读者参考。
![ingredients](https://github.com/MeatbunBigking/Homework/blob/master/ingredients%20of%20MCD.jpg)
- 显然，垃圾食品并不止麦当劳这一种，食品包装的垃圾也并不只是麦辣鸡腿堡一样产品所产生的。所以，此次可视化作品仅作为某一种食品包装问题的展示样例，借此以小见大，让读者关注快餐的包装问题和演变的故事。

- 数据来源：好奇心日报、麦当劳官网、Kaggle
- 思路：由“垃圾”二字联想到“垃圾食品”，既分析垃圾食品的包装问题，也扩展到垃圾食品本身的问题。
- 工具：Tableau、Photoshop


# 第三次作业
- 所选数据集：NBA球员卢卡 东契奇的菜鸟赛季数据（from Kaggle）
- 所用工具：镝数、数可视、Excel、Tableau
- 体会：国内的平台注重平台版权————水印等；国外平台格式严谨，且不仅会开发线上平台，更多的是通过css或py文件呈现。同时，国外平台注册大多需要提供单位及职业信息。
![dydata1](https://github.com/MeatbunBigking/Homework/blob/master/dydata1.jpg)
![dydata2](https://github.com/MeatbunBigking/Homework/blob/master/dydata2.jpg)
![shukeshi](https://github.com/MeatbunBigking/Homework/blob/master/shukeshi.jpg)
![tableau](https://github.com/MeatbunBigking/Homework/blob/master/tableau.png)


# 第二次作业

1. 我国关于公共数据开放的法规：

《科学数据管理办法》
《上海市公共数据开放暂行办法》
《政府数据开放准备度报告》
《促进大数据发展行动纲要》
《数据安全管理办法》（征求意见稿）
《北京市公共数据管理办法》（征求意见稿）
《成都市公共数据管理应用规定》


数据平台：
- 国内：
镝数、国家数据、万方数据库

- 国外：
纽约政府开放数据平台
https://opendata.cityofnewyork.us/

United States Census Bureau
https://www.census.gov/
美国人口普查局

Quandl.Com 
https://www.quandl.com/
金融，经济和替代数据集的主要来源，为投资专业人士提供服务。Quandl的平台被超过40万人使用，其中包括来自世界顶级对冲基金，资产管理公司和投资银行的分析师。

Figshare.Com
https://figshare.com/
研究论文上传网站，已有2600万+浏览量、750万+下载、800，000+上传、200万+文章

A Deep Catalog Of Human Genetic Variation
https://www.internationalgenome.org/data
国际基因组样本资源

Google Public Data
https://www.google.com/publicdata/directory
谷歌公开数据搜索网站

World Bank Data
https://data.worldbank.org/
世界银行开放数据搜索网站

NYC Taxi Data
http://chriswhong.github.io/nyctaxi/
纽约出租车数据开放平台

National Climatic Data Center - NOAA
https://www.ncdc.noaa.gov/
美国国家环境信息中心，监测，评估和提供国家气候和历史天气数据和信息

ClimateData.Us 
http://www.climatedata.us/
美国宇航局公布的美国气候数据

2. 季度GDP增速计算

|2012第一季度|106938.5亿元|
|:----:|:----:|
|2012第二季度|118757.4亿元|
|2012第三季度|123917.0亿元|
|2012第四季度|137370.4亿元|
|2013第一季度|115342.5亿元|
|2013第二季度|127743.9亿元|
|2013第三季度|133751.6亿元|
|2013第四季度|147965.2亿元|
|2014第一季度|123850.1亿元|
|2014第二季度|137305.0亿元|
|2014第三季度|143294.9亿元|
|2014第四季度|158668.8亿元|
|2015第一季度|132491.5亿元|
|2015第二季度|146898.4亿元|
|2015第三季度|153127.4亿元|
|2015第四季度|169488.4亿元|
|2016第一季度|160837.9亿元|
|2016第二季度|179089.5亿元|
|2016第三季度|187498.6亿元|
|2016第四季度|204764.2亿元|
|2017第一季度|171852.5亿元|
|2017第二季度|191284.6亿元|
|2017第三季度|200133.4亿元|
|2017第四季度|218393.3亿元|
|2018第一季度|183613.0亿元|
|2018第二季度|204077.2亿元|
|2018第三季度|213043.8亿元|

增速D=（本季度GDP-前一季度GDP）/前一季度GDP*100%
D1=11.05%
D2=4.34%
D3=10.86%
D4=10.76%
D5=4.70%
D6=10.63%
D7=10.86%
D8=4.36%
D9=10.73%
D10=10.87%
D11=4.24%
D12=10.69%
D13=11.35%
D14=4.70%
D15=9.21%
D16=11.31%
D17=4.63%
D18=9.12%
D19=11.15%
D20=4.40%

# 第一次作业
   2017新闻学（数据新闻报道方向）
   李佳昊
   201701133002
   
## 数据说明

本次作业收集了自己一周以来（9.21-9.27）每天三餐主食的种类。

本次作业的数据收集中发现的问题及感想主要是：
1. 收集数据的过程比较繁琐，经常会忘记记录。
2. 若不进行长期的数据收集，无法看出明显的收集意义。
3. 多少会为了数据多样而影响自己的饮食选择。



## 数据表部分

![drawing1](https://github.com/MeatbunBigking/Homework/blob/master/shouhui1.jpg)
![drawing2](https://github.com/MeatbunBigking/Homework/blob/master/shouhui2.jpg)

| 三餐/日期 | 9.21 | 9.22 | 9.23 | 9.24 | 9.25 | 9.26 | 9.27 |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | 
| 早餐 | 饼干 | 面条 | 饼干 | 没吃 | 面条 | 饼干 | 没吃 |
| 午餐 | 米饭 | 米饭 | 米饭 | 面条 | 米饭 | 米饭 | 米饭 |
| 晚餐 | 米饭 | 驴肉火烧 | 米饭 | 米饭 | 米饭 | 饺子 | 米饭 |

- 日常生活中，我进出学校的时间会通过校门口面部识别系统被学校记录；
- 我的位置信息和步数、运动状态会被手机及软件运营商记录；
- 电子产品的使用时间会被电子产品生产商记录；
- 我的消费记录会被手机支付软件、校园卡运维人员记录。
