## 性能趋势

性能趋势页面的监控指标，采集频率为5s/次；前端页面可以开启自动刷新，开启自动刷新后，前端页面的刷新频率为15s/次。

## 进入性能趋势页面

  首先进入“实例管理”界面，侧边栏选择 "MongoDB"， 然后选择需要分析的数据库实例，点击“性能趋势”进入
  性能趋势界面。侧边栏支持对不同的节点进行筛选，以查看对应节点的监控数据。
   ![image](/images/mongodb-perf-1.png)
   ![image](/images/mongodb-perf-2.png)

## 指标筛选

  点击“指标筛选”选择需要展示的监控指标(用户自选/关键指标)，
  ![image](/images/mongodb-perf-3.png)

  选择完成后，界面展示选择的指标数据。

## 指标诊断

  指标诊断功能针对半个小时(30min)的范围内的指标(CPU使用率，内存使用率，IOPS，慢日志数)数据进行健康诊断,
  在性能趋势页面，启用“诊断”，
  ![image](/images/mongodb-perf-4.png)
  
  鼠标拖动选择诊断的时间范围，
  ![image](/images/mongodb-perf-5.png)

  点击“诊断”获取结果(正常，告警，异常3个状态)，
  ![image](/images/mongodb-perf-6.png)

  同时支持“重新诊断”，获取新的诊断结果(正常，告警，异常3个状态)，
  ![image](/images/mongodb-perf-7.png)
  
  诊断完成可以关闭“诊断”，
  ![image](/images/mongodb-perf-8.png)

## 指标联动

   趋势页面，对于数据库实例监控指标数据，在时间纬度上支持“联动”，在界面勾选“联动图标”设置为
   “ON”,
  启用联动后，在页面选择某个时间指标数据，不同监控指标数据在时间纬度上进行联动。
  ![image](/images/mongodb-perf-9.png)

## 性能趋势对比
  趋势页面选择“性能趋势对比”，支持对同一指标在不同时间纬度上的一个对比,
   ![image](/images/mongodb-perf-10.png)
  
  首先筛选需要进行对比的“监控指标”，
  ![image](/images/mongodb-perf-11.png)

  再次选择对比的2个时间，
   ![image](/images/mongodb-perf-12.png)
