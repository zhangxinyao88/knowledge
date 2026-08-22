# Spark Repository Map

Source: local code at `~/projects/spark`
Last reviewed: 2026-08-22

## AI Summary

| Path | What lives there |
|---|---|
| `sql/catalyst` | SQL analysis and optimization |
| `sql/core` | `SparkSession`, planning, execution, AQE |
| `core` | RDD, scheduler, executor, shuffle, storage |
| `python` | PySpark and Python workers |
| `connector` | Kafka, Avro, Protobuf, and other connectors |
| `resource-managers` | YARN and Kubernetes integration |

Read one query end to end:

1. `sql/core/.../classic/SparkSession.scala`
2. `sql/core/.../execution/QueryExecution.scala`
3. `sql/core/.../execution/SparkPlan.scala`
4. `core/.../rdd/RDD.scala`
5. `core/.../scheduler/DAGScheduler.scala`
6. `core/.../executor/Executor.scala`

Do not try to understand the entire repository first.

Related: [[Spark Architecture|Overview]], [[Spark SQL Query Lifecycle|SQL lifecycle]]
