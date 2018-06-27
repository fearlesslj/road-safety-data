# road-safety-data
Data science visualisation project on a UK Road Safety dataset
-----

**Note:** While the matplotlib graphs will show up even without running the notebook, the bokeh visualisations and the interactive elements will not work unless one runs the notebook locally. This repository does not contain the data files that were over the github 25MB limit, so for many of the visualisations to work the following two dataset zip files will need to be downloaded and unpacked in the notebook folder.

2005-2014 data: http://data.dft.gov.uk.s3.amazonaws.com/road-accidents-safety-data/Stats19_Data_2005-2014.zip     
1979-2004 data: http://data.dft.gov.uk/road-accidents-safety-data/Stats19-Data1979-2004.zip

Full dataset repository: https://data.gov.uk/dataset/cb7ae6f0-4be6-4935-9277-47e5ce24a11f/road-safety-data

Jupyter Notebook Introduction:
-----

Every year, the UK Department for Transport publishes a detailed record of all road accidents that were reported to the police and their details, containing everything from the location, conditions and severity of each individual accident to the type of vehicles involved and characteristics of the casualties. The resulting data has been recorded since 1979 and compiled into a fairly large publicly accessible dataset on the governmental data website (data.gov.uk). Road safety is a common concern for the government, the public and a significant number of private companies alike: an analysis of this dataset could grant us insights into the problem that could, for example, inform government policy and transport regulations, promote safer driving habits for individual drivers or highlight relevant areas of safety development for car manufacturers. In the following, we will carry out an exploratory analysis of the data to find some of its more interesting features and use some Python data visualisation tools to display them in an informative and attractive way.

Before we start, a quick note on the data itself: it comes as a collection of CSV files split into periods, namely 1979 to 2004, 2005 to 2014 and individual files for 2015 and 2016 (the 2017 is unavailable since the records are published in the autumn of the subsequent year). Furthermore, the data for each period is itself split into three CSV files:

* an "Accidents" file containing most of the essential data (such as the time, date and location of the accident, number and severity of casualties or road conditions),
* a "Vehicles" file describing the vehicles involved in the accident (including things such as the type of vehicle, its age or what kind of manoeuvers it was involved in at the time; some of the later years also have individual related "Make/Model" files that additionally list the make and model of the vehicles involved),
* a "Casualties" file detailing the accident's casualties (including, for example, their age, sex, type and the severity of their injuries).

The data itself is recorded with the codes corresponding from the police form (entitled STATS19) that is used to compile it rather than textual descriptions, which are available in the look-up table provided (Road-Accident-Safety-Data-Guide.xls). More detailed definitions of some of the terms can be found here. Finally, the first column in each file ('Accident_Index') provides a unique identifier for each individual accident that can be used as a key to join the various files on.
