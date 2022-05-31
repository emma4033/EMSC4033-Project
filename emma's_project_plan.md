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

_Give more details on the scientific problem that you are working on and how this project will advance the discipline or help with your own research.
(Where applicable, describe how people have been achieving this goal up to now, talk about existing packages, their limitations, whether you can generalise something to help other people use your code)._

## Resources & Timeline

_What do you have at your disposal already that will help the project along. Did you convince somebody else to help you ? Are there already some packages you can build upon. What makes it possible to do this project in the time available. Do you intend to continue this project in the future ?_

# maps with coral locations 
- maps created through cartopy

# coral data processing to produce accompaning time-series graphs:
- laser ablation data (trace metal analysis) can be processed through LAtools 
- SST data can be processed through xarray, cartopy, matplotlib
- radiocarbon data can be processed through 

## Testing, validation, documentation

- testing is vital -  notebook may run now, but with so many components coming together something will stop working with time, so you need to figure out how that will be addressed in the future.
- hide duplications (things users can break) - makes it harder to use but easier to read
- docstrings for how the user should upload the files

**Note:** You need to think about how you will know your code is correct and achieves the goals that are set out above (specific tests that can be implemented automatically using, for example, the `assert` statement in python.)  It can be really helpful if those tests are also part of the documentation so that when you tell people how to do something with the code, the example you give is specifically targetted by some test code.

_Provide some specific tests with values that you can imagine `assert`ing_
