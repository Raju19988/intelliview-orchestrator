# Log Retention and Purge Policy

## 1. Log Aggregation Approach
- Production logs from containerized orchestrator microservices are aggregated centrally using Docker's standard `json-file` logging driver.

## 2. Defined Retention Period
- **Max File Size:** restricted to `10m` (10 Megabytes) per individual service stream block.
- **Max Rotation Count:** capped at a maximum of `5` rotated configuration backups per active container.

## 3. Verified Purge Behavior
- Logs older than the 5-file rotation lifecycle or exceeding the specified sizes are automatically purged and hard-deleted by the daemon environment.
