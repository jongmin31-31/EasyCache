# Backup

**Database > EasyCache > Console User Guide > Backup**

You can prepare in advance to recover the cache in case of a failure. You can also perform backups from the console whenever you need them, or set them to occur periodically. During a backup, the cache’s master node may experience performance degradation. To avoid service impact, we recommend performing the backup during off-peak hours. If you do not want performance degradation due to backups, you can also use a high-availability configuration.

!!! tip "Note"
    Valkey creates a .rdb file while performing backup. When restoring from a backup you created, we recommend using a cache with an engine version that is compatible with the backup.

## Backup Types

There are two backup types: manual backup and auto backup.

### Manual Backup

You can permanently store the data of the cache at a point in time by performing backup manually in the console. Unlike auto backups, manual backups are not deleted when the cache is deleted unless you explicitly delete it. When creating a manual backup, you must specify a backup name and there are the following restrictions:

* The backup name can be between 1 and 100 characters long and can only contain English letters, numbers, and some symbols (-, \_, .). The first character can only be an English letter.

![backup1.PNG](https://static.toastoven.net/prod_easycache/25.09.27/backup1.PNG)

#### Create Manual Backup

❶ Select the cache you want to back up from the cache list and click Backup to manually create a backup. ❷ Click Create Backup in the backup list and specify the cache to back up to manually create a backup.

### Auto Backup

In addition to performing manual backups, auto backups can be performed when needed for restore operations or according to scheduled auto backup settings.

#### Set Auto Backup

You can specify settings to be applied to backups when creating and modifying caches.

![backup2.PNG](https://static.toastoven.net/prod_easycache/25.09.27/backup2.PNG)

##### Allow Auto Backup

If you do not allow auto backups, auto backups will not be performed, and the auto backup-related items below cannot be configured.

##### Backup Retention Period (day)

Set the retention period for auto backups in backup storage. You can retain automatic backups for up to 730 days. If the retention period is changed, automatic backup files that have exceeded the retention period will be deleted immediately.

##### Number of Auto Backup Retries

If auto backups fail due to cache overload or other various reasons, you can set them to retry. You can retry up to 10 times. Even if there are remaining retries, automatic backups may not retry depending on your auto backup execution time settings.

##### Schedule Auto Backup Time

You can set the time at which backups are automatically performed. It consists of a backup start time and a backup window. You can set multiple backup times without overlapping. A backup is performed at any point within the backup window based on the backup start time. The backup window has nothing to do with the total time it takes to perform the backup. The time taken for a backup is proportional to the memory usage of the cache and varies depending on the service load. If the backup fails, the backup will be retried based on the number of backup retries, provided the backup window has not been exceeded.

What is !!! tip "Note" Backup may not be performed in some situations, such as when the previous backup was not complete.

## Backup Storage and Billing

All backup files are uploaded and stored in internal backup storage. Manual backups are stored indefinitely until deleted, and backup storage billing apply based on the backup capacity. Auto backups are stored for the configured retention period and are charged based on the backup file size. The internal backup storage where backup files are stored cannot be directly accessed. If backup files are required, you can use the cache's data export function to export RDB files to NHN Cloud's object storage.

## Restore

You can use backups to restore data to any point in time. When restoring, you can choose to restore to an existing cache or create a new cache and restore it. You can restore to a cache that uses the same engine version as the original cache from which the backup was performed. To restore it with external RDB files, you can upload an RDB file to NHN Cloud object storage in the same region and then use the data import function for the cache you want.

!!! tip "Note"
    If the memory or Max Memory (MB) value of the cache to be restored is smaller than the “Backup Memory Capacity of Backup”, or if a parameter group different from the original cache parameter group is used, the restore may fail.