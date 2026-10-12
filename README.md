# mc-redis-topology

Redis deployment patterns for Minecraft networks. Choose topology from failure-domain and consistency requirements, not from a preference for a particular Redis mode.

## Guidance
- Use separate ACL identities and key prefixes per service.
- Keep credentials out of plugin configs committed to source control.
- Set explicit memory limits and eviction policy per workload.
- Pub/Sub is ephemeral; do not use it for durable transactions.
- Monitor replication lag, evictions, rejected connections, and persistence health.

Test broker outage, reconnect storms, and failover behavior before rollout. MIT licensed.
