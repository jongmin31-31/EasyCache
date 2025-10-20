# Notification

**Database > EasyCache > Console User Guide > Notification**

Using notification group allows you to receive notifications for performance metrics. Select **Notification Type** and **Activation Status**, and then specify nodes for monitoring and user groups to receive the notifications. In the **Monitoring Settings**, set the thresholds and conditions for performance metrics to receive notifications. When the configured metrics meet the monitoring settings conditions, a notification is sent to the connected user group. Notifications are sent via SMS or email, depending on the notification type set for the notification group.

### Create Notification Group

![notification1.PNG](https://static.toastoven.net/prod_easycache/25.09.27/notification1.PNG)

❶ Click **Create Notification Group** to display a pop-up screen for creating a notification group. ❷: Select how to receive the notification. ❸: Notification groups for which you select No for **Activation Status** will not send notifications. ❹: Select the target node for monitoring. ❺: Select the user groups to receive notifications.

## Monitoring Settings

The monitoring settings are made up of monitoring items, comparison methods, thresholds, and durations. To determine whether conditions are met, the performance indicators of the monitoring items are compared with the thresholds. If the conditions are met continuously for a duration longer than the specified duration, an alert will be sent. For example, if the CPU usage threshold is 90% or higher and the duration is 5 minutes, a notification will be sent to users defined in the user group when the CPU usage of a node associated with the notification group exceeds 90% for 5 minutes or more. If CPU usage exceeds 90%, but falls below 90% within 5 minutes, no notification will be generated.

### Monitoring Setting Items

Monitorable performance metrics include:

| Category| Item| Unit|
|----------|----------|----------|
| CPU| CPU_USAGE| %|
| CPU| CPU_USAGE_IOWAIT| %|
| CPU| CPU_USAGE_NICE| %|
| CPU| CPU_USAGE_SYSTEM| %|
| CPU| CPU_USAGE_USER| %|
| CPU| LOAD_AVG_1M| |
| CPU| LOAD_AVG_5M| |
| CPU| LOAD_AVG_15M| |
| MEMORY| MEMORY_USAGE| %|
| MEMORY| MEMORY_USED| Bytes|
| MEMORY| MEMORY_FREE| Bytes|
| MEMORY| MEMORY_BUFFERS| Bytes|
| MEMORY| MEMORY_CACHED| Bytes|
| MEMORY| SWAP_USED| Bytes|
| MEMORY| SWAP_TOTAL| Bytes|
| NETWORK| NETWORK_SENT| Bytes/sec|
| NETWORK| NETWORK_RECV| Bytes/sec|
| STORAGE| STORAGE_FREE_BYTE| Bytes|
| STORAGE| STORAGE_IO_READ_TOTAL| Bytes/sec|
| STORAGE| STORAGE_IO_WRITE_TOTAL| Bytes/sec|
| STORAGE| STORAGE_IO_READ| %|
| STORAGE| STORAGE_IO_WRITE| Bytes|
| STORAGE| LINUX_DISK_FAULT| |
| REDIS| REDIS_CONNECTED_CLIENTS| |
| REDIS| REDIS_CONNECTED_SLAVES| |
| REDIS| REDIS_USED_MEMORY_RATE| %|
| REDIS| REDIS_USED_MEMORY_RSS_RATE| %|
| REDIS| REDIS_MEM_FRAGMENTATION_RATIO| %|
| REDIS| REDIS_INSTANTANEOUS_OPS_PER_SEC| ops/sec|
| REDIS| REDIS_HIT_RATE| %|
| REDIS| REDIS_KEYS| |
| REDIS| REDIS_DELTA_BLOCKED_CLIENTS| |
| REDIS| REDIS_DELTA_NET_INPUT_BYTES| Bytes|
| REDIS| REDIS_DELTA_NET_OUTPUT_BYTES| Bytes|
| REDIS| REDIS_EXPIRED_KEYS| |
| REDIS| REDIS_EVICTED_KEYS| |
| REDIS| REDIS_KEYSPACE_HITS| |
| REDIS| REDIS_KEYSPACE_MISSES| |
| REDIS| REDIS_DELTA_CMDSTAT_GET_USEC_PER_CALL| ms|
| REDIS| REDIS_DELTA_CMDSTAT_SET_USEC_PER_CALL| ms|
| REDIS| REDIS_DELTA_CMDSTAT_GET_CALLS| |
| REDIS| REDIS_DELTA_CMDSTAT_SET_CALLS| |
| REDIS| REDIS_DELTA_CMDSTAT_HGET_CALLS| |
| REDIS| REDIS_DELTA_CMDSTAT_HSET_CALLS| |

### Add Monitoring Settings

![notification2.PNG](https://static.toastoven.net/prod_easycache/25.09.27/notification2.PNG)

❶ Press **Monitoring Settings** to display a pop-up window where you can change the monitoring settings. ❷ Press **Add Monitoring Settings** to add new monitoring settings. ❸ Enter the items to monitor, comparison method, threshold, and duration, then click **Add**.

### Change and Delete Monitoring Settings

![notification3.PNG](https://static.toastoven.net/prod_easycache/25.09.27/notification3.PNG)

❶ Click the button to change the added monitoring settings. ❹ Click the button to delete the added monitoring settings.

## User Group

You can manage the recipients as groups. The target should be registered as a project member. If a user belonging to a user group is removed from project membership, they will not receive notifications even if they belong to the user group.

!!! danger "Caution"
    If you do not complete real-name authentication and do not have mobile phone information, you will not be able to receive SMS notifications.

### Create User Group

![notification4.PNG](https://static.toastoven.net/prod_easycache/25.09.27/notification4.PNG)

❶ Press **Create User Group** to display a pop-up window where you can create user groups. ❷ Select All Project Members in the **Notification Method** section to automatically reflect all project members. ❸ Select Custom in the **Notification Method** section to display a list of notification recipients in the user group. ❹ Click **Add** to display the project members that you can add to the notification recipients list. ❺ Click **Confirm** to create the user group.

### Modify and Delete User Groups

![notification5.PNG](https://static.toastoven.net/prod_easycache/25.09.27/notification5.PNG)

❶ Click the button to modify the added user groups. ❹ Click the button to delete the added user groups.