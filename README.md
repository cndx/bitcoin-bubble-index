# Bitcoin Bubble Index

### @玛雅cndx 对代码fork更新的说明

1、访问 [www.btcie.com/bubble] 查看更新

2、改进点一：优化了下显示界面。

3、改进点二：将原始数据放在同一目录，即original_data文件夹可删除了。

4、自己更新方法：

（1）打开[www.bitinfocharts.com] 各数据页面查看源文件。

（2）将最新数据整理到各对应的.txt文件中，注意最新日期要相同，数据不足地需补充。

（3）安装Python，点击process_data.py文件，若无问题，即可生成新的data.json，即可完成更新。

（4）打开index.htm或原index.html即可，刷新加载data.json。

5、更多交流可微博私信 [www.jdoge.com] 。


### What's this?

This project provides a visualization analysis tool for price bubble of Bitcoin, including basic price information, 60-days accumulative increase, hot keywords index, and bubble index. We accumulated the original data (`2010/07/17` - `2020/03/09`) and put them into `/original_data` folder, and we visualize our analysis result using [echarts][1].

### Datasets

We provide the following dataset:

 - *price.txt:* The bitcoin price in USD per day. 
 - *sentaddr.txt:* Number of unique active addresses per day. 
 - *transaction.txt:* Number of transactions in BTC blockchain per day. 
 - *difficulty.txt:* Average mining difficulty per day. 
 - *gtrend.txt:* Google Trends to "Bitcoin".
 - *tweets.txt:* Tweets per day #Bitcoin.

You can get the lastest data from [bitinfocharts.com][2]

### How to use

Open `index.html` in your browser directly and you will see the following page:

<img src="https://github.com/aksnzhy/bitcoin-bubble-index/blob/master/index.png" width = "800"/>

In `original_data` folder, you can run the command:

```
python process_data.py
```

to get the analysis result, which will be stored in `data.json`.


  [1]: https://github.com/apache/incubator-echarts
  [2]: https://bitinfocharts.com/comparison/bitcoin-transactions.html
