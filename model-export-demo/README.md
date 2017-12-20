# Demo application for Databricks Model Export

This repository contains demos showing how to export Apache Spark ML models using **Databricks ML Model Export**
and use them in your own application.

- The notebook shows how to export an MLlib model on Databricks.
- The Java demo apps show how to import the model and perform inferernce via `dbml-local`.

For details including *supported models* and *versioning*, please check out [Databricks Documentation on Machine Learning](https://docs.databricks.com/spark/latest/mllib/index.html).

### Instructions to run

Use the accompanying notebook to train and export MLlib models. The `my_models/` directory also
contains example models you can use to get started.

Make sure that you have Maven installed, and then run:
```bash
mvn compile
mvn exec:java@app-vector-input
mvn exec:java@app-string-input
mvn exec:java@app-multi-threading
```
The calls to Maven exec will execute the example applications.

### `dbml-local` package

See the `pom.xml` file for the one dependency required by Databricks ML model export: `dbml-local`.
This package is published at [https://dl.bintray.com/databricks/maven/com/databricks/dbml-local/].
