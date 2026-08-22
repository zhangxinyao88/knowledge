# Spark Distributed Execution

Source: local code at `~/projects/spark`
Last reviewed: 2026-08-22

## AI Summary

```text
Driver: plans and coordinates
Cluster manager: allocates resources
Executors: process data
```

- The **driver** owns `SparkSession`, query plans, and scheduler state.
- The **cluster manager** is usually YARN, Kubernetes, or Spark Standalone.
- **Executors** run tasks, read partitions, shuffle data, and cache blocks.

Spark has two scheduler layers:

- `DAGScheduler`: which stages must run, and in what order?
- `TaskScheduler`: which executor should run each task?

With classic PySpark, Python controls a JVM-based driver. Built-in SQL stays visible to Catalyst; Python UDFs may require Python workers and extra serialization.

Related: [[Spark Architecture|Overview]], [[Spark Execution Terms|execution terms]]
