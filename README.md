# Undergraduate-Research-2
## Abstract
The discovery of a low-amplitude long-term slow slip event (SSE) has filled the spatial gap between the locked zone and the ETS zone within the Cascadia subduction zone (CSZ). Apart from this event, three transient-like signals were observed. Their surface deformations are at noise levels, making it difficult to determine whether they are of tectonics. Potentially, oceanic loading can cause crustal deformation and generate akin to those previously observed. In this study, we focus on poorly resolved surface deformation transients detected in southern Washington, northern Oregon, and northern California. Our method involves analyzing sea level data from NOAA and GNSS measurements to assess the correlation between water level fluctuations and observed signals. Through correlation coefficient analysis, we aim to determine whether these events are of tectonic origin, environmental loading, or artifacts. The results reveal inconsistent correlation intervals within each state, suggesting a nuanced relationship between oceanic loading and surface deformation. However, the observed signals in the three regions are unlikely to be attributed to oceanic loading, supporting their tectonic origin. 
## Introduction
With the advent of high-sensitivity seismic observation networks and the global navigation satellite system (GNSS) observation networks, aseismic slip phenomena known as slow earthquakes have been discovered. Slow earthquakes are an intermediate type of fault slip between regular earthquakes and stable sliding (Obara & Kato, 2016). The mechanism of slow earthquakes is the same as that of regular earthquakes, except for their longer duration. Slow earthquakes are sometimes accompanied by seismic emissions called tremor (Beroza & Ide, 2011). Such slow earthquakes can be divided according to their characteristic time scale: short-term SSEs with durations of days to weeks or long-term SSEs with durations of months to years (Obara & Kato, 2016). 

The Cascadia subduction zone (CSZ) lies off the west coast from Northern Vancouver Island to Cape Mendocino, California. The CSZ is a convergent plate boundary where the Juan de Fuca, Explorer, and Gorda plates subduct underneath the North American plate. Numerous phenomena are observed within this region, such as megathrust earthquakes, with the most recent event in the year 1700 (Satake et al., 1996). While the CSZ produces lower levels of seismicity than other subduction zones, there are abundant slow slip and low-frequency tremors, commonly known as episodic tremor and slip (ETS) in the downdip zone of the seismogenic zone (Dragert et al., 2004). ETS is located downdip from the locked zone of the subduction plate interface between 25- and 45-km-depth contours (Peng & Gomberg, 2010). 

SSEs play an essential role in accommodating relative plate motion and transferring stress to the seismogenic zone. Uchida et al. (2016) studied periodic slow slip events in northern Japan and found they preceded or coincided with large earthquakes, contributing to periodic stress perturbations and subsequent seismic events. These similar scenarios can be seen elsewhere. For instance, in northern Chile, a SSE was detected less than a month before the 2014 Mw 8.2 Iquique earthquake took place in the same region (Ruiz et al., 2014). Long-term SSEs may also trigger tremors in the adjacent downdip zone, as observed in the Bungo channel and Mexico (Obara & Kato, 2016). Even more, long-term SSEs may have triggered the subsequent short-term SSEs–as observed in New Zealand (Wallace et al., 2012). ​​Given their potential to load the locked zone and trigger large earthquakes, studying SSEs in the CSZ is crucial for understanding the seismic cycle.

Although long-term SSEs (e.g., in Nankai) are numerically modeled to occur between the locked zone of megathrust events and the regions where ETS or short-term SSEs occur (Matsuzawa et al., 2013), Hyndman (2013) identified a spatial gap between the downdip limit of seismogenic zone and the ETS zone. Subsequently, Nuyen and Schmidt (2021) examined the long-term SSEs in Cascadia. However, cm-scale surface deformation was not observed through the GNSS time series in Cascadia. Instead, they proposed the possible low-amplitude SSEs (i.e., mm-scale surface deformation). After examining the gap, they discovered the low-amplitude long-term slow slip in Cascadia through careful filtering to remove relevant signals from noise, short-term SSEs, and secular tectonics. They concluded that non-tectonic events (e.g., soil moisture or snow water equivalent) were unlikely to explain the transient signals. One long-term SSE in southern Cascadia and three poorly resolved events were detected.

In this study, we investigate three poorly resolved surface deformation transients identified in southern Washington, northern Oregon, and northern California. Our goal is to examine these transients using sea level data (from tide gauge observations) and assess the correlation between this dataset and the observed signals. Essentially, ocean tides load the crustal surface, resulting in small displacements up to several mm for both horizontal and vertical directions, as seen in Alaska (Martens & Simons, 2020). 

By analyzing the relationship between water level fluctuations and the detected transients, we can determine whether these signals are of tectonic origin (i.e., SSEs), environmental loading of the crust, or artifacts. This analysis will provide insights into the nature of these events and their implications for understanding seismic processes in the CSZ.

 ![Alt text](https://github.com/Benz-Poobua/Undergraduate-Research-2/blob/main/Station%20Map.png)
Figure 1. The GNSS (pink pins) and NOAA (yellow pins) stations are located along the Cascadia along with the plate boundaries from the USGS Earthquake Hazards Program
(https://www.usgs.gov/programs/earthquake-hazards/google-earthtmkml-files) 
## Methods
The Global Navigation Satellite System (GNSS) data from the Pacific Northwest Geodetic Array (PANGA) are used to measure the deformation of the surface.  Sea level data from the National Oceanic and Atmospheric Administration (NOAA) measure fluctuation of the water height relative to the land.  In this study, we are interested in and utilize the cleaned GNSS data in the east component. Water Level data from NOAA are resampled using a sampling rate of 24 hours to obtain daily water-level data. We remove the high-frequency noise by applying a 30-day moving average for both datasets. To compare the two data sets, we calculate the correlation coefficient using the Python library (NumPy). Setting a one-year window on those derived datasets, we can calculate the correlation between the GNSS and water level data in each timeframe. Correlation coefficients close to 0 suggest that the signals are of tectonic origin, while those close to 1 or -1 imply the tidal loading effects.

To compare these two parameters (displacements and water level), GPS stations are paired with the nearest NOAA stations (Figure 1; Table 1). The comparison between the GPS and water level data is shown in Fig S1. The timeframe of interest for these pairs spans plus or minus two years from the observed events (Nuyen & Schmidt, 2021) in each state: Washington (2015 to 2020), Oregon (2006 to 2011), and California (2015 to 2020). Missing data and artifacts resulting from equipment changes are considered, leading to the truncation of some datasets. Details of each station and access to raw data are available in the Supplementary Data.
| GNSS stations  | NOAA stations |
| ------------- | ------------- |
| PABH  | Westport  |
| LWCK  | Cape Disappointment  |
| CHZZ  | Garibaldi  |
| ONAB  | South Beach  |
| PTSG  | Crescent City  |
| TRND  | North Spit  |
| P059  | Arena Cove  |
| P193  | Point Reyes  |

Table 1. The pairs of GNSS and NOAA stations used to compare their correlation between the surface displacements and water level variation.

## Results
Each panel displays correlation coefficients and GPS data for comparison (Fig. 2A: Washington, Fig. 2B: Oregon, and Fig. 2C: California). We set arbitrary thresholds for the correlation coefficients at ± 0.75. Highlighted in green are intervals where these values exceed the threshold. In Washington, correlation coefficients between Cape Disappointment-LWCK exceed -0.75 during the winter months of 2016 and 2017. However, in Oregon, correlation coefficients do not exceed 0.75 in the specified time interval. Conversely, in California, North Spit-TRND correlation coefficients surpass the threshold in January 2019. Additionally, Arena Cove-P059 correlation coefficients exceed during the winter months of 2016 and 2017. 

![Alt text](https://github.com/Benz-Poobua/Undergraduate-Research-2/blob/main/Corr_gps_WA.jpeg)
![Alt text](https://github.com/Benz-Poobua/Undergraduate-Research-2/blob/main/Corr_gps_OR.jpeg)
![Alt text](https://github.com/Benz-Poobua/Undergraduate-Research-2/blob/main/Corr_gps_CA.jpeg)
Figure 2. The correlation coefficient of the GPS and water level data (blue lines) compared with the surface displacements (red lines). The green regions represent the intervals where the coefficients exceed the arbitrary thresholds of ± 0.75: (A) Washington, (B) Oregon, and (C) California.  
## Discussion
Some missing data in the original datasets were filled using interpolation in the Python function. However, the moving average also resulted in missing data in the first and last terms based on the window used. Additionally, recent station settlements caused some missing data. For example, the ONAB station began operating in late 2008, so data before that time are unavailable.

The consistency observed in water level data within each state suggests minimal variation in tidal loading across the region, indicating that the uncertainty associated with selected NOAA stations within a state is negligible. However, the surface displacement data from GNSS stations exhibit variability within states, potentially attributable to geological factors such as the segmentation of subducting velocity and local lithological features.

If we were to hypothesize that tidal loading is responsible for the poorly resolved signals, we would expect consistent correlations between GPS and NOAA data within a state at similar times, irrespective of the surface displacement variation, with high correlation coefficients greater than ± 0.75. Higher correlation coefficients close to 1 or -1 indicate a non-tectonic origin, such as tidal loading, while coefficients close to 0 suggest a tectonic origin. 

However, the intervals where correlation coefficients exceed the arbitrary threshold differ among pairs within states. Consequently, the observed signals in southern Washington, northern Oregon, and northern California, as identified by Nuyen and Schmidt (2021), cannot be attributed to oceanic loading, supporting the idea that these three transients are of tectonic origin. 
## Conclusion 
In conclusion, our study explored the connection between oceanic loading and surface deformation by analyzing GNSS and NOAA data. However, inconsistent correlation intervals within each state suggest a more nuanced relationship. Previous research on regional soil moisture and snowpack variation, coupled with findings on tidal loading from our study, reinforces the notion that transient signals are predominantly tectonic in nature.
## References
Beroza, G. C., & Ide, S. (2011). Slow earthquakes and nonvolcanic tremor. Annual review of Earth and planetary sciences, 39, 271-296. https://doi.org/10.1146/annurev-earth-040809-152531  

Dragert, H., Wang, K., & Rogers, G. (2004). Geodetic and seismic signatures of episodic tremor and slip in the northern Cascadia subduction zone. Earth, planets and space, 56(12), 1143-1150. https://doi.org/10.1186/BF03353333  

Hyndman, R. D. (2013). Downdip landward limit of Cascadia great earthquake rupture. Journal of Geophysical Research: Solid Earth, 118(10), 5530-5549. https://doi.org/10.1002/jgrb.50390  
Martens, H. R., & Simons, M. (2020). A comparison of predicted and observed ocean tidal loading in Alaska. Geophysical Journal International, 223(1), 454-470. 
https://doi.org/10.1093/gji/ggaa323  

Matsuzawa, T., Shibazaki, B., Obara, K., & Hirose, H. (2013). Comprehensive model of short‐and long‐term slow slip events in the Shikoku region of Japan, incorporating a realistic plate configuration. Geophysical Research Letters, 40(19), 5125-5130. 
https://doi.org/10.1002/grl.51006  

Nuyen, C. P., & Schmidt, D. A. (2021). Filling the gap in Cascadia: The emergence of low‐amplitude long‐term slow slip. Geochemistry, Geophysics, Geosystems, 22(3), e2020GC009477.​ https://doi.org/10.1029/2020GC009477  

Obara, K., & Kato, A. (2016). Connecting slow earthquakes to huge earthquakes. Science, 353(6296), 253-257. https://doi.org/10.1126/science.aaf1512  

Peng, Z., & Gomberg, J. (2010). An integrated perspective of the continuum between earthquakes and slow-slip phenomena. Nature geoscience, 3(9), 599-607. 
https://doi.org/10.1038/ngeo940  

Ruiz, S., Metois, M., Fuenzalida, A., Ruiz, J., Leyton, F., Grandin, R., ... & Campos, J. (2014). Intense foreshocks and a slow slip event preceded the 2014 Iquique M w 8.1 earthquake. Science, 345(6201), 1165-1169. https://doi.org/10.1126/science.1256074  

Satake, K., Shimazaki, K., Tsuji, Y., & Ueda, K. (1996). Time and size of a giant earthquake in Cascadia inferred from Japanese tsunami records of January 1700. Nature, 379(6562), 246-249. https://doi.org/10.1038/379246a0   

Uchida, N., Iinuma, T., Nadeau, R. M., Bürgmann, R., & Hino, R. (2016). Periodic slow slip triggers megathrust zone earthquakes in northeastern Japan. Science, 351(6272), 488-492. https://doi.org/10.1126/science.aad3108  

Wallace, L. M., Beavan, J., Bannister, S., & Williams, C. (2012). Simultaneous long‐term and short‐term slow slip events at the Hikurangi subduction margin, New Zealand: Implications for processes that control slow slip event occurrence, duration, and migration. Journal of Geophysical Research: Solid Earth, 117(B11). https://doi.org/10.1029/2012JB009489   

## Supplementary Data
1. Datasets and Script
Cleaned data in the CSV format and script (Jupyter Notebook) analyzing the correlation between the GNSS data and water level data are available at
https://github.com/Benz-Poobua/Undergraduate-Research-2/tree/main. 

2. GPS data
We use the post-processing cleaned data with linear trends, steps from known earthquakes or equipment changes, and annual and semi-annual sinusoidal signals removed from the GPS time series provided by the Pacific Northwest Geodetic Array (PANGA), Central Washington University, via https://www.geodesy.org/data/bysite/. Also, the file named gps_pre.sh is used to clean the data and provide it in CSV format. 

3. NOAA data
Water level data can be accessed at https://tidesandcurrents.noaa.gov/. We use the settings to obtain the raw data: Units = Standard, Timezone = GMT, Datum = MLLW, Interval = 1 hour. 

   


