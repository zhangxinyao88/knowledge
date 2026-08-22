# Spark Execution Terms

Source: local code at `~/projects/spark`
Last reviewed: 2026-08-22

## AI Summary

| Term | Meaning |
|---|---|
| Action | `count`, `show`, or `write`; asks Spark for a result |
| Job | Top-level work created by an action |
| Stage | Work between shuffle boundaries |
| Task | One stage's work for one partition |
| Partition | A slice of data and the unit of parallelism |
| Shuffle | Redistribution of data across partitions/executors |
| Exchange | Physical-plan node that usually causes redistribution |
| Spill | Intermediate data written to disk |
| Skew | A few partitions have much more work than others |

```text
action -> job -> stages -> tasks -> partitions
                  ^
               shuffle boundary
```

`filter` is usually narrow and can stay in one stage. `GROUP BY`, `JOIN`, `DISTINCT`, and `repartition` often shuffle.

Related: [[Spark Architecture|Overview]], [[Spark Distributed Execution|distributed execution]]
