# EMSC4033 project plan template

## Project title

## Executive summary

Allow the user to create maps focused on coastlines and ocean topography with coral sample locations specified and displayed with climate data from the coral samples. For example, the data from laser ablation analysis of coral core samples from Gladstone Harbour (past research I have done), or SST and radiocarbon analysis from coral core samples from Montebello Island (my current research).
- overlay the data collected from coral analysis with a map of the temporal and spatial changes in the region specific to what was being analysed.

- visualisation: combines climate research and climate data applications, branching the gap between proxy data attribution and the scientific process.


**Example:** _(this is based on the seismic monitoring dashboard that Louis showed). Seismic stations can be used to monitor human noise over the course of the day. Some seismometers stream data live to a server and so this processing can be done in near-real time. In this project I plan to build an online dashboard which processes the data once a day and uploads the results to github as 1) raw data, 2) an image that can be embedded in websites, 3) an updating csv table in github. I also plan to use the github "actions" engine to provide all the necessary processing power._

## Goals

- how to upload user data in a readable format - preparing the data for analysis
- how to create the graphs
- how to create the maps - identify the location and put down markers for the coral locations
- display this data in a visually appealing and easily digestable manner
- with the maps - need to balance interactive and static
- analysis of tools to use: Pandas, LAtools, Cartopy, 
- ingenuity in the design - what helped (i.e. course resources), what was troubleshooted, what was added to others packages e.t.c

Using Panda for easier data manipulation
- get in a form pandas can read - i.e. file shape/format
- testing - i.e. missing data from users: make error, leave it, plot it

(Write things that you can assess whether they have been accomplished. For example, a goal like “improve visualisation of ocean output” is vague... But a goal that reads “implement functionality to plot streamlines of horizontal velocities in various slices from 3D ocean output” is specific enough.)

## Background and Innovation  

Climate science and environmental studies rely on the analysis of data collected from records, including corals, ice cores, tree rings, and sediment samples. These physical samples can be used as proxies for environmental conditions, such as sea-surface temperatures, precipitation, and atmospheric carbon dioxide levels, going backwards in time. The proxy records provide this link to the more conceptual ideas of changing climate patterns, and are often limited to the region of collection. Pulling together data from multiple proxy records both within a region and globally, allows broader climate research to be conducted.

There is an abundance of programming software out there for the purposes of displaying data from proxy records, primarily as graphs. There is also an abundance of mapping programs for displaying regional to global scale maps in a range of resolutions. There is even some softwards specifically for displaying climate data on world maps, in the form of overlays and interactive maps. Being able to visually display the link between the scientific collection of environmental proxies and the results from analysing that data would aid the world of climate science in conveying key concepts to the general public.

My aim with this Notebook is to provide a way for scientists to easily produce a map with the proxy record collection location marked and the data displayed alongside in the form of graphs. This will be achieved by combining multiple python programming packages, such as cartopy, LAtools, Xarray, and matpltlib, and tuning them towards my goal. This Notebook is specific in the sense that it is targeted towards climate scientists for the novel use of proxy record location mapping, however, is general in the sense that multiple disiplines can utilise it for a range of applications such as journal papers, posters, and seminar presentations. 


## Resources & Timeline

Inspiration for this project came from using a python package called LAtools which allows the user to create graphs from Laser Ablation data (a form of mass spectrometry). I found LAtools quite difficult as a beginner programmer and the graphs it created were confusing without the spatial and temporal knowledge that it was showing from the original proxy records. By combining the applications of LAtools with other packages, such as cartopy, the data would be able to be displayed in an easier to understand manner. Further combination of other packages will allow a more general application of this Notebook, as more data can be displayed then just Laser Ablation data. At my disposal I have coral sample Laser Ablation data and some radiocarbon data, as well as the exact locations of the corals, which I can use to test my Notebook.


**maps with coral locations **
- maps created through cartopy

**coral data processing to produce accompaning time-series graphs:**
- laser ablation data (trace metal analysis) can be processed through LAtools 
- SST data can be processed through xarray, cartopy, matplotlib
- radiocarbon data can be processed through 

**Testing, validation, documentation**

- testing is vital -  notebook may run now, but with so many components coming together something will stop working with time, so you need to figure out how that will be addressed in the future.
- hide duplications (things users can break) - makes it harder to use but easier to read
- docstrings for how the user should upload the files

**Note:** You need to think about how you will know your code is correct and achieves the goals that are set out above (specific tests that can be implemented automatically using, for example, the `assert` statement in python.)  It can be really helpful if those tests are also part of the documentation so that when you tell people how to do something with the code, the example you give is specifically targetted by some test code.

_Provide some specific tests with values that you can imagine `assert`ing_
