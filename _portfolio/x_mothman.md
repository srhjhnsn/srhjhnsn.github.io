---
title: "GES 486 Final Project: An Analysis of Mothman Sightings in Point Pleasant, WV from 1966-1967"
excerpt: "Mothman is a cryptozoological creature that terrororized the citizens of Point Pleasant, WV and surrounding areas between 1966-1967. Here, I present an analysis of the sighings I could find information about. Image of Mothman Statue in Point Pleasant from [The Charleston Gazette](https://www.wvgazettemail.com/arts_and_entertainment/annual-mothman-festival-makes-point-pleasant-a-paranormal-paradise-this-weekend/article_1a0652dc-d480-5c2e-809a-5db33dd90f7d.html) <br/><img src='/images/mothman_statue.jpg'>"
collection: portfolio
---
## **Methods**

### ***Data Source***

The data I used came from 2 books, *The Mothman Prophecies* by J. A. Keel, and *Mothman: The Facts Behind the Legend* by D. Sergent and J. Wamsley. I read and tabbed both books, noting sightings and other interesting information that could be relevant to this analysis. It is worth noting that my data set is most likely incomplete, as there are many sightings that did not reach the news or these books that I could not attain more information on.

### ***Analysis***

After the books were read and tabbed, I extracted the sightings into an Excel spreadsheet, converted into a .csv file, and loaded into R, where the points were given geometry and converted into a .shp file. For the locations of each sighting, I estimated based on the description of the event. Some were specific enough to pinpoint an exact location, but others were more vague so I gave my best educated guess based on the context. 
	
The TNT area is very relevant to this analysis, so I created a polygon of the NPL’s boundary of the Superfund Site as of 1994 to use based off an image from the Wikipedia site for [West Virginia Ordnance Works](https://en.wikipedia.org/wiki/West_Virginia_Ordnance_Works#).

## **Results**
![](/images/mothman_heatmap.jpg)

