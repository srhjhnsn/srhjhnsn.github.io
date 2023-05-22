---
title: "GES 486 Final Project: An Analysis of Mothman Sightings in Point Pleasant, WV from 1966-1967"
excerpt: "Mothman is a cryptozoological creature that terrororized the citizens of Point Pleasant, WV and surrounding areas between 1966-1967. Here, I present an analysis of the sighings I could find information about. Image of Mothman Statue in Point Pleasant from [The Charleston Gazette](https://www.wvgazettemail.com/arts_and_entertainment/annual-mothman-festival-makes-point-pleasant-a-paranormal-paradise-this-weekend/article_1a0652dc-d480-5c2e-809a-5db33dd90f7d.html) <br/><img src='/images/mothman_statue.jpg'>"
collection: portfolio
---
## **Introduction**

### ***Who is Mothman?***

Mothman is a humanoid, cryptozoological creature with moth-like features, most notably having bright red eyes and large moth wings. He is a part of modern West Virginia folklore; sightings started in November of 1966 in Point Pleasant, West Virginia and came to a stop in December, 1967 after the collapse of the [Silver Bridge]( https://en.wikipedia.org/wiki/Silver_Bridge).

### ***TNT Area***

There have been many sightings at and around the site of a former World War II munitions plant called the West Virginia Ordnance Works, also known as the “TNT Area”. After WW2 ended, the government deeded the area to the state of West Virginia under the stipulation that it would become a wildlife management area. And so, in 1945, the McClintic State Wildlife Management Area was created (EPA, 2023). The area was put on the National Priority List (NPL) in 1983 due to the heavy pollution, making it eligible for government assisted cleanup through the Superfund Program. At the time, it was in the top 10 most polluted sites in the United States. As of 2007, it has still not been fully cleaned (Wikipedia Contributors, 2021).

### ***Speculations***

Some have attributed the creation of the Mothman to the TNT Area’s pollution, meaning that the toxic chemicals created some sort of mutation. Some also believe that the TNT area is Mothman’s home. Author John Keel relates sightings as premonitions to the collapse of Silver Bridge in December 1967, which is when sightings from this time came to a halt. Mothman has since made Point Pleasant a tourist attraction, with a museum, statue, and several Mothman themed places, and even a festival. 
Whether Mothman is real or not, if it was mass hysteria, or if Mothman was a premonition to the 1967 Silver Bridge collapse, I find the topic to be fascinating and thought it would be interesting to do an geographic analysis of Mothman sightings.

## **Methods**

### ***Data Source***

The data I used came from 2 books, *The Mothman Prophecies* by J. A. Keel, and *Mothman: The Facts Behind the Legend* by D. Sergent and J. Wamsley. I read and tabbed both books, noting sightings and other interesting information that could be relevant to this analysis. It is worth noting that my data set is most likely incomplete, as there are many sightings that did not reach the news or these books that I could not attain more information on.

### ***Analysis***

After the books were read and tabbed, I extracted the sightings into an Excel spreadsheet, converted into a .csv file, and loaded into R, where the points were given geometry and converted into a .shp file. For the locations of each sighting, I estimated based on the description of the event. Some were specific enough to pinpoint an exact location, but others were more vague so I gave my best educated guess based on the context. 
	
The TNT area is very relevant to this analysis, so I created a polygon of the NPL’s boundary of the Superfund Site as of 1994 to use based off an image from the Wikipedia site for [West Virginia Ordnance Works](https://en.wikipedia.org/wiki/West_Virginia_Ordnance_Works#).

I used RStudio to create bar graphs of various factors of the sightings, such as Mothman’s color, height, and wingspan, as well as the day of the week and time of day of the sightings. These graphs individually excluded any sightings that didn’t have information for the respective category. I picked color, height, and wingspan to see how much witness’s accounts of his appearance were alike. Time of day was chosen because I was curious to see when Mothman tended to appear. Author John Keel noted something in his book called the Wednesday effect, in which he did an analysis of odd events such as UFO sightings and Mothman sightings and determined that they tended to fall on Wednesdays. I wanted to see if the data I collected aligned with this theory.

I then used QGIS to create 3 maps. The first map I made was a Web Map of all sightings I had information about. The points include descriptions of the event, location, witness name, and how many people were present at the time of the event. I also included the NPL Boundary polygon and background information about it as a Superfund Site. The second map I created was a heatmap of the sightings in the Point Pleasant area, and the third was a map depicting the proximity of each sighting to the TNT area, based on the NPL boundary. Both of these maps used the polygons acquired from TIGRIS, and the shapefile I made of the Silver Bridge.


## **Results**

### ***Heatmap***
<br/><img src='/images/mothman_heatmap.jpeg'>

This is a heatmap of the approximate locations of each sighting. In this area, they seem to be concentrated in and around the TNT Area. This map excludes sightings outside of the Point Pleasant Area.

### ***Proximity to TNT Area***
<br/><img src='/images/mothman_proximity_map.jpeg'>
<br/><img src='/images/mothman_proximity_chart.png'>

This map depicts the proximity of each sighting in the Point Pleasant area to the TNT area in half mile intervals. The chart breaks down the percentage of the sighting’s proximity, combining the previous category to the next. For example, the <1 mile category includes the sightings inside the TNT area and sightings <0.5 miles away.

### ***Bar Charts***
<br/><img src='/images/mothman_chart_layout.jpg'>

These bar charts depict different aspects of the sightings. Specifically, attribtues of Mothman's appearance and details of the timings of sightings

### ***Web Map***
<iframe src="https://srhjhnsn.github.io/portfolio/mothman_webmap/index.html" width="750" height="750" style="border:0" allowfullscreen></iframe>

This is the link to the Web Map, which depicts the locations of all the Mothman sightings I could find in the 2 books, including the ones outside of the Point Pleasant area.

## **Discussion**


## **References**

EPA. (2023). WEST VIRGINIA ORDNANCE (USARMY) | Superfund Site Profile | Superfund Site Information | US EPA. https://cumulis.epa.gov/supercpad/SiteProfiles/index.cfm?fuseaction=second.cleanup&id=0303066

Keel, J. A. (2002). The Mothman Prophecies: A True Story. Tor Books.

Romain, L. (2020, August 5). What Is the Mothman and Why Are We So Obsessed? - Nerdist. Nerdist. https://nerdist.com/article/mothman-why-we-are-so-obsessed/

Sergent, D., & Wamsley, J. (2002). Mothman: The Facts Behind the Legend. Mothman Lives Publishing.

Wikipedia contributors. (2023). Mothman. Wikipedia. https://en.wikipedia.org/wiki/Mothman#

Wikipedia contributors. (2021). West Virginia Ordnance Works. Wikipedia. https://en.wikipedia.org/wiki/West_Virginia_Ordnance_Works#
