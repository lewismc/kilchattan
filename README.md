# Kilchattan

<img src="https://github.com/lewismc/kilchattan/blob/master/docs/a-sunny-day-in-kilchattan-bay.jpg" align="right" width="300" />

**Kilchattan is a [Scientific Data Formats](http://fileformats.archiveteam.org/wiki/Scientific_Data_formats)
(SDF)-to-[CoverageJSON](https://github.com/Reading-eScience-Centre/coveragejson/) 
generation framework**.

##Introduction
Figuratively speaking, SDF come in many shapes and sizes. Primarily however they
exist as machine-independent data formats that support the creation, access, and 
sharing of array-oriented scientific data. Within Earth Science, the most notable 
general examples include the [HDF](https://eosweb.larc.nasa.gov/HBDOCS/hdf.html) family, 
[NetCDF](http://www.unidata.ucar.edu/software/netcdf/), etc. with other formats such
as [GRIB](http://www.wmo.int/pages/prog/www/WDM/Guides/Guide-binary-2.html)
being used pervasively within specific domains such as the Oceanographic, 
Atmospheric and Meteorological sciences.

Such file formats contain [Coverage Data](https://en.wikipedia.org/wiki/Coverage_data)
e.g. _a digital representation of some spatio-temporal phenomenon_. Consuming coverage 
data and visualizing it interactively in web clients is still not straight-forward. 
One reason is that existing formats are either unsuitable for the web 
(like netCDF files) or hard to interpret independently due to missing standard 
structures and metadata (e.g. the OPeNDAP protocol).

[CoverageJSON](https://github.com/Reading-eScience-Centre/coveragejson/) 
is a data format for publishing coverage data to the web in a web-friendly way.

[Kilchattan](https://github.com/lewismc/kilchattan/) is a framework which creates
CoverageJSON from Coverage Data contained within SDF. This process is described 
simply as 'SDF-to-CoverageJson'. The framework generates JSON snippets from data
products which can then be embedded as linked data within (for example) [dataset
landing pages](http://go.nasa.gov/2ac81Oc).

## Example SDF-to-CoverageJSON Generation

As an example of what the output of Kilchattan is, lets take a look at 
the following example.
Here we take the [
Jason-1 Sensor Geophysical Data Record (SGDR) NetCDF](http://podaac.jpl.nasa.gov/dataset/JASON-1_SGDR_NETCDF) data product fro NASA JPl's PO.DAAC which enables us to understand 
measurments relating to Ocean Waves, Significant Wave Height, 
Sea Surface Topography and Sea Surface Height. In particular, we are interested 
in genrating CoverageJSON from this product because it has the following coverage
characteristics: 
 * Region: Global
 * Northernmost Latitude: 66.15 degrees
 * Southernmost Latitude: -66.15 degrees
 * Westernmost Longitude: 0 degrees
 * Easternmost Longitude: 360 degrees
 * Time Span: 2002-Jan-14 to 2012-Mar-03

Lets feed in the data product as a parameter to the kilchattan script
```
	$ wget "http://podaac-opendap.jpl.nasa.gov:80/opendap/allData/jason1/L2/sgdr_netcdf_c/c002/JA1_GPS_2PcP002_014_20020125_152010_20020125_155958.nc"
	$ python kilchattan.py JA1_GPS_2PcP002_014_20020125_152010_20020125_155958.nc
```
The output CoverageJSON will be written to the current working directory. Examples of
what this _may_ look like (and other CoverageJSON examples) can be found at the
[CoverageJSON Playground](https://covjson.org/playground/).


##What does the word Kilchattan mean?
**[Kilchattan Bay](https://en.wikipedia.org/wiki/Kilchattan_Bay)** is a village on 
the [Isle of Bute](https://en.wikipedia.org/wiki/Isle_of_Bute), 
[Scotland](https://en.wikipedia.org/wiki/Scotland). It lies the island's southern 
end, along the coast road at the foot of a steep hill called the _Suidhe Chattan_ 
which shields the village from the prevailing westerly wind. The village faces 
the mainland to the east across the 
[Firth of Clyde](https://en.wikipedia.org/wiki/Firth_of_Clyde). 
A sandy bay known locally as the _Wee Bay_ sweeps around to the north.

##License
Kilchattan is permissively licensed under the [Apache License v2.0](http://www.apache.org/licenses/LICENSE-2.0), a copy of that license is shipped with this software.

