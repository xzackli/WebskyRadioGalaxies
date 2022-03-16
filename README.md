# WebskyRadioGalaxies

Catalogs  are available online 
[here](https://portal.nersc.gov/project/sobs/users/Radio_WebSky/matched_catalogs_2/). Maps in Healpix and CAR pixelizations are [also available](https://portal.nersc.gov/project/sobs/users/Radio_WebSky/matched_maps/). Catalogs are HDF5 files with 

```
import h5py

f = h5py.File('catalog_100.0.h5', 'r')
print(f.keys())
```

The number in the filename refers to the frequency band center. This will output ['flux', 'phi', 'theta']. The fluxes are in Jansky. Angles are outputs from healpix vec2ang, so theta and phi are the colatitude and longitude in radians. 

## Matching Catalogs script 

In order to match the simulated catalogs from WebSky with updated number counts and SED, you can use the python script `matching_websky_catalogs.py`, as it's shown : 

```
python matching_websky_catalogs.py --frequencies 27  39 90. 150. --fwhm 10. 20. 5. 5.   --sensitivities 30. 20. 10. 5.    --input-catalog PATH/TO/REFERENCE/CATALOG  --ps4c-dir PATH/to/PS4C   --polarization  --verbose
```


Notice that you need to install PointSourceForeCasts ([PS4C](https://gitlab.com/giuse.puglisi/PS4C.git) ). 
The code is publicly available and documented [here](http://giuspugl.github.io/ps4c/index.html), you can install it with:  

```
 python setup.py install
```



