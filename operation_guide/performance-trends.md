## 性能趋势

## 进入性能趋势页面
  首先进入“实例管理”界面，然后选择需要分析的数据库实例，点击“性能趋势”进入
  性能趋势界面。
   ![image](/images/performance-trends-instance-click.png)

   ![image](/images/performance-trends-instance-page.png)

## 指标筛选 
  点击“指标筛选”选择需要展示的监控指标(用户自选/关键指标)，
  ![image](/images/performance-trends-metrics-select.png)

  选择完成后，界面展示选择的指标数据。
  ![image](/images/performance-trends-metrics-select-completed.png)

## 指标诊断
  指标诊断功能针对半个小时(30min)的范围内的指标(CPU使用率，内存使用率，IOPS，慢日志数)数据进行健康诊断,
  在性能趋势页面，启用“诊断”，
  ![image](/images/performance-trends-open-metrics-diagnosis.png)
  
  选择诊断的时间范围，
  ![image](/images/performance-trends-open-metrics-diagnosis-timerange.png)

  点击“诊断”获取结果(正常，告警，异常3个状态)，
  ![image](/images/performance-trends-open-metrics-diagnosis-result.png)

  同时支持“重新诊断”，获取新的诊断结果(正常，告警，异常3个状态)，
  ![image](/images/performance-trends-open-metrics-diagnosis-again.png)
  
  诊断完成可以关闭“诊断”，
  ![image](/images/performance-trends-open-metrics-diagnosis-cancel.png)

## 指标联动
   趋势页面，对于数据库实例监控指标数据，在时间纬度上支持“联动”，在界面勾选“联动图标”设置为
   “ON”,
  ![image](/images/performance-trends-metrics-open-linkage.png)

  启用联动后，在页面选择某个时间指标数据，不同监控指标数据在时间纬度上进行联动。
  ![image](/images/performance-trends-metrics-linkage-select.png)

## 性能趋势对比
  趋势页面选择“性能趋势对比”，支持对统一指标在不同时间纬度上的一个对比,
   ![image](/images/performance-trends-instance-compare-click.png)
  
  首选筛选需要进行对比的“监控指标”，
  ![image](/images/performance-trends-metrics-compare-select.png)

  在次选择对比的2个时间，
   ![image](/images/performance-trends-instance-compare-two-timerange.png)
