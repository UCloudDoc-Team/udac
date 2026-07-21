# 使用UDAC智能运维Agent功能

## AI诊断

1. 仅支持对当前Agent助手纳管的数据库实例进行诊断。
2. 支持通过自然语言直接发起AI诊断，也支持选择场景模板进行诊断。

![发起诊断](/udac/images/agent-use-diagnosis-step1.png)

![发起诊断-场景模板](/udac/images/agent-use-diagnosis-step2.png)

3. 在左侧点击新建会话，输入自然语言描述需要巡检的数据库实例ID及时间范围等信息即可发起巡检。Agent会根据您的提问自动规划诊断路径，从CPU、内存、会话、慢SQL等多个维度综合分析，并在必要时深入诊断（如发现慢SQL问题后自动进行SQL优化分析），提供索引建议或语句改写方案。

![发起诊断-会话](/udac/images/agent-use-diagnosis-step3.png)

4. 在Agent助手左侧导航栏查看近期会话记录。

## 运维报告

1. 运维报告内容仅覆盖当前Agent助手纳管的数据库实例。

![运维报告](/udac/images/agent-use-report-step1.png)

2. 每日凌晨2:00-5:00自动生成，对异常告警明细、重点优化建议（含高价值慢SQL识别）、磁盘空间使用态势、无效索引检测结果及关键资源水位（CPU、内存、I/O等）进行深度洞察与结构化汇总，助力运维团队全面掌握数据库健康状态。

![运维报告详情](/udac/images/agent-use-report-step2.png)

3. 在Agent助手左侧导航栏查看运维报告。
