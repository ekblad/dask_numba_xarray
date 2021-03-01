# dask_numba_xarray
Short demo of Dask, Numba, and Xarray for Herman Group meeting. If you want to download the data that was used to run the Xarray notebook, it can be found [here](https://www.earthsystemgrid.org/dataset/ucar.cgd.ccsm4.CLIVAR_LE.canesm2_lens_new.html). I used these four files from the atmospheric variables:
1. huss_day_CanESM2_historical_rcp85_r1i1p1_19500101-21001231.nc (from the daily atmospheric data - 1.37 GB)
2. pr_day_CanESM2_historical_rcp85_r1i1p1_19500101-21001231.nc (from the daily atmospheric data - 1.54 GB)
3. tas_day_CanESM2_historical_rcp85_r1i1p1_19500101-21001231.nc (from the daily atmospheric data - 1.09 GB)
4. zg_Amon_CanESM2_historical_rcp85_r1i1p1_195001-210012.nc (from the monthly atmospheric data - 694 MB)

![](canesm2_fields.png?raw=true)

These scripts need the Dask, Xarray, and Numba libraries (particularly dask.distributed) and the usual Numpy/Pandas/Matplotlib. In addition, the Dask demo uses NetworkX for visualizing the task graph, and the Xarray demo also requires Cartopy for adding countries/states/coastlines to the maps. Lastly, working in Jupyter Lab is the best way to visualize when using Dask, as there is [an extension](https://github.com/dask/dask-labextension) that implements Dask diagnostic widgets alongside your Notebook in the same browser tab. Oh, yeah, I also used a Seaborn color palette in the Xarray script, sorry! I will containerize a python install with all necessary libraries for this type of thing in the future, so you can run this in a temporary environment and delete it after.
