# Convert grib2 to netcdf
# If version of wgrib is after 1.9.8, can remove the g2clib option
wgrib2 -g2clib 0 test.grb2 -netcdf test.nc

