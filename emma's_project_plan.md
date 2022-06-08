# EMSC4033 project plan template

## Project title

## Executive summary

My project is a tutorial notebook for beginner python users, specifically in the realm of marine science. The notebook produces two maps for the user; a general map centred on an ocean of choice by the user, and a focused map for a specific location (i.e. coastline or island topography). Each map allows the user to specify a latitude and location so a marker can be placed and named, intended to be used to mark the location of scientific sample location (e.g. coral cores, sediment cores, seawater capture etc.). 

These maps can be used by scientists to highlight the location of their research. Often in marine climate research the data collected is proxy data that links specific samples to the broader climate systems in the regions, for instance; coral proxies can infer sea-surface temperatures through time. Conveying such research to a general audience is tricky as it requires knowledge of proxies in a spatial and temporal manner. The maps produce by my Notebook aims to bridge the gap between physical climate research and the applications of climate data.

The notebook runs 6 functions, 2 I have written from scratch and 4 from the Cartopy gallery that I have added to and adapted. Instructions on using the functions is contained in the docstrings above each function. An example is already contained in the Notebook, with instructions on how to run the example and where to change the variables to make personalised maps. 


## Goals

1.	Produce a Notebook that introduces marine scientists to the world of python programming with Cartopy in a way that is useful and applicable to their research. 
2.	Use and create functions that produce two simple maps that highlights the location of the scientific samples in relation to the oceanic region in which they were collected. 


## Background and Innovation  

Climate science and environmental studies rely on the analysis of data collected from records, including corals, ice cores, tree rings, and sediment samples. These physical samples can be used as proxies for environmental conditions, such as sea-surface temperatures, precipitation, and atmospheric carbon dioxide levels, going backwards in time. The proxy records provide this link to the more conceptual ideas of changing climate patterns, and are often limited to the region of collection. Pulling together data from multiple proxy records both within a region and globally, allows broader climate research to be conducted.

There is an abundance of programming software out there for the purposes of displaying data from proxy records, primarily as graphs. There is also an abundance of mapping programs for displaying regional to global scale maps in a range of resolutions. There is even some softwares specifically for displaying climate data on world maps, in the form of overlays and interactive maps. Being able to visually display the link between the scientific collection of environmental proxies and the results from analysing that data would aid the world of climate science in conveying key concepts to the general public.

My aim with this Notebook is to provide a way for scientists to easily produce maps with the proxy record collection location marked. This will be achieved through the use of cartopy and matplotlib, and tuning them towards my goal. This Notebook is specific in the sense that it is targeted towards climate scientists for the novel use of proxy record location mapping, however, is general in the sense that multiple disiplines can utilise it for a range of applications such as journal papers, posters, and seminar presentations. 


## Resources & Timeline

Inspiration for this project came from using a python package called LAtools which allows the user to create graphs from Laser Ablation data (a form of mass spectrometry) from analysing coral samples. I found LAtools quite difficult as a beginner programmer and the graphs it created were confusing without the spatial and temporal knowledge that it was showing from the original proxy records. By combining the applications of LAtools with other packages, such as cartopy, the data would be able to be displayed in an easier to understand manner. Further combination of other packages (e.g. pandas, xarray and pyleoclim) will allow a more general application of this Notebook, as more data can be displayed then just Laser Ablation data. At my disposal I have coral sample Laser Ablation data and some radiocarbon data, as well as the exact locations of the corals, which I can use to test my Notebook. Unfortunately I was unable to add the graphing capabilities of python to my project and was only able to do the mapping side of my project. In the future I would like to add to this Notebook and allow the user to add graphs alongside their maps.

**Timeline**

-	tested out some resources for making maps specific to displaying climate data. This included a method of making a global map with an overlay of sea-surface temperature anomalies. 
-	spent a few days figuring out LAtools and how to apply it in a more user friendly manner for non-programming users. Unfortunately I was unsuccessful with my limited knowledge of python and gave up on the idea of implementing LAtools in my project in the limited time I have. 
-	trouble-shooted using pyleoclim as a resource for plotting paleogeoscientific data from LiPD data-sources. Also, xarray and pandas for graphing data, however, ran into similar issues and decided against graphs for my project with the limited time schedule.  
-	devoted the rest of my time developing the maps and how a beginner user could learn simple cartopy map making for a specific scientific purpose.
-	developed some simple testing functions within my notebook to check the user input is valid to run the functions.


**Review of Existing Code**

- LAtools

LAtools is a Python toolbox developed for the processing of Laser Ablation Mass Spectrometry (LA-MS) raw data in a standard manner, removing the need for manual processing. It processes data through signal de-spiking, background identification and subtraction, standard normalisation, and calibration. LAtools goes a bit further than other Laser Ablation processing packages by implementing filters for contaminant signal removal. 

Through using and testing LAtools I found the most difficult aspect of the toolbox is in uploading user data. LAtools requires the data to be in a specific format for processing. The method provided for splitting data files into the correct format was difficult to understand and ended with me manually splitting my data in excel. 

I hope to use LAtools in the future as a means to easily produce graphs of laser ablation data.

- Cartopy

Cartopy is useful for simple mapping specific for scientific data visualisation, making it ideal for the goal of my Notebook. To better visualise scientific data in relation to the spatial aspects of data collection, two options will be available for the user; a wider region with location marker (i.e. country area) and more distinct region location marker (i.e. to highlight topography features). 

**First map option**
I have adapted a function from the Cartopy Gallery that creates a simple map with the ability to specify a location marker and name based on latitude and longitude input by the user. This map requires user input for the global location, which I have simplified to a list of areas. The purpose of this map is for global visualisation, intended to broaden the impact of spatial consideration for scientific sample collection. I tested a few different versions of map creation styles from the Cartopy Gallery, including different projections, topography styles, and features
-	used cartopy features (cartopy.feature) and tested combinations. Settled for rivers, oceans, land, borders, coastlines and states_provinces, for the final map.
-	tested some map tiles, however, for the broader map the generic cartopy topography is a simple option that highlights the location.
-	made a dictionary for easy creation of maps based on the 5 world oceans. This centers the focus on oceans instead of land, which is important for linking marine science to its applications.

**Second Map option**
-	a more specific map option that requires the knowledge of the latitude and longitude of the map.
-	use NaturalEarth tiles for the higher resolution smaller scale maps required to highlight features such as topography and coastlines.


**Testing, validation, documentation**

- docstrings are contained with each function and file upload, for how the user should upload the files and use the functions.
- there is a test in the ocean_maps.ipynb for the function I created to extract data from the dictionary of ocean latitudes and longitudes. This test tells the user which projection is being used for the main map and why projection specification is important.
- There is another test for the location marker code called check_location_marker that ensures the user input is coordinates.

**Limitations and further development**

My maps are limited in there complexity, which is useful for beginner programmers, however branching off from this Notebook into more complex map making capabilities is not plausible and the Cartopy Gallery resource is recommended. Further innovation of this Notebook could be done to make it more applicable and stylish for marine scientists, such as including marking of ocean features, such as major currents and ocean circulation. 

