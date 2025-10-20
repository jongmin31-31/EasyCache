# Server Dashboard

**Database > EasyCache > Console User Guide > Server Dashboard**

You can visualize performance metrics in chart form from the Server Dashboard. The chart is laid out according to a preset layout. The metrics are collected once a minute and stored for up to 5 years. The metrics data is aggregated as averages at 5-minute, 30-minute, 2-hour, and 1-day intervals. The retention period for each aggregate unit is as follows:

| Aggregation Unit| Retention Period|
|----------|----------|
| 1 minute| 7 days|
| 5 minute| 1 month|
| 30 minute| 6 month|
| 2 hours| 2 years|
| 1 days| 5 years|

## Layout

You can indicate the size and location of the chart by using layout. When the service is enabled, it provides a default layout of **basic system metrics** and **basic Redis metrics**. You cannot change or delete the default layout. Also, you cannot add a chart, or change or delete the added chart. To view the information not included in the default layout on the chart, you can create a new layout and add it to the chart.

![server-dashboard-layout](https://static.toastoven.net/prod_rds_postgres/20240611/server-dashboard-layout-ko.png)

❶ Click **Manage Layouts** to display a pop-up screen for managing layouts. ❷ Click **+Create Layout** to create a layout.

- Enter a layout name and click **Create** to create the layout. ❸ Click the button to change the added layout. ❹ Click the button to delete the added layout.

### Add Layout to Chart

![server-dashboard-chart-add](https://static.toastoven.net/prod_rds_postgres/20240611/server-dashboard-chart-add-ko.png)

❶ Select the layout you want. ❷ Press **+ Add Chart** to display a pop-up screen for adding a chart. ❸ Select the checkbox to choose multiple metrics to add. ❹ Click the metric name to display a chart in the left preview area. ❺ Click **Add** to add all selected charts.

### Change and Delete Layout’s Chart

![server-dashboard-chart-manage](https://static.toastoven.net/prod_rds_postgres/20240611/server-dashboard-chart-manage-ko.png)

❶ Click the top of a chart and then drag and drop it to move the position. ❷ Drag and drop the right bottom of the chart to change the size of the chart. ❸ Click the x in the top right of the chart to delete it from the layout.

## Chart

You can view various performance metrics for nodes in chart form. Each performance metrics is composed of a different type of chart. In addition to basic system metrics, we provide various performance metrics provided by Redis in the form of charts. The metrics that can be checked by charts are as follows:

| Chart| Metric (unit)| Note|
|----------|----------|----------|
| CPU Utilization| cpu used (%)| |
| CPU Details| cpu user (%)<br/>cpu system (%)<br/>cpu nice (%)<br/>cpu IO wait (%)| |
| CPU Average Load| 1m<br/>5m<br/>15m| |
| Memory Usage| memory used (%)| |
| Memory Details| memory used (bytes)<br/>memory free (bytes)<br/>memory cached (bytes)<br/>memory buffers (bytes)| |
| Swap Usage| swap used (bytes)<br> swap total (bytes)| |
| Storage Usage| storage used (%)| |
| Remaining Storage Usage| storage free (%)| |
| Storage IO| disk read (bytes)<br> disk write (bytes)| |
| Network Data Transfer| nic incoming (bytes)<br> nic outgoing (bytes)| This is the basic network transmission used by Redis.|
| Storage Defect| disk fault status| Abnormal: 0, Normal: 1|
| Redis Memory Usage| Redis Memory Usage (bytes)| |
| Redis Memory Usage (rss)| Redis Memory Usage rss (bytes)| |
| Number of Connected Clients| Number of Connected Clients (counts)| |
| Number of Connected Replicas| Number of Connected Replicas (counts)| |
| Number of Blocked Clients| Number of Blocked Clients (counts)| |
| Memory Fragmentation Rate| Memory Fragmentation Rate (%)| |
| Commands Processed Per Second| Commands Processed Per Second (ops/1sec)| |
| Input Bytes| Input Bytes (bytes)| |
| Output Bytes| Output Bytes (bytes)| |
| Number of Keys Expired (expired)| Number of Keys Expired (counts)| |
| Number of Keys Deleted (evicted)| Number of Keys Deleted (counts)| |
| Number of Successful Lookups| Number of Successful Lookups (counts)| |
| Number of Failed Lookups| Number of Failed Lookups (counts)| |
| Lookup Success Rate| Lookup Success Rate (%)| |
| Number of Keys| Number of Keys (counts)| |
| get Execution Count| get Execution Count (counts)| |
| hget Execution Count| hget Execution Count (counts)| |
| get usec/get calls| get usec/get calls (counts)| |
| set Execution Count| get Execution Count (counts)| |
| hset Execution Count| hget Execution Count (counts)| |
| set usec/get calls| set usec/get calls (counts)| |

## Server Group

By using a server group, you can check performance metrics of various nodes from a single chart. Performance metrics for each node in a server group are displayed in a single chart. Charts with multiple performance metrics will all be changed to individual performance metrics within a server group.

### Create Server Group

![server-dashboard-group-add](https://static.toastoven.net/prod_rds_postgres/20240611/server-dashboard-group-add-ko.png)

❶ Click **+ Add Group** to display a pop-up screen for creating a group. ❷ Select the node to add to the server group.

### Server Group Settings

A node and server group are displayed together on the left side of the server dashboard.

![server-dashboard-group-manage](https://static.toastoven.net/prod_rds_postgres/20240611/server-dashboard-group-manage-ko.png)

❶ Press **+**, **-** to expand and collapse a server group. ❷ Click the node belonging to the server group to display a color selection pop-up that allows you to change the color it will appear in the chart.

![server-dashboard-group-menu](https://static.toastoven.net/prod_rds_postgres/20240611/server-dashboard-group-menu-ko.png)

❶ Click More icon that displays to the right of each item in the server list to change or delete the server group.