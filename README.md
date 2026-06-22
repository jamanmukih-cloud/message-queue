# Message Queue 📬

Embedded message queue with persistence and consumer groups.

## Features

- **Persistent Storage**: WAL-based durability
- **Consumer Groups**: Partition-level balancing
- **Dead Letter Queue**: Failed message routing
- **At-least-once Delivery**: Offset tracking

## Performance

| Metric | Value |
|--------|-------|
| Publish | 200K msg/s |
| Consume | 300K msg/s |
| Latency (p99) | 0.5ms |

## Quick Start

```rust
let queue = MessageQueue::open("/data/queue")?;
queue.publish("events", b"hello")?;
let msg = queue.consume("consumer-group-1")?;
```

## License

MIT