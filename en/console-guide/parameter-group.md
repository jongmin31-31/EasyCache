# Parameter Group

**Database > EasyCache > Console User Guide > Parameter Group**

EasyCache provides a parameter group feature to apply Valkey (old Redis) settings installed on the cache. A parameter group is a set of parameters that allow you to configure Valkey. When activating the service, a default parameter group is provided for each version of each engine. The default parameter group is provided as `{engine version name} Default` and consists of default parameter values recommended by versions. The default parameter group can be modified or deleted as the same as the common parameter group does.

### Create Parameter Group

You can create parameter groups in the console as needed. Parameter groups are created and named for each engine version, and have the following restrictions:

* The parameter group name can be between 1 and 100 characters long and can only contain English letters, numbers, and some symbols (-, \_, .). The first character can only be an English letter.
* When creating a parameter group, parameters are always created with default values. To create a parameter group based on an existing parameter group, you must use the Copy Parameter function to create the parameter group.

### Copy Parameter Group

Create a new parameter group based on an existing parameter group. The copied new parameter group consists of parameter values from the original parameter group. There is no relationship between the original and copied parameter groups, and changes or deletions in the original parameter group have no effect on the copied parameter group.

### Reset Parameter Group

Resetting parameter groups change all parameter values into engine version’s default values.

### Apply Parameter Group

You can select parameter groups to be applied to caches when creating and modifying them. A parameter group applies to a single cache, and a parameter group can be applied to multiple caches. When parameters in a parameter group are changed, the changes are not immediately applied to the cache. If there are associated caches, the parameter group status changes to "Apply Required," and the associated cache's **Parameter** button becomes active in the cache list screen. You can apply parameter changes to the cache by clicking the **Parameter** button on the Cache List screen. Once the parameter group changes are applied to all connected caches, the parameter group will change to the "Applied" status.

What is !!! tip "Note" If a parameter that requires a restart is changed, the cache will be restarted during the application process.

### Compare Parameter Group

Select two different parameter groups in the console and click **Compare** to see the parameter differences. You can compare parameter groups not only from the same engine but also from different engine versions.

### Delete Parameter Group

You can freely delete parameter groups except those currently being applied to caches. To delete a parameter group currently being applied to a cache, you must first change the parameter groups in all connected caches before deleting it.

## Parameter

### Change Parameter

You can change parameters by selecting a parameter group in the console and clicking **Edit Parameter**. Parameters that cannot be changed will display their values in plain text, while those that can be changed will display an input field where you can change the value. Clicking **Preview Changes** in the Edit screen will display a separate pop-up window where you can review the changed parameters. Clicking **Reset** will revert the changes to their previous state. By clicking **Save** changes, all values changed in the Edit mode will be reflected in the parameter group

### Change `acl-save-enabled` Parameter

`acl-save-enabled` is a parameter applicable from Redis version 6.0 onwards that determines whether to enable the feature of permanently storing the engine's user account and permission information in a file. The default is `no`. If you specify user and permission information for a node, that information will be lost and revert to the default settings if the node restarts. Therefore, to permanently record user information, you should change this option to `yes`. If you edit user information, it's recommended to click **Save** to settings to ensure complete saving.

!!! danger "Caution"
    Changing the value of the acl-save-enabled parameter requires careful manipulation, as it requires restarting the associated caches and nodes.