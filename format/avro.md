# AVRO
Row based format
- has logical type timestamp
- Optimized for heavy write
- innovates use of JSON to describe the data, while using binary format to optimize storage size.

# Inspect
- In python: pypi [davidkhala.data.format[avro]](https://github.com/davidkhala/py-data/tree/main/format)
- In desktop
  - Avro Viewer
  - Apache Nifi
- In Java: Avro tools JAR
  - `java -jar avro-tools-X.X.X.jar tojson your-file.avro`
