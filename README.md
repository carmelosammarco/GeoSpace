# GeoSpace: Anaconda environment for the earth's observations 

<p align="center">
  <img width="" height="200" src='https://github.com/carmelosammarco/GeoSpace/main/src/Logo.jpg'>
</p>

# Library needed before the main Anaconda installation

The environment to be fully fuctional (few fuctions depends on it) require the installation of the CDO (Climate Data Operators) library which can be installed with the following instructons (windows is excluded because not very user friendly.. maybe in the future):

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

Once you installled CDO, just download the environment file relative to your operating system [HERE](https://anaconda.org/CSammarco/GeoSpace/files) and run:

```
conda env create -f GeoSpace.yml
```

after that just activate the evironment to start to use it with:

```
conda activate GeoSpace
```

One you are done with the creation of the environment, you will  have all the main modules nedded for the earth observation field (the most used at least), plus some  python tools  developed by me that I hope will semplify many of yours operation and procedures (I will describe brefly each one here but I kindly suggest you to to visit this [link](carmelosammarco.com) for more detailed information and more detailed overview). The tools created by me are:

**- Tool4NC** --> A python module for the netcdf file manipulation and conversion

**- MerOC**   --> A Python module (with a GUI interface) to download data and manipulate/convert netCDF-files 

**- ads4MO**  --> A Python module which adds new downloads services to the CMEMS portal (by Copernicus - registration to the portal required to download the data). It is applied mainly to big data requests using just a CLI and the HTTP data requests.

**- FTPsubsetMO** --> Python module to download file from the CMEMS FTP servers (by Copernicus - registration to the portal required to download the data) and automatically subset them using many decisional criteria. It is applied mainly to big data requests of product with an elevated number of data requests and where then the HTTP protocol fail. It has a very intuitive GUI interface. 

**- GPSconverter** --> Python application to manipulate & view/plot GPS data.

**Periodically I suggest you to run  the following command, inside the GeoSpace environment, to have always the last version avaiable of modules and tools:**

```
conda update --all
```

# Disclaimer:

The original tools included are result of personal intellectual work and as such I will not be held responsible for any use you make of it, nor for the results and conclusions you may find using it. Also Although I have cross-checked the whole code, I cannot warranty it is exempt of bugs. 

Please also to remember to cite them  if they help for research or jobs activities. Feedbacks ara also well accepted.

Enjoy! :)
