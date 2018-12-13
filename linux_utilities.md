## WGRIB2 
Convert grib2 to netcdf (If version of wgrib is after 1.9.8, can remove the g2clib option)

```wgrib2 -g2clib 0 test.grb2 -netcdf test.nc```

## GDAL
Retrieve Proj4 from any grid file

```gdalsrsinfo -o proj4 /opt/meteo/data/regional/RAP/2015/rap_130_20150101_0000_000.grb2```

Convert netcdf or grib to GeoTIFF

```gdal_translate -of GTiff -sds -b 1 rap_130_20151231_2300_000.nc output.tiff```

Polygonize GeoTiff

```gdal_polygonize.py output.tiff output.shp```
