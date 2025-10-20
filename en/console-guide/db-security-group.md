# DB Security Group

**Database > EasyCache > Console User Guide > DB Security Group**

DB security groups are used to protect the cache and nodes by collectively controlling the outgoing and incoming traffic of nodes belonging to the cache. It uses a “positive security model” that allows traffic specified by rules and blocks the rest. If you do not connect a cache to the DB security group, the outgoing and incoming traffic is not allowed. Even if you create a DB security group, the rules of the DB security group will not be applied if you do not apply it to the cache. You can apply multiple DB security groups to the cache. The main features of DB security groups are as follows:

* Because DB security groups operate “stateful”, a session that has once been connected to DB security rules is allowed even if there are no rules in the opposite direction.
* For example, if the first packet on TCP 3306 to a node was passed by the “Receiving TCP PORT 3306” rule, packets sent from the node originating on TCP 3306 port will not be blocked.
* However, if the session expires since no packets matching the rules arrive within a certain period of time, packets in the opposite direction are also blocked.
* It's more efficient to specify a range of DB security rules than to add them one by one. Increasing the number of DB security rules can lead to performance degradation. Traffic with inappropriate session status may be blocked.

A DB security group consists of a name, a description, and multiple DB security rules. DB security group names have the following restrictions:

* The DB security group name can be between 1 and 100 characters long and can only contain English letters, numbers, and some symbols (-, \_, .). The first character can only be an English letter.

### Apply DB Security Group

You can select a DB security group to apply when creating a cache. All nodes within the cache will be affected by the selected DB security group. You can apply multiple DB security groups to the cache. All DB security group rules applied are applied to the cache. You can freely change it in the cache modification screen.

## DB Security Rules

You can create multiple DB security rules for a single DB security group. When you set a DB security group for a cache, all DB security rules created in the DB security group will be applied to all nodes within the cache.

| Item| Description|
|----------|----------|
| Direction| Incoming refers to the direction of incoming traffic to a node belonging to the cache. Outgoing refers to the direction of outgoing traffic from a node belonging to the cache.|
| Port| Set the port to apply the rules. Options are available for port, port range, service port, and TLS service port. When you select a service port or TLS port, the port value is assigned according to the cache information associated with the DB security group.|
| Ether| It refers to the version of EtherType IP. You can specify Ipv4 and IPv6.|
| Remote| You can specify IP address range. If the rule's direction is "Send," the destination is remote. If the rule's direction is "Receive," the source is remote. Depending on the rule's direction, the source and destination of the traffic are compared to the specified IP address or range.|
| Description| You can add the description for DB security group rules.|

### Change DB Security Group

When changes to a DB security rule occur, such as creation, modification, or deletion, the changes are applied sequentially to caches associated with the DB security group and the nodes within the caches. You cannot add new DB security rules to the DB security group, nor can you modify or delete other DB security rules until the changes are applied to all caches and nodes associated with the DB security group.