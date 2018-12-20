# Create table
```
CREATE TABLE weather_grid_RAP
(
  latitude double precision NOT NULL,
  longitude double precision NOT NULL,
  grid_id serial PRIMARY KEY
);
```

# Copy content of CSV in table
```
psql -h penguins -d telematic -U jgadoury \
      -c "\copy weather_grid_RAP (latitude, longitude, grid_id) \
      from STDIN with delimiter as ',' CSV HEADER" < rap_grid_canada.csv'
```

# Transfer shapefile to geoms on PostgreSQL 
```
shp2pgsql -s 4326 -d polygonized_RAP_grid_epsg4326.shp weather_grid_RAP_poly | psql -h penguins -d telematic -U jgadoury
```
