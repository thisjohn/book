# How Redis Powers Your Web Service
by Gene Lian

## How to achieve faster web serving experience?

Solution: Redis Server: Works as a cache server

## Redis Server

- key-value cache
- very fast
    - c
    - in-memory
    - TCP socket (so no HTTP overhead)

## Drawbacks of Native Redis Server

Solution: Redis Sentinel: To automatically failover Redis Servers

## Drawbacks of Redis Server/Sentinel

- single thread
    - thread-safe
    - cannot use multicore CPUs
    - requests have to be queued
- cannot shared data acrooss them

Solution: Twemproxy

## Twemproxy

A fast Redis proxy from Twitter

- Automatically **shard** data across multiple Redis Servers by keys

## Redis Cluster

= Redis Server + Redis Sentinel + Twemproxy

- Automatic data sharding and fault tolerance

## More About Redis

- Transaction
- Pub/Sub
- Expiration
- Persistence
    - RDB (dump snapshot) and AOF (append each command)
- Queue/Stack

## Demo

- http://try.redis.io
- http://redis.io/commands

