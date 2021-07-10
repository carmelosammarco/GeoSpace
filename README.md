# GeoSpace: Anaconda environment for the earth's observations 

<p align="center">
  <img width="" height="200" src='src/Logo.png'>
</p>

# Library needed (before the main Anaconda installation)

The environment require the installation of the CDO (Climate Data Operators) library which can be installed with the following instructons. It is not strickly necessary and its installation or not installation depends on your aim. I leave to you the decision.

**- For MacOS:**

You can use homebrew, please check the extensive documentation under "https://brew.sh". After successful installation, CDO can be installed as easy as:

  ```
  brew install cdo
  ```

  **- For Linux:**
  
  You can use the native package manager of Linux Ubuntu as follow:

  ```
  sudo apt-get install cdo
  ```

# Anaconda environment installation

Once you installled CDO, just download the environment file relative to your operating system [HERE](https://anaconda.org/CSammarco/GeoSpace/files) and run in the same folder where you saved the file downloaded:

```
conda env create -f GeoSpace.yml
```

after that just activate the evironment to start to use it with:

```
conda activate GeoSpace
```

One you are done with the creation of the environment, you will  have all the main python modules nedded for the earth observation field (the most used at least, you can always add more if you need to), plus some  python tools  developed by me that I hope will semplify many of yours operation and procedures (I will describe brefly each one here but I kindly suggest you to to visit this [WEB-PAGE](carmelosammarco.com) for more detailed information and more detailed overview of these tools). The tools included in this environment and created by me are:

**- Tool4NC** : A python module for the netcdf file manipulation and conversions.

**- MerOC** : A Python module (with a GUI interface) to download data and manipulate/convert netCDF-files.  

**- ads4MO** : A Python module which adds new downloads services to the CMEMS portal (by Copernicus - registration to the portal required to download the data). It is applied mainly to big data requests using just a CLI and the HTTP data requests.

**- FTPsubsetMO** : Python module to download file from the CMEMS FTP servers (by Copernicus - registration to the portal required to download the data and then use the tool) and automatically subset them using many decisional criteria. It is applied mainly to big data requests of product with an elevated number of data requests and where as conseguence the HTTP protocol fail. It has a very intuitive GUI interface very user friendly. 

**- GPSconverter** : Python application to manipulate & view/plot GPS data. 

The standard python modules included in this environment and important to cite are (in alfabetic order):

- flask
- folium
- ftputil
- geopandas
- gmt
- gpxpy
- matplotlib
- motuclient
- netcdf4
- numpy
- pandas
- pygmt
- requests
- scipy
- simplekml
- xarray

but of course many more can be listed (with "conda list" command you can visualize all of them).Here I just tried to highlight the main one jst to give you an idea..

**Periodically I suggest you to run  the following command, inside the GeoSpace environment, to have always the last version avaiable of modules and tools:**

```
conda update --all
```

# Disclaimer:

The original tools included are result of personal intellectual work and as such I will not be held responsible for any use you make of it, nor for the results and conclusions you may find using it. Also Although I have cross-checked the whole code, I cannot warranty it is exempt of bugs. 

Please also to remember to cite them  if they help for research or jobs activities. Feedbacks ara also well accepted.

Enjoy! :)
