# Kilchattan

<img src="https://github.com/lewismc/kilchattan/blob/master/docs/a-sunny-day-in-kilchattan-bay.jpg" align="right" width="300" />

Kilchattan is a [Scientific Data Formats](http://fileformats.archiveteam.org/wiki/Scientific_Data_formats)
(SDF)-to-[CoverageJSON](https://github.com/Reading-eScience-Centre/coveragejson/) generation framework.

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

[Kilchattan](https://github.com/lewismc/kilchattan/) is a framework which assists
in producing CoverageJSON from Coverage Data contained within SDF.

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

