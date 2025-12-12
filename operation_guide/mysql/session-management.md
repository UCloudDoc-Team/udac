## 会话管理
  提供对会话的管理和监控

## 进入会话管理页面
  首先进入“实例管理”界面，然后选择需要监控的数据库实例，点击三个点的按钮，在弹出的菜单中选择“会话管理”进入会话管理界面
  ![image](/images/session-management-instance-click.png)

  ![image](/images/session-management-instance-page.png)

## SQL统计Top10
  点击“SQL统计Top10”，会统计出会话中出现的次数排在前10的SQL模板
  ![image](/images/session-management-sql-stat-top10.png)

  在“SQL统计Top10”页面对于每条SQL模板可以点击详情选项，会选择相同模板下执行时间最长的SQL语句分析执行计划
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

## SQL限流

SQL限流功能通过自主设置SQL类型、最大并发度、限流时间、SQL关键词/SQL模板，来限制数据库的请求访问量和SQL并发量，保障服务的可用性。该功能目前仅支持MySQL 5.7.41

SQL限流功能的首页会展示正在运行的限流任务数量以及正在运行的限流任务与历史限流任务的列表，列表中同时会展示限流任务的各项信息，限流任务列表是按照任务的开始时间倒序排列的。

![image](/images/sql_throttle_home_page.png)

单击“新建限流任务”按钮会弹出创建任务的页面，页面配置参数说明如下：

|    参数    |  说明   |
| --------- | ------- |
|  限流方式   |  限流方式分为SQL模板限流和关键字限流。SQL模板限流即根据SQL样本，提取出SQL模板，对该类型的SQL进行限流。关键字限流即根据SQL语句中的关键字进行匹配从而限流。   |
|   数据库   |  需要限流的数据库，如果选择了数据库，即只限流在该库上执行的SQL，如果不选择，则限流所有匹配到的SQL。  |
|   SQL类型  |  包括 SELECT、UPDATE、DELETE、INSERT。仅在关键字限流方式下支持该参数。   |
|  SQL样本   |  需要限流的SQL的样本，根据该SQL样本，提取SQL关键字或SQL模板。仅支持单条SQL。SQL样本长度不超过5000个字符。  |
|  提取结果   |  根据SQL样本，提取的SQL模板或SQL关键字，根据该参数进行SQL的限流。  |
|  最大并发数 |  为 SQL 最大并发数，当包含关键词的 SQL 达到最大并发数时会触发 SQL 限流策略。如果该值设为0，则表示限制所有匹配的 SQL 执行。在创建限流任务之前，已经开始执行的SQL语句，不会被计入并发数。  |
|  限流时长  |  SQL 限流时间。时间范围：[1,1440]，单位：分钟。  |

![image](/images/create_sql_throttle_task.png)

单击"重新发起"按钮即可重新发起任务。重新发起任务页面与“新建限流任务”页面相同，不过会填充上次任务的参数。如果重新发起的任务是正在运行的任务，会先结束正在运行的任务，然后再发起新任务。

当SQL语句匹配多个限流任务时，优先生效最新创建的限流任务，之前的任务将不再生效。

关键字限流对关键字有顺序要求，会按照关键字设置顺序进行匹配。如关键字设置为select~a~b，“select a, b from table”语句符合关键字顺序会被限流，“select b, a from table”语句因不符合关键字顺序而不会被限流