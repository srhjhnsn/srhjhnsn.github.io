---
title: "Summer 2024 Internship at SSAI/NASA: Environmental Impacts of Urban Growth - Urban Heat"
excerpt: "The results of my internship project, where I compared Landsat data and NLCD Land Cover data to find how urban change has affected temperatures in the DMV.
Photo: NLCD Land Cover around Dulles International Airport, 2021 <br/><img src='/images/su24_preview.png'>"
collection: portfolio
---
## **Introduction**
Over the last several decades, there has been a tremendous amount of urban growth in the Baltimore-Washington Metro area (4). Due to this rapid urban expansion, there has also been an increase of urban heat.

Urban heat is the heightened temperatures that cities and urban areas experience in comparison to their nearby rural areas. The difference in temperature is caused by a multitude of factors, namely the radiative and thermal properties of impervious surfaces (1).

The purpose of this study was to analyze the 22 counties and independent cities chosen in the Baltimore-Washington Area and quantify the change in surface temperature in relation to urban growth between 2001-2021.

## **Data and Methods**
- NLCD Land Cover (LC) Data from USGS from the following years:
  - 2001, 2021, 2001-2021 Land Cover Change Index (LCCI)
- Landsat 5 and 8 Level 2 Thermal Infrared data from the following years:
  - 2001-2003 (L5), 2021-2023 (L8)
- Google Earth Engine was used to acquire and process the Landsat Data
  - 06/01 to 09/15 dates to get maximal summer temperatures
- Composites were made for each set of data, taking the median surface temperature in Celsius
- Difference raster created from the 2001-2003 and 2021-2023 composites
- Referenced code from previous and similar work to help structure this code2.
- Zonal Statistics using NLCD LC Change Index and Mean Temperature Change to quantify change in surface temperature based on urbanization
- Anything classified as Open Water in 2021 was masked out of all calculations to avoid skewed numbers in counties bordering large bodies of water.

## **Results**
<img src='/images/su24_fig1.png' width="800"><br/>
Fig. 1: Comparison of NLCD LC and Median Surface Temperature around Dulles International Airport (IAD) This area includes Loudoun, Fairfax, and Prince William Counties in VA. Also visible is Montgomery County, MD and Fauquier County, VA. This comparison’s purpose is to show the spatial overlap between new urban developments and surface temperature increases in more detail than shown in Fig. 2. This figure also visually shows the overall increase of temperature over time, which was calculated to be 3.317°C ± 0.001 (see Fig.5).

<img src='/images/su24_fig2.png' width="800"><br/>
Fig. 2: An overlapping comparison of NLCD LCCI - Urban Change (2001-2021) and Median Surface Temperature Change (2001-2023) in the whole 22 county study area. In this map, we can see new urban heat islands that have formed, which spatially overlap with high increases in surface temperature.

<img src='/images/su24_fig3.png' width="800"><br/>
Fig. 3: Bar chart depicting change in surface temperature, separated into urban growth areas, non-urban change or no change areas, and the average of the whole county/independent city. Right vertical axis displays the area (Ha) of urban growth in each county/independent city. Independent cities were also noted with a * since they have less area of urban growth due to being previously urbanized and/or being smaller in total area. These were calculated using Zonal Statistics with the NLCD LCCI and Median Surface Temperature Change.

<img src='/images/su24_fig4.png' width="800"><br/>
Fig. 4: NLCD LC Data from 2001 and 2021 was compared to see how much change occurred in each LC Class in the study area. The classes with the most net gain are all four Development classes and Cultivated Crops. The classes with the most net loss are Deciduous Forest and Hay/Pasture.

<img src='/images/su24_fig5' width="800"><br/>
Fig. 5: Table containing the mean temperature changes by county. These were calculated using Zonal Statistics with the Median Temperature Change raster and NLCD LCCI Urban Change and Non-Urban Change separated by county. Also included is the area of urban change per county, which can be found visually displayed in Fig. 3.

## **Discussion and Further Research**
- Every county/independent city had a larger temperature increase in areas with urban growth than the other areas in the county
- The counties where there has been urban growth surrounding Dulles International Airport (Loudoun and Prince William) have the highest urban growth related surface temperature increase (see Fig. 3). This could be due to the very large area of urban expansion, which could be causing a more intense Urban Heat Island effect.
- Cities that were previously urbanized experienced less urban growth, however the temperature increases in those areas were still similar to counties with lots of urban growth.
- Previous research shows that loss of forest land cover had a more extreme effect on heat increase5. This may prove to be true in Charles County, which is heavily forested. There is a minimal urban change with a large increase in surface temperature in the new urban developments (see Fig. 3). A potential subject of further research could be to find which LC changes have the most effect on surface temperature for this study area
- Historically, there has been a disproportionate exposure to heat among low income communities and communities of color (3). The next step in this research would be to incorporate socio-economic census data to see how urban heat as a result of urban growth has affected these communities.
- Due to differences in satellite calibrations between Landsats 5 and 8, results may be more extreme than reality.

## **References**
1. (2022). ARSET - Satellite Remote Sensing for Measuring Urban Heat Islands and Constructing Heat Vulnerability Indices. NASA ARSET http://appliedsciences.nasa.gov/get-involved/training/english/arset-satellite-remote-sensing-measuring-urban-heat-islands-and
2. Google Earth Engine code from Eleanor Horvath
3. Hsu, A., Sheriff, G., Chakraborty, T. et al. Disproportionate exposure to urban heat island intensity across major US cities. Nat Commun 12, 2721 (2021). https://doi.org/10.1038/s41467-021-22799-5
4. Sexton, J. O. et al. (2013). Urban growth of the Washington, D.C.–Baltimore, MD metropolitan region from 1984 to 2010 by annual, Landsat-based estimates of impervious cover. Remote Sensing of Environment, 129, 42–53. https://doi.org/10.1016/j.rse.2012.10.025
5. Slides from Explore Earth CCRI: Connecting Changes in the Local Urban Fabric to Global Climate Change

