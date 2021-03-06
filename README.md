# GeoSpace: Anaconda environment for the earth's observations 

<p align="center">
  <img width="" height="200" src='src/Logo.png'>
</p>

# Library needed before the main Anaconda installation

The GeoSpace environment and especially some tool's functionalities require the installation of the [CDO library](https://code.mpimet.mpg.de/projects/cdo/) (Climate Data Operators) which can be installed with the instructons given below. Overall it is not strictly necessary because the opration involved (to be more precise concerning the netcdf4 data splitting/merging and grib conversion). I just decide to add such library because I find it very intuitive and easy to use. Anyway,I am planning to create my own pythom module to archive the same results of the CDO library some time soon)

**- For MacOS:**

You can use homebrew, please check the extensive documentation under "https://brew.sh". After successful installation, CDO can be installed as easy as:

  ```
  brew install cdo
  brew install gmt
  ```

  **- For Linux:**
  
  You can use the native package manager of Linux Ubuntu as follow:

  ```
  sudo apt-get update
  sudo apt-get install cdo
  sudo apt-get install gmt
  ```

  **- For Window:**

  Install CDO is not very user friendly.. from the ufficial project [WEB-PAGE](https://code.mpimet.mpg.de/projects/cdo/wiki/Win32) you can retrive more info about.

# Anaconda environment installation

Once you installled CDO or not, Please to download the environment.yml file relative to your operating system [HERE](https://anaconda.org/CSammarco/GeoSpace/files) called "GeoSpace.yml" and run:

```
conda env create -f GeoSpace.yml
```

To activate the evironment run:

```
conda activate GeoSpace
```

**If you have trouble with the environment file as above then please try to do as follow:**

```
conda create --name GeoSpace  python=3.8
conda activate GeoSpace
conda install -c conda-forge gmt geopandas
```

Once done with it please to run:

```
pip install tool4NC MerOC FTPsubsetMO ads4MO CADS GPSconverter
```

At this point your environment should be functional and ready with my GeoSpatial tools! (if you want to have just few or none of them just modify the last pip command).

One you are done with the creation of the environment, you will  have all the main python modules used for the earth observation (the most used at least, but free to add more yourself to make it more tailored to your needs), plus, if it is your decision, some pip installed python tools developed by me that I hope will semplify many of yours operations and procedures, listed below (I will describe brefly each one here but I kindly suggest you to to visit the [LINK] for more detailed information or if you are just inteested in one specifically. If it is the latte case I suggest then to install the single tool rather the full environment):

**- Tool4NC** : A python module for the netcdf file manipulation and conversions. [[LINK](https://github.com/carmelosammarco/Tool4NC)]

**- MerOC** : A Python module (with a GUI interface) to download data from the CMEMS portal (by Copernicus - registration to the portal required to download the data) and manipulate/convert netCDF-files. [[LINK](https://github.com/carmelosammarco/MerOC)]

**- ads4MO** : A Python module which adds new downloads services to the CMEMS portal (by Copernicus - free registration to the portal required to download the data). It is applied mainly to big data requests using just a CLI and the HTTP data requests. [[LINK](https://github.com/carmelosammarco/ads4MO)]

**- FTPsubsetMO** : Python module to download file from the CMEMS FTP servers (by Copernicus - free registration to the portal required to download the data) and automatically subset them using many decisional criteria. It is applied mainly to big data requests of product with an elevated number of data requests and where then the HTTP protocol fail. It has a very intuitive GUI interface. [[LINK](https://github.com/carmelosammarco/FTPsubsetMO)]

**- GPSconverter** : Python application to manipulate & view/plot GPS data. [[LINK](https://github.com/carmelosammarco/GPSconverter)]

**-CADS** : Python module which merge both MerOC, ads4MO and FTPsubsetMO functionalities. [[LINK](https://github.com/carmelosammarco/CADS)]

**Periodically I suggest you to run  the following command, inside the GeoSpace environment, to have always the last version avaiable of modules and tools described above:**

```
conda update --all
```

# Disclaimer:

My tools included in this environment and listed above are result of personal intellectual work and development, so as such I will not be held responsible for any use you make of it, nor for the results and conclusions you may find using them. Also Although I have cross-checked the whole code, I cannot warranty it is exempt of bugs. 

Please also to remember to cite them  if they help your research or jobs activities and let me know of course!

Feedbacks ara well accepted.

Enjoy! :)
