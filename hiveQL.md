# Concatenate two tables

### Keep all rows
UNION ALL

### Remove duplicates
UNION

### Repair partitoned table so that it can communicate between Hive and Spark
MSCK REPAIR TABLE <table_name>
  
### View how table was created
SHOW CREATE TABLE <table_name>
