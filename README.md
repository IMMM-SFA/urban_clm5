# urban_clm5
The codes and files to convert WRF-generated meteorological forcings to the format that CLM5 can read.

To use it, do the following:
1. Modify covert.sh
2. Submit the job: ./covert.sh
3. Modify wrfout_forcing_spatial_replace.ncl
4. Sumbit the job: ncl wrfout_forcing_spatial_replace.ncl 
