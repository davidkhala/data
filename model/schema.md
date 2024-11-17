Database tables schema design choices for analytical use

Keywords: [OLAP](https://github.com/davidkhala/data/wiki/OLAP)

https://www.thoughtspot.com/data-trends/data-modeling/star-schema-vs-snowflake-schema
## Star Schema
denormalized dimension tables
- More storage space in use 
- difficult to update and troubleshoot

## Snowflake schema
More complexity in design by further normalizing dimension tables
- more JOIN between dimension tables
