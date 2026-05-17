# PySpark Notes & Practice 🚀

A hands-on PySpark learning repository covering core concepts from architecture to advanced transformations, practiced on real datasets using Databricks.

## 📂 Repository Structure

| File | Description |
|------|-------------|
| `PySpark.ipynb` | Main notebook with all PySpark concepts and code |
| `BigMartSales.csv` | Retail dataset used for DataFrame practice |
| `drivers.json` | JSON dataset used for reading and schema exercises |

## 📚 Topics Covered

### Core Concepts
- **Spark Architecture** — Driver Program, SparkContext, Cluster Manager, Worker Nodes (Executor, Cache, Tasks)
- **Spark Benefits** — In-memory computation, Lazy Evaluation, Fault Tolerance, Partitioning
- **Lazy Evaluation** — Logical Plan, Transformations vs Actions (`show`, `display`, `collect`)
- **Hierarchical Structure** — Job → Stage → Task
- **Spark API** — Python, Scala, SQL, R

### Data Reading & Schema
- Reading CSV and JSON with `spark.read.format().option().load()`
- `inferSchema` for automatic type detection
- Schema definition via **DDL** and **StructType / StructField**
- `printSchema()` to inspect column data types

### Common Transformations
`select` · `alias` · `filter` · `withColumnRenamed` · `withColumn` · `cast` · `sort` · `limit` · `drop` · `dropDuplicates` · `distinct` · `union` · `unionByName`

### Functions
- **String**: `initcap()`, `upper()`, `lower()`
- **Date**: `current_date()`, `date_add()`, `date_sub()`, `datediff()`, `date_format()`
- **Null Handling**: `dropna()` (all / any / subset), `fillna()` (all columns / subset)

### Intermediate / Advanced
- **Split & Indexing** — splitting columns and accessing elements by index
- **Explode** — converting array columns into rows
- **Array Contains** — checking presence of values in array columns
- **GroupBy & Aggregations** — `sum`, `count`, multiple agg functions
- **Collect List** — aggregating values into a list per group
- **Pivot** — reshaping data
- **When-Otherwise** — conditional column creation

### Joins
`inner` · `left` · `right` · `full` · `anti`

### Window Functions
- `row_number()` — unique sequential numbering
- `rank()` and `dense_rank()` — with comparison table
- **Cumulative Sum** — using frame clauses (`unboundedPreceding`, `currentRow`, `unboundedFollowing`)

### UDFs (User Defined Functions)
1. Define a Python function
2. Convert to PySpark UDF with `udf()`
3. Use with `withColumn()`

### Writing Data
- Formats: CSV, Parquet, Table (`saveAsTable`)
- Modes: `append`, `overwrite`, `error`, `ignore`

### Spark SQL
- `createTempView` for running SQL queries on DataFrames

## 🛠️ Setup

This project was built and run on **Databricks**. To use locally:

```bash
pip install pyspark
```

Then open `PySpark.ipynb` in Jupyter or any compatible notebook environment.

