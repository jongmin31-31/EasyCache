# Event

**Database > EasyCache > Console User Guide > Event**

Event is an important incident that occurred by Valkey or a user. Event consists of an event type, a time and date when it occurred, an original source, and a message. Events can be viewed in the console, and you can subscribe to receive event notifications via email or SMS. The types of events and the possible events are as follows:

* Event Type and Event Code Currently Provided

| Event Type| Event Code| Subscription Availability| Description|
|----------|----------|----------|----------|
| CACHE| APPLY_LATEST_PARAMETER_GROUP_START| Yes| Applying the Latest Parameter Group Started|
| CACHE| APPLY_LATEST_PARAMETER_GROUP_END| Yes| Applying the Latest Parameter Group Completed|
| CACHE| APPLY_LATEST_PARAMETER_GROUP_FAILED| Yes| Applying the Latest Parameter Group Failed|
| CACHE| AUTO_BACKUP_ACTIVATION_START| Yes| Enabling Automatic Backup Started|
| CACHE| AUTO_BACKUP_ACTIVATION_END| Yes| Enabling Automatic Backup Completed|
| CACHE| AUTO_BACKUP_ACTIVATION_FAILED| Yes| Enabling Automatic Backup Failed|
| CACHE| AUTO_BACKUP_DEACTIVATION_START| Yes| Disabling Automatic Backup Started|
| CACHE| AUTO_BACKUP_DEACTIVATION_END| Yes| Disabling Automatic Backup Completed|
| CACHE| AUTO_BACKUP_DEACTIVATION_FAILED| Yes| Disabling Automatic Backup Failed|
| CACHE| BACKUP_START| Yes| Backup Started|
| CACHE| BACKUP_END| Yes| Backup Completed|
| CACHE| BACKUP_FAILED| Yes| Backup Failed|
| CACHE| BACKUP_MIGRATE_START| No| Backup Migration Started|
| CACHE| BACKUP_MIGRATE_END| No| Backup Migration Completed|
| CACHE| BACKUP_MIGRATE_DOWNLOAD_FAILED| No| Downloading Backup Migration Failed|
| CACHE| BACKUP_MIGRATE_RDB_CHECK_FAILED| No| Backup Migration RDB Check Failed|
| CACHE| BACKUP_MIGRATE_RDB_CHECKSUM_FAILED| No| Backup Migration RDB Checksum Failed|
| CACHE| BACKUP_MIGRATE_RDB_MEMORY_FAILED| No| Backup Migration RDB Memory Failed|
| CACHE| BACKUP_MIGRATE_RDB_TYPE_FAILED| No| Backup Migration RDB Type Failed|
| CACHE| BACKUP_MIGRATE_RDB_VERSION_FAILED| No| Backup Migration RDB Version Failed|
| CACHE| BACKUP_MIGRATE_REPLICA_CHECK_FAILED| No| Backup Migration Replica Check Failed|
| CACHE| BACKUP_MIGRATE_RESTART_FAILED| No| Restarting Backup Migration Failed|
| CACHE| BACKUP_RESTORE_EXISTING_CACHE_START| Yes| Backup Restoration with Existing Cache Started|
| CACHE| BACKUP_RESTORE_EXISTING_CACHE_END| Yes| Backup Restoration with Existing Cache Completed|
| CACHE| BACKUP_RESTORE_EXISTING_CACHE_FAILED| Yes| Backup Restoration with Existing Cache Failed|
| CACHE| BACKUP_RESTORE_EXISTING_CACHE_DOWNLOAD_FAILED| Yes| Downloading Backup Restoration with Existing Cache Failed|
| CACHE| BACKUP_RESTORE_EXISTING_CACHE_RDB_CHECK_FAILED| Yes| Backup Restoration RDB Check with Existing Cache Failed|
| CACHE| BACKUP_RESTORE_EXISTING_CACHE_RDB_CHECKSUM_FAILED| Yes| Backup Restoration RDB Checksum with Existing Cache Failed|
| CACHE| BACKUP_RESTORE_EXISTING_CACHE_RDB_MEMORY_FAILED| Yes| Backup Restoration RDB Memory with Existing Cache Failed|
| CACHE| BACKUP_RESTORE_EXISTING_CACHE_RDB_TYPE_FAILED| Yes| Backup Restoration RDB Type with Existing Cache Failed|
| CACHE| BACKUP_RESTORE_EXISTING_CACHE_RDB_VERSION_FAILED| Yes| Backup Restoration RDB Version with Existing Cache Failed|
| CACHE| BACKUP_RESTORE_EXISTING_CACHE_REPLICA_CHECK_FAILED| Yes| Backup Restoration Replica Check with Existing Cache Failed|
| CACHE| BACKUP_RESTORE_EXISTING_CACHE_RESTART_FAILED| Yes| Restarting Backup Restoration with Existing Cache Failed|
| CACHE| BACKUP_RESTORE_NEW_CACHE_START| Yes| Backup Restoration with New Cache Started|
| CACHE| BACKUP_RESTORE_NEW_CACHE_END| Yes| Backup Restoration with New Cache Completed|
| CACHE| BACKUP_RESTORE_NEW_CACHE_FAILED| Yes| Backup Restoration with New Cache Failed|
| CACHE| CACHE_CERTIFICATE_UPDATE_START| Yes| Renewing Cache Certificate Started|
| CACHE| CACHE_CERTIFICATE_UPDATE_END| Yes| Renewing Cache Certificate Completed|
| CACHE| CACHE_CERTIFICATE_UPDATE_FAILED| Yes| Renewing Cache Certificate Failed|
| CACHE| CACHE_CREATION_START| Yes| Creating Cache Started|
| CACHE| CACHE_CREATION_END| Yes| Creating Cache Completed|
| CACHE| CACHE_CREATION_FAILED| Yes| Creating Cache Failed|
| CACHE| CACHE_DATA_EXPORTING_START| Yes| Cache Data Export Started|
| CACHE| CACHE_DATA_EXPORTING_END| Yes| Cache Data Export Completed|
| CACHE| CACHE_DATA_EXPORTING_FAILED| Yes| Cache Data Export Failed|
| CACHE| CACHE_DATA_EXPORTING_RDB_CREATE_FAILED| Yes| Generating Cache Data Export RDB Failed|
| CACHE| CACHE_DATA_EXPORTING_SETTING_FAILED| Yes| Setting up Cache Data Export Failed|
| CACHE| CACHE_DATA_EXPORTING_UPLOAD_FAILED| Yes| Uploading Cache Data Export Failed|
| CACHE| CACHE_DATA_IMPORTING_START| Yes| Cache Data Import Started|
| CACHE| CACHE_DATA_IMPORTING_END| Yes| Cache Data Import Completed|
| CACHE| CACHE_DATA_IMPORTING_FAILED| Yes| Cache Data Import Failed|
| CACHE| CACHE_DATA_IMPORTING_DOWNLOAD_FAILED| Yes| Downloading Cache Data Import Failed|
| CACHE| CACHE_DATA_IMPORTING_RDB_CHECK_FAILED| Yes| Cache Data Import RDB Check Failed|
| CACHE| CACHE_DATA_IMPORTING_RDB_CHECKSUM_FAILED| Yes| Cache Data Import RDB Checksum Failed|
| CACHE| CACHE_DATA_IMPORTING_RDB_MEMORY_FAILED| Yes| Cache Data Import RDB Memory Failed|
| CACHE| CACHE_DATA_IMPORTING_RDB_TYPE_FAILED| Yes| Cache Data Import RDB Type Failed|
| CACHE| CACHE_DATA_IMPORTING_RDB_VERSION_FAILED| Yes| Cache Data Import RDB Version Failed|
| CACHE| CACHE_DATA_IMPORTING_REPLICA_CHECK_FAILED| Yes| Cache Data Import Replica Check Failed|
| CACHE| CACHE_DATA_IMPORTING_RESTART_FAILED| Yes| Restarting Cache Data Import Failed|
| CACHE| CACHE_DATA_IMPORTING_SETTING_FAILED| Yes| Setting up Cache Data Import Failed|
| CACHE| CACHE_DELETION_START| Yes| Deleting Cache Started|
| CACHE| CACHE_DELETION_END| Yes| Deleting Cache Completed|
| CACHE| CACHE_DELETION_FAILED| Yes| Deleting Cache Failed|
| CACHE| CACHE_DELETION_PROTECTION_DISABLING_START| Yes| Disabling Cache Deletion Protection Started|
| CACHE| CACHE_DELETION_PROTECTION_DISABLING_END| Yes| Disabling Cache Deletion Protection Completed|
| CACHE| CACHE_DELETION_PROTECTION_DISABLING_FAILED| Yes| Disabling Cache Deletion Protection Failed|
| CACHE| CACHE_DELETION_PROTECTION_ENABLING_START| Yes| Enabling Cache Deletion Protection Started|
| CACHE| CACHE_DELETION_PROTECTION_ENABLING_END| Yes| Enabling Cache Deletion Protection Completed|
| CACHE| CACHE_DELETION_PROTECTION_ENABLING_FAILED| Yes| Enabling Cache Deletion Protection Failed|
| CACHE| CACHE_DETAIL_MODIFICATION_START| Yes| Modifying Cache in Detail Started|
| CACHE| CACHE_DETAIL_MODIFICATION_END| Yes| Modifying Cache in Detail Completed|
| CACHE| CACHE_DETAIL_MODIFICATION_FAILED| Yes| Modifying Cache in Detail Failed|
| CACHE| CACHE_FLAVOR_MODIFICATION_START| Yes| Changing Cache Specs Started|
| CACHE| CACHE_FLAVOR_MODIFICATION_END| Yes| Changing Cache Specs Completed|
| CACHE| CACHE_FLAVOR_MODIFICATION_FAILED| Yes| Changing Cache Specs Failed|
| CACHE| CACHE_HIGH_AVAILABILITY_REPAIR_START| Yes| Recovering Cache High Availability Started|
| CACHE| CACHE_HIGH_AVAILABILITY_REPAIR_END| Yes| Recovering Cache High Availability Completed|
| CACHE| CACHE_HIGH_AVAILABILITY_REPAIR_FAILED| Yes| Recovering Cache High Availability Failed|
| CACHE| CACHE_MASTER_ROLE_CHANGING_START| Yes| Changing Cache Master Role Started|
| CACHE| CACHE_MASTER_ROLE_CHANGING_END| Yes| Changing Cache Master Role Completed|
| CACHE| CACHE_MASTER_ROLE_CHANGING_FAILED| Yes| Changing Cache Master Role Failed|
| CACHE| CACHE_MODIFICATION_START| Yes| Modifying Cache Started|
| CACHE| CACHE_MODIFICATION_END| Yes| Modifying Cache Completed|
| CACHE| CACHE_MODIFICATION_FAILED| Yes| Modifying Cache Failed|
| CACHE| CACHE_RESTART_START| Yes| Restarting Cache Started|
| CACHE| CACHE_RESTART_END| Yes| Restarting Cache Completed|
| CACHE| CACHE_RESTART_FAILED| Yes| Restarting Cache Failed|
| CACHE| CACHE_STARTING_START| Yes| Starting Cache Started|
| CACHE| CACHE_STARTING_END| Yes| Starting Cache Completed|
| CACHE| CACHE_STARTING_FAILED| Yes| Starting Cache Failed|
| CACHE| CACHE_STOPPING_START| Yes| Stopping Cache Started|
| CACHE| CACHE_STOPPING_END| Yes| Stopping Cache Completed|
| CACHE| CACHE_STOPPING_FAILED| Yes| Stopping Cache Failed|
| CACHE| CACHE_UPGRADE_START| Yes| Cache Upgrade Started|
| CACHE| CACHE_UPGRADE_END| Yes| Cache Upgrade Completed|
| CACHE| CACHE_UPGRADE_FAILED| Yes| Cache Upgrade Failed|
| CACHE| CACHE_UPGRADE_HA_UPGRADE_FAILED| Yes| Cache Upgrade HA Failed|
| CACHE| CACHE_UPGRADE_MASTER_UPGRADE_FAILED| Yes| Cache Upgrade Master Failed|
| CACHE| CACHE_UPGRADE_REPLICA_PROMOTE_FAILED| Yes| Promoting Cache Upgrade Replica Failed|
| CACHE| CACHE_UPGRADE_REPLICA_UPGRADE_FAILED| Yes| Cache Upgrade Replica Failed|
| CACHE| FAILOVER_DNS_FAILED| No| DNS Update Failed|
| CACHE| FAILOVER_DNSFAIL| Yes| Failover DNS Failed|
| CACHE| FAILOVER_EXECUTED| Yes| Failover occurred|
| CACHE| FLOATING_IP_ATTACHING_START| Yes| Connecting Floating IP Started|
| CACHE| FLOATING_IP_ATTACHING_END| Yes| Connecting Floating IP Completed|
| CACHE| FLOATING_IP_ATTACHING_FAILED| Yes| Connecting Floating IP Failed|
| CACHE| FLOATING_IP_DETACHING_START| Yes| Disconnecting Floating IP Started|
| CACHE| FLOATING_IP_DETACHING_END| Yes| Disconnecting Floating IP Completed|
| CACHE| FLOATING_IP_DETACHING_FAILED| Yes| Disconnecting Floating IP Failed|
| CACHE| HA_NODE_CREATION_START| Yes| Creating HA Node Started|
| CACHE| HA_NODE_CREATION_END| Yes| Creating HA Node Completed|
| CACHE| HA_NODE_CREATION_FAILED| Yes| Creating HA Node Failed|
| CACHE| HA_NODE_DELETION_START| Yes| Deleting HA Node Started|
| CACHE| HA_NODE_DELETION_END| Yes| Deleting HA Node Completed|
| CACHE| NODE_OS_UPGRADE_START| Yes| Node OS Upgrade Started|
| CACHE| NODE_OS_UPGRADE_END| Yes| Node OS Upgrade Completed|
| CACHE| NODE_OS_UPGRADE_FAILED| Yes| Node OS Upgrade Failed|
| CACHE| READONLY_DOMAIN_ATTACHING_START| Yes| Start Connecting Read-only Domain|
| CACHE| READONLY_DOMAIN_ATTACHING_END| Yes| Read-only Domain Connection Completed|
| CACHE| READONLY_DOMAIN_ATTACHING_FAILED| Yes| Connecting Read-only Domain Failed|
| CACHE| READONLY_DOMAIN_DETACHING_START| Yes| Disconnect Read-only Domain|
| CACHE| READONLY_DOMAIN_DETACHING_END| Yes| Read-only Domain Disconnection Completed|
| CACHE| READONLY_DOMAIN_DETACHING_FAILED| Yes| Read-only Domain Disconnection Failed|
| CACHE| READONLY_DOMAIN_UPDATE_START| Yes| Start Read-only Domain Update|
| CACHE| READONLY_DOMAIN_UPDATE_END| Yes| Read-only Domain Update Completed|
| CACHE| READONLY_DOMAIN_UPDATE_FAILED| Yes| Read-only Domain Update Failed|
| CACHE| SENTINEL_CREATION_START| No| Creating Sentinel Node Started|
| CACHE| SENTINEL_CREATION_END| No| Creating Sentinel Node Completed|
| CACHE| SENTINEL_CREATION_FAILED| No| Creating Sentinel Node Failed|
| CACHE| SENTINEL_DELETION_START| No| Deleting Sentinel Node Started|
| CACHE| SENTINEL_DELETION_END| No| Deleting Sentinel Node Completed|
| CACHE| SENTINEL_DELETION_FAILED| No| Deleting Sentinel Node Failed|
| CACHE| SENTINEL_FAILOVER| No| Failover occurred|
| CACHE| SENTINEL_FAILOVER_DNSFAIL| No| Failover DNS Failed|
| CACHE| SENTINEL_QUORUM_UPDATE_START| Yes| Sentinel Quorum Update Started|
| CACHE| SENTINEL_QUORUM_UPDATE_END| Yes| Sentinel Quorum Update Completed|
| CACHE| SENTINEL_QUORUM_UPDATE_FAILED| Yes| Sentinel Quorum Update Failed|
| CACHE| SLAVE_NODE_PROMOTION_START| Yes| Promoting Slave Node Started|
| CACHE| SLAVE_NODE_PROMOTION_END| Yes| Promoting Slave Node Completed|
| CACHE| SLAVE_NODE_PROMOTION_FAILED| Yes| Promoting Slave Node Failed|
| NODE| NODE_DELETION_START| Yes| Deleting Node Started|
| NODE| NODE_DELETION_END| Yes| Deleting Node Completed|
| NODE| NODE_DELETION_FAILED| Yes| Deleting Node Failed|
| NODE| NODE_DOWN_DETECTED| Yes| Node Stopped|
| NODE| NODE_FLAVOR_MODIFICATION_START| Yes| Changing Node Specs Started|
| NODE| NODE_FLAVOR_MODIFICATION_END| Yes| Changing Node Specs Completed|
| NODE| NODE_FLAVOR_MODIFICATION_FAILED| Yes| Changing Node Specs Failed|
| NODE| NODE_PLANNED_MIGRATION_START| Yes| Node Planned Migration Started|
| NODE| NODE_PLANNED_MIGRATION_END| Yes| Node Planned Migration Completed|
| NODE| NODE_PLANNED_MIGRATION_FAILED| Yes| Node Planned Migration Failed|
| NODE| NODE_RECOVERED| Yes| Executing Node|
| NODE| NODE_UPGRADE_START| Yes| Node Engine Upgrade Started|
| NODE| NODE_UPGRADE_END| Yes| Node Engine Upgrade Completed|
| NODE| NODE_UPGRADE_FAILED| Yes| Node Engine Upgrade Failed|
| NODE| NODE_UPGRADE_DOWNLOAD_FAILED| Yes| Downloading Node Engine Upgrade Failed|
| NODE| NODE_UPGRADE_PROFILE_UPDATE_FAILED| Yes| Updating Node Engine Upgrade Parameter Group Failed|
| NODE| NODE_UPGRADE_REDIS_N_SENTINEL_START_FAILED| Yes| Starting Node Engine Upgrade Service Failed|
| NODE| NODE_UPGRADE_REDIS_N_SENTINEL_STOP_FAILED| Yes| Stopping Node Engine Upgrade Service Failed|
| NODE| NODE_UPGRADE_REDIS_UPGRADE_FAILED| Yes| Upgrading Node Engine Upgrade Redis Failed|
| NODE| NODE_UPGRADE_REPLICA_CHECK_FAILED| Yes| Node Engine Upgrade Replica Check Failed|
| NODE| NODE_UPGRADE_RPM_DELETE_FAILED| Yes| Deleting Node Engine Upgrade RPM Failed|
| NODE| NODE_UPGRADE_SENTINEL_START_FAILED| Yes| Starting Node Engine Upgrade Sentinel Failed|
| NODE| NODE_UPGRADE_SENTINEL_STOP_FAILED| Yes| Stopping Node Engine Upgrade Sentinel Failed|
| NODE| SENTINEL_INSTANCE_RUNNING| No| Instance Executed|
| NODE| SENTINEL_INSTANCE_STOPPED| No| Instance Stopped|
| NODE| SLAVE_NODE_CREATION_START| Yes| Creating Replication Node Started|
| NODE| SLAVE_NODE_CREATION_END| Yes| Creating Replication Node Completed|
| NODE| SLAVE_NODE_CREATION_FAILED| Yes| Creating Replication Node Failed|
| NODE| STATUS_CHANGED_DISABLED| No| Disable|
| NODE| STATUS_CHANGED_ENABLED| No| Enable|
| DB_SECURITY_GROUP| DB_SECURITY_GROUP_CREATION_START| No| Creating DB Security Group Started|
| DB_SECURITY_GROUP| DB_SECURITY_GROUP_CREATION_END| No| Creating DB Security Group Completed|
| DB_SECURITY_GROUP| DB_SECURITY_GROUP_CREATION_FAILED| No| Creating DB Security Group Failed|
| DB_SECURITY_GROUP| DB_SECURITY_GROUP_DELETION_START| No| Deleting DB Security Group Started|
| DB_SECURITY_GROUP| DB_SECURITY_GROUP_DELETION_END| No| Deleting DB Security Group Completed|
| DB_SECURITY_GROUP| DB_SECURITY_GROUP_DELETION_FAILED| No| Deleting DB Security Group Failed|
| DB_SECURITY_GROUP| DB_SECURITY_GROUP_MODIFICATION_START| No| Modifying DB Security Group Started|
| DB_SECURITY_GROUP| DB_SECURITY_GROUP_MODIFICATION_END| No| Modifying DB Security Group Completed|
| DB_SECURITY_GROUP| DB_SECURITY_GROUP_MODIFICATION_FAILED| No| Modifying DB Security Group Failed|
| DB_SECURITY_GROUP| DB_SECURITY_GROUP_RULE_CREATION_START| No| Creating DB Security Group Rule Started|
| DB_SECURITY_GROUP| DB_SECURITY_GROUP_RULE_CREATION_END| No| Creating DB Security Group Rule Completed|
| DB_SECURITY_GROUP| DB_SECURITY_GROUP_RULE_CREATION_FAILED| No| Creating DB Security Group Rule Failed|
| DB_SECURITY_GROUP| DB_SECURITY_GROUP_RULE_DELETION_START| No| Deleting DB Security Group Rule Started|
| DB_SECURITY_GROUP| DB_SECURITY_GROUP_RULE_DELETION_END| No| Deleting DB Security Group Rule Completed|
| DB_SECURITY_GROUP| DB_SECURITY_GROUP_RULE_DELETION_FAILED| No| Deleting DB Security Group Rule Failed|
| DB_SECURITY_GROUP| DB_SECURITY_GROUP_RULE_MODIFICATION_START| No| Modifying DB Security Group Rule Started|
| DB_SECURITY_GROUP| DB_SECURITY_GROUP_RULE_MODIFICATION_END| No| Modifying DB Security Group Rule Completed|
| DB_SECURITY_GROUP| DB_SECURITY_GROUP_RULE_MODIFICATION_FAILED| No| Modifying DB Security Group Rule Failed|
| PARAMETER_GROUP| PROFILE_UPDATE_START| No| Profile Update Started|
| PARAMETER_GROUP| PROFILE_UPDATE_END| No| Profile Update Completed|
| PARAMETER_GROUP| PROFILE_UPDATE_FAILED| No| Profile Update Failed|
| MONITORING| METRIC_ALARM_TRIGGERED| Yes| Monitoring Alarm occurred|

* Event codes that remain in the record but are no longer created

| Event Type| Event Code| Subscription Availability| Description|
|----------|----------|----------|----------|
| CACHE| GROUP_CERTIFICATE_UPDATE_START| No| Updating Group Certificate Started|
| CACHE| GROUP_CERTIFICATE_UPDATE_END| No| Updating Group Certificate Completed|
| CACHE| GROUP_CERTIFICATE_UPDATE_FAILED| No| Updating Group Certificate Failed|
| CACHE| GROUP_CREATION_START| No| Start Group Creation|
| CACHE| GROUP_CREATION_END| No| Group Creation Completed|
| CACHE| GROUP_CREATION_FAILED| No| Group Creation Failed|
| CACHE| GROUP_DATA_EXPORTING_START| No| Group Data Export Started|
| CACHE| GROUP_DATA_EXPORTING_END| No| Group Data Export Completed|
| CACHE| GROUP_DATA_EXPORTING_FAILED| No| Group Data Export Failed|
| CACHE| GROUP_DATA_EXPORTING_RDB_CREATE_FAILED| No| Group Data Export RDB Creation Failed|
| CACHE| GROUP_DATA_EXPORTING_SETTING_FAILED| No| Group Data Export Settings Failed|
| CACHE| GROUP_DATA_EXPORTING_UPLOAD_FAILED| No| Group Data Export Upload Failed|
| CACHE| GROUP_DATA_IMPORTING_START| No| Group Data Import Started|
| CACHE| GROUP_DATA_IMPORTING_END| No| Group Data Import Completed|
| CACHE| GROUP_DATA_IMPORTING_DOWNLOAD_FAILED| No| Group Data Export Download Failed|
| CACHE| GROUP_DATA_IMPORTING_RDB_CHECK_FAILED| No| Group Data Import RDB Check Failed|
| CACHE| GROUP_DATA_IMPORTING_RDB_CHECKSUM_FAILED| No| Group Data Import RDB Checksum Failed|
| CACHE| GROUP_DATA_IMPORTING_RDB_MEMORY_FAILED| No| Group Data Import RDB Memory Failed|
| CACHE| GROUP_DATA_IMPORTING_RDB_TYPE_FAILED| No| Group Data Import RDB Type Failed|
| CACHE| GROUP_DATA_IMPORTING_RDB_VERSION_FAILED| No| Group Data Import RDB Version Failed|
| CACHE| GROUP_DATA_IMPORTING_REPLICA_CHECK_FAILED| No| Group Data Import Replica Check Failed|
| CACHE| GROUP_DATA_IMPORTING_RESTART_FAILED| No| Group Data Export Restart Failed|
| CACHE| GROUP_DATA_IMPORTING_SETTING_FAILED| No| Group Data Export Settings Failed|
| CACHE| GROUP_DELETION_START| No| Start Group Deletion|
| CACHE| GROUP_DELETION_END| No| Group Deletion Completed|
| CACHE| GROUP_DELETION_FAILED| No| Group Deletion Failed|
| CACHE| GROUP_FLAVOR_MODIFICATION_START| No| Changing Group Specification Started|
| CACHE| GROUP_FLAVOR_MODIFICATION_END| No| Changing Group Specification Completed|
| CACHE| GROUP_FLAVOR_MODIFICATION_FAILED| No| Changing Group Specification Failed|
| CACHE| GROUP_MODIFICATION_START| No| Group Modification Started|
| CACHE| GROUP_MODIFICATION_END| No| Group Modification Completed|
| CACHE| GROUP_MODIFICATION_FAILED| No| Group Modification Failed|
| CACHE| GROUP_RESTART_START| No| Group Restart Started|
| CACHE| GROUP_RESTART_END| No| Group Restart Completed|
| CACHE| GROUP_RESTART_FAILED| No| Group Restart Failed|
| CACHE| GROUP_UPGRADE_START| No| Group Upgrade Started|
| CACHE| GROUP_UPGRADE_END| No| Group Upgrade Completed|
| CACHE| GROUP_UPGRADE_FAILED| No| Group Upgrade Failed|
| CACHE| GROUP_UPGRADE_HA_UPGRADE_FAILED| No| Group Upgrade HA Failed|
| CACHE| GROUP_UPGRADE_MASTER_UPGRADE_FAILED| No| Group Upgrade Master Failed|
| CACHE| GROUP_UPGRADE_REPLICA_PROMOTE_FAILED| No| Group Upgrade Replica Promotion Failed|
| CACHE| GROUP_UPGRADE_REPLICA_UPGRADE_FAILED| No| Group Upgrade Replica Failed|

## Event Subscription

You can subscribe to events by event type, code, and source. Subscribing by event type will receive notifications for all event codes included in the event type. If notifications are too broad, you can further refine your subscription by event code and source. You can select only project members to receive notifications. Event notifications are sent by email by default, and additional notifications are sent via SMS only if a verified mobile phone number is registered.

![event1.PNG](https://static.toastoven.net/prod_easycache/25.09.27/event1.PNG) ![event2.PNG](https://static.toastoven.net/prod_easycache/25.09.27/event2.PNG)

❶: Click **Register for Event Subscription** to display a pop-up window where you can register for an event subscription. ❷: Select the type of event you wish to subscribe to. Depending on the event type, the event codes you can select will change. ❸: Using an event template, you can enter predefined event codes in a single step. ❹: Select the event code you want to subscribe to. If you change the event code while using an event template, the event template item will be disabled. ❹: Select the event source you want to subscribe to. ❻: Select the user groups to receive event notifications. ❼: Select how you want to receive notifications via Notification Type. ❽: Select whether to enable it. If you select **No** for enabling, no event notifications will be sent.