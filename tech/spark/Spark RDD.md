# Spark RDD

Source: `~/projects/spark/core/src/main/scala/org/apache/spark/rdd/RDD.scala`
Last reviewed: 2026-08-22

## AI Summary

> An RDD is a distributed recipe, not necessarily data already in memory.

It describes:

- partitions
- how to compute each partition
- dependencies on parent RDDs
- partitioning and preferred locations

SQL is analyzed and optimized first. Its physical operators then use RDDs of internal rows or columnar batches for lower-level execution.

RDD lineage lets Spark recompute many lost partitions from their parents. RDDs are not cached unless requested and materialized by an action.

Related: [[Spark Architecture|Overview]], [[Spark Execution Terms|execution terms]]
