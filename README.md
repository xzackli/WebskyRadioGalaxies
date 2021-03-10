# WebskyRadioGalaxies



## Matching script 

In order to match the simulated catalogs from WebSky with updated number counts and SED, you can use the python script `matching_websky_catalogs.py`, as it's shown : 


```
python matching_websky_catalogs.py --frequencies 27  39 90. 150. --fwhm 10. 20. 5. 5.   --sensitivities 30. 20. 10. 5.    --input-catalog PATH/TO/REFERENCE/CATALOG  --ps4c-dir PATH/to/PS4C   --polarization  --verbose
```
Notice that you need to install PointSourceForeCasts PS4C

