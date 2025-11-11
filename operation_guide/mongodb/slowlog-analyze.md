# 慢日志分析
  提供对一段时间范围内慢日志数据统计分析。


## 进入慢日志分析
  点击操作界面“慢日志”，进入慢日志分析界面，
  ![image](/images/mongodb-slowlog-1.png)
  ![image](/images/mongodb-slowlog-2.png)
  
  默认会罗列出慢日志统计信息(如果在时间范围内存在数据)，
  ![image](/images/mongodb-slowlog-3.png)

## 慢日志明细(统计数据)
  在慢日志统计界面中，可以选择一条统计数据，获取该数据匹配的慢日志明细数据，

  点击右侧“明细”，
  ![image](/images/mongodb-slowlog-4.png)

  将在新弹出的页面展示明细数据。
  ![image](/images/mongodb-slowlog-5.png)


## 慢日志明细(全量数据)
  在慢日志分析界面，能获取选择的时间范围内全量慢日志数据，

  点击右侧“明细”，
  ![image](/images/mongodb-slowlog-6.png)

  将获取到该对应时间范围的慢日志数据。
  ![image](/images/mongodb-slowlog-7.png)

  同时慢日志明细中的展示字段，用户可以进行选择，
  ![image](/images/mongodb-slowlog-8.png)

  在该界面的右侧支持对数据进行下载，以csv文件格式，
  ![image](/images/mongodb-slowlog-9.png)
  
  ![image](/images/mongodb-slowlog-10.png)

## 慢日志统计图联动慢日志信息
  在慢日志分析界面，点击统计图中的慢日志柱状图，能联动该点击区域的慢日志数据信息，
  ![image](/images/mongodb-slowlog-11.png)
