# 慢日志分析
  提供对一段时间范围内慢日志数据统计分析。


## 进入慢日志分析
  点击操作界面“慢日志”，进入慢日志分析界面，
  ![image](/images/slowlog-analyze-click.png)
  
  ![image](/images/slowlog-analyze-detail-info.png)
  
  默认会罗列出慢日志统计信息(如果在时间范围内存在数据)，
  ![image](/images/slowlog-analyze-statistics-info.png)

## 样本分析 
  在慢日志统计页面选择一条统计数据，点击右侧“样本分析”，将罗列出选择的时间范围内匹配的慢日志数据中
  执行执行时间最久的慢日志数据做执行计划分析

  ![image](/images/slowlog-analyze-statistics-sample-click.png)
  
  操作后获取到对应的执行计划结果数据，
  ![image](/images/slowlog-analyze-statistics-sample-result.png)

  样本分析界面也支持“重新分析”，获取执行计划结果，
  ![image](/images/slowlog-analyze-statistics-sample-again.png)

## 慢日志明细(统计数据)
  在慢日志统计界面中，可以选择一条统计数据，获取该数据匹配的慢日志明细数据，

  点击右侧“明细”，
  ![image](/images/slowlog-analyze-statistics-sample-detail-click.png)

  将在新弹出的页面展示明细数据。
  ![image](/images/slowlog-analyze-statistics-sample-detail-info.png)


## 慢日志明细(全量数据)
  在慢日志分析界面，能获取选择的时间范围内全量慢日志数据，

  点击右侧“明细”，
  ![image](/images/slowlog-analyze-all-sample-click.png)

  将获取到该对应时间范围的慢日志数据。
  ![image](/images/slowlog-analyze-all-sample-detail-info.png)

  同时慢日志明细中的展示字段，用户可以进行选择，
  ![image](/images/slowlog-analyze-all-sample-detail-info-description-field.png)

  在该界面的右侧支持对数据进行下载，以csv文件格式，
  ![image](/images/slowlog-analyze-all-sample-detail-info-download.png)
  
  ![image](/images/slowlog-analyze-all-sample-detail-info-download-result.png)

## 慢日志统计图联动慢日志信息 
  在慢日志分析界面，点击统计图中的慢日志柱状图，能联动该点击区域的慢日志数据信息，
  ![image](/images/slowlog-analyze-info-linkage.png)
