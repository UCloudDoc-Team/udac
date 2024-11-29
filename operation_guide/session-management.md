## 会话管理
  提供对会话的管理和监控

## 进入会话管理页面
  首先进入“实例管理”界面，然后选择需要监控的数据库实例，点击三个点的按钮，在弹出的菜单中选择“会话管理”进入会话管理界面
  ![image](/images/session-management-instance-click.png)

  ![image](/images/session-management-instance-page.png)

## SQL统计Top10
  点击“SQL统计Top10”
  ![image](/images/session-management-sql-stat-top10.png)

  在“SQL统计Top10”页面对于每条SQL可以点击详情选项
  ![image](/images/session-management-sql-stat-top10-detail.png)

## 会话统计
  点击“会话统计”可以看到当前会话涉及的用户、访问来源及数据库
  ![image](/images/session-management-session-stat-user.png)

  ![image](/images/session-management-session-stat-source.png)

  ![image](/images/session-management-session-stat-db.png)

## 性能监控
  会话管理页面有性能监控面板，可以监控当前数据库的总连接数、活跃连接数、最大连接数、CPU使用率
  ![image](/images/session-management-perf-monitor.png) 

## 会话监控
  会话监控可以根据会话类型、User、Host、DB、Command、Info、State等指标筛选要监控的会话。其中Command表示每个线程当前正在执行的命令类型，详见[MySQL文档](https://dev.mysql.com/doc/refman/8.4/en/thread-commands.html)。State描述了线程当前的具体状态，详见[MySQL文档](https://dev.mysql.com/doc/refman/8.4/en/general-thread-states.html)。
  ![image](/images/session-management-session-monitor.png)

  在会话监控中，可以查看会话的明细，不过如果会话中执行的SQL太长或者SQL无法分析，则无法查看明细。
  ![image](/images/session-management-session-detail.png)

## 终止记录
  终止记录页面显示在会话监控页面终止掉的会话，可以根据时间范围进行筛选
  ![image](/images/session-management-termination-record.png)