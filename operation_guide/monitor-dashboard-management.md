# 监控大盘管理 

监控大盘中的监控指标，采集数据的频率为5s/次；前端页面可以开启自动刷新，开启自动刷新后，前端页面的刷新频率为15s/次

## 进入监控大盘 
  点击操作界面“监控大盘”，进入监控大盘管理页面,
  ![image](/images/monitor-dashboard-management-page.png)
  界面会展示创建的所有的监控大盘信息，默认展示被设置为“默认”大盘的数据库实例指标
  信息。
  ![image](/images/monitor-dashboard-management-default.png)

## 创建监控大盘
  点击界面“新建大盘”，
  ![image](/images/monitor-dashboard-management-click-creation.png)
  
  弹出新建大盘编辑界面，填写大盘名，和是否需要选择数据库实例加入新建大盘中，
  ![image](/images/monitor-dashboard-management-click-creation-edit.png)
  
  然后点击“下一步”，进行指标配置项的选择，
  ![image](/images/monitor-dashboard-management-click-creation-item-edit.png)

  最后选择完成，成功后大盘创建成功。
  ![image](/images/monitor-dashboard-management-creation-completed.png)

## 编辑监控大盘实例 
  在大盘页面选择需要编辑的监控大盘，点击“编辑实例”，进入编辑页面，
  ![image](/images/monitor-dashboard-management-click-edit-instance.png)

  在编辑页面对该大盘实例进行操作(添加实例到大盘/从大盘移除实例)，
  ![image](/images/monitor-dashboard-management-edit-instance-operate.png)
  
  编辑完成后点击“确定”后，该大盘实例信息将进行更新。
  ![image](/images/monitor-dashboard-management-edit-instance-completed.png)

## 编辑监控大盘监控指标
  在大盘页面选择需要编辑的监控大盘，点击“编辑指标”，进入编辑页面，
  ![image](/images/monitor-dashboard-management-click-edit-metrics.png)

  在编辑页面对大盘监控指标进行操作(添加监控指标到大盘/从大盘移除已经选择的监控指标),
  ![image](/images/monitor-dashboard-management-edit-metrics-operate.png)

  编辑完成后点击“确定”后，该大盘监控指标信息将进行更新。
  ![image](/images/monitor-dashboard-management-edit-metrics-completed.png)

## 修改默认监控大盘 
   在监控大盘页面可以修改默认监控大盘(默认只有一个监控大盘设置为默认)。

   在大盘页面选择需要设置为默认的监控大盘，点击“设为默认”，
   ![image](/images/monitor-dashboard-management-click-set-default.png)

   设置完成后在该大盘右上角能看到“默认”的标识。
   ![image](/images/monitor-dashboard-management-click-set-default-completed.png)

## 删除监控大盘 
   在大盘页面选择需要删除的监控大盘，点击“删除大盘”进行大盘的删除操作，
   ![image](/images/monitor-dashboard-management-click-delete.png)

   操作完成后该大盘将被删除(无法恢复)。
