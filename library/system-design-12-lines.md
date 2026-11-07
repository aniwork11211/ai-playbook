# System design in 12 lines

Source: @iamsaumyaawasthi. Twelve common problems and the move that answers each one.

Use this file when a backend symptom shows up and you need the first move. Open it from `C:\Users\ANISH\Documents\ai-playbook\LIBRARY.md` and use the one line that matches the symptom.

- Slow reads — add a cache
- Write spikes — buffer with a queue
- Too much traffic — add a load balancer
- Read-heavy database — add read replicas
- Write-heavy database — shard the data
- Slow queries — add indexes
- Slow file loads — object storage plus a CDN
- Temporary failures — retry with backoff
- Too many requests — rate limiting
- One service failing — circuit breaker
- Duplicate requests — idempotency keys
- Cannot see what broke — logs, metrics, tracing
