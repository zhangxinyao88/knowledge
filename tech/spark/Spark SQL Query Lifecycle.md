# Spark SQL Query Lifecycle

Source: local code at `~/projects/spark`
Last reviewed: 2026-08-22

## AI Summary

```text
SQL
 -> parse: build a logical tree
 -> analyze: resolve tables, columns, and types
 -> optimize: rewrite into an equivalent cheaper plan
 -> plan: choose scans, joins, aggregation, and exchanges
 -> execute: an action starts distributed work
 -> adapt: AQE may revise the remaining plan
```

A DataFrame is mainly a plan until an action such as `show`, `count`, `collect`, or `write` asks for a result.

Parsing and metadata work may happen earlier. `collect()` returns data to the driver and can overwhelm it.

```python
df.explain("formatted")
```

Related: [[Spark Architecture|Overview]], [[Spark AQE|AQE]], [[Spark Execution Terms|execution terms]]
