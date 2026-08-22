# Spark AQE

Source: `~/projects/spark/sql/core/src/main/scala/org/apache/spark/sql/execution/adaptive/AdaptiveSparkPlanExec.scala`
Last reviewed: 2026-08-22

## AI Summary

> The initial physical plan is a draft. AQE can improve the remaining plan using actual runtime statistics.

AQE works at query-stage boundaries and can:

- combine small shuffle partitions
- handle skewed partitions
- change supported join strategies

Example: Spark may replace a sort-merge join when runtime data shows that one side is small enough to broadcast.

AQE helps, but it does not remove the need to understand partitioning, shuffles, or query plans.

Related: [[Spark Architecture|Overview]], [[Spark SQL Query Lifecycle|SQL lifecycle]]
