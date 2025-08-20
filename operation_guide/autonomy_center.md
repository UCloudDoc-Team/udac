# 自治中心

自治中心支持自动SQL限流与异常SQL KILL功能。配置并开启自动限流服务后，当大量SQL并发或当SQL消耗大量CPU资源时，系统会自动检测，当满足触发条件时，自动触发SQL限流和异常SQL KILL任务，解决数据库异常问题。

## 注意事项

* 目前仅支持MySQL 5.7.41版本
* 数据库实例要开启performance_schema后，才可以正常使用限流功能。开启performance_schema需要重启数据库。

## 进入自治中心

在“实例管理”页面，点击数据库名称，打开页面后点击“自治中心”，进入自治中心页面。

![image](/images/enter_autonomy_center.png)

![image](/images/autonomy_center_page.png)

## 自动限流简介

当触发自动限流之后，会启动一个自动限流事件，在该事件中，会发起自动限流的任务。任务分为KILL任务和限流任务两种，KILL任务作用是终止某条异常SQL，限流任务的作用是限流异常SQL。

一个限流事件中可以发起多个限流任务。

## 开启自动限流

点击右上方的“修改”按钮进行自动限流功能的开启和关闭操作

![image](/images/start_throttle_step_one.png)

![image](/images/start_throttle_step_two.png)

![image](/images/start_throttle_step_three.png)

![image](/images/start_throttle_step_four.png)

## 配置自动限流策略

![image](/images/config_throttle.png)

* 设置阈值触发的条件
  * CPU使用率及活跃会话数：设置CPU使用率和数据库活跃会话数的阈值，支持并且和或者为判断原则。
  * 触发条件：当满足CPU使用率及活跃会话数中设置的阈值及判断原则，且持续发生时间超过设置的时长，则触发自动限流。
  * 在限流事件中的所有任务执行完毕且等待设置的时长后，如果数据库实例的CPU使用率和活跃会话书不满足阈值，事件将会自动终止。

* 任务持续时间
  * 发起自动限流的任务后，任务的持续时间。

* KILL异常SQL
  * 选择是否开启异常SQL KILL
  * 开启后，当触发自动限流时，会终止正在执行的异常SQL。

* 可限流时间段
  * 只有在可限流时间段内，才会触发自动限流，该时间段之外不会触发限流。  

* 注意事项
  * 修改策略将会终止正在进行的事件与任务
  * 正在进行中的限流事件，在超出可限流时间段后，会自动终止。
  * 正在进行中的限流事件和限流任务可手动终止。

## 事件及任务详情

![image](/images/throttle_event.png)

![image](/images/throttle_task.png)

* 会话快照
  * 在触发限流的时候，会抓取information_schema.PROCESSLIST中的信息作为快照。

* 监控参考
  * 该任务限流期间的CPU使用率、活跃会话数、TPS、QPS信息

* SQL执行记录
  * 该任务限流期间，拒绝执行的SQL的记录。

* InnoDB快照
  * 触发限流的时候，InnoDB的实时运行快照。

## 触发限流的通知

触发限流发出通知，需要进入USNS服务进行设置。

![image](/images/enter_usns.png)

![image](/images/usns_auto_event.png)

![image](/images/usns_auto_event_set.png)

具体配置细节见[USNS产品文档](https://docs.ucloud.cn/umon/guide/message)

* 注意事项：
  * 一定要选择“UDAC 自治事件通知”设置通知对象