# 练手项目

## 基金净值计算 2016-4-11

在观察两只基金的净值，但是陆金所的净值计算总是落后一天、非实盘，每次都要手动计算。
打算通过爬去天天基金网来实现自动计算净值。
因为不会爬取JS生成的数据，决定通过requests将整个html代码下载，通过正则表达式找到显示金额的语句，二次处理将数字抓下来，并进行简单计算，得出现在的持仓总额。
已经完成。

## Catan Dice-Roller on CLI

玩卡坦岛的时候，郭老师总是扔出7……
后来郭老师的妹妹也在同一家店买了同一套盗版卡坦岛，玩的时候也发现，总是扔出7……
这盗版卡坦的骰子的品控好严格啊，连瑕疵都一模一样！！

在郁闷的输了一局3人卡坦后，决定写个随机骰子工具，顺便还能玩DnD的时候用上。
呵呵呵呵，再给我来个7试试？？？

## 万能骰子（DND/PathFinder等TRPG适用）
几个月之前写过一个专门用来玩卡坦岛的命令行骰子工具，里面的骰子设定都是写死的，只能选2d6/2d10/3d4这几个，够用，但是不方便，实用性太差。最近入了《Pathfinder基础包》，准备重新开始跑团，看几个跑团QQ群里都有骰子机器人（方便大家开网团的时候投骰子），他们输入『.r 3d6』『.r 4d10』甚至『.r 1d97』这种实际中并不存在的骰子也可以得到值，自由度非常高。于是我计划用Python来实现这种高自由度的骰子。遇到了一些困难，但是都解决了，写程序时候的心得在我的博客里：http://www.aliengu.com/archives/1770

## JPG to PDF
有一批 JPG 图片文件要转换成 PDF 格式，并按顺序排序融合为一个文件。于是写了这个小脚本。
给文件按名称排序时，我遇到一些障碍，文件名虽然是『1.pdf』『2.pdf』『3.pdf』这种格式，但数据类型是 str（非 int），不能直接 sort，要用正则表达式把数字部分摘出来再排序，非常麻烦。搜索了一下，发现一个极方便的第三方包，叫做 natsort，以后排序可以用这个。

## drop_duplicates
帮朋友处理几十万条数据，他 Excel 卡死了没法弄，于是临时学了 pandas，写好后居然 2 秒处理好所有数据……震惊！

