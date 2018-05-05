## GROUP 3 - FINAL PROJECT

# IS MUSIC TOO LOUD IN MANHATTAN?

## INTRODUCTION

Prof. Saldarriaga proposed an idea during one of the first lectures in the course, which was "visualizing the sounds of the city." People live in modern city are surrounded by all kinds of noises today. Where and when do people complain more about noise? Our project, Is Music Too Loud in Manhattan, focuses on visualizing the clusters of loud music complaints in different neighborhoods in Manhattan in 2017, based on the 311 Service Requests from 2010 to Present. The result may surprise you.  

Loud music is the most complained noise no matter in Manhattan or the rest of city. Notably, our research shows that the noise complaints increase significantly along Broadway where theaters, traffic and active human activities gathered. The number of the complaints changes along Broadway; however, the number of complaints change does not varies much during different seasons. 

Our project displays our findings of the loud music complaints in different neighborhoods along Broadway and the demographic characters of these neighborhoods. Viewers can also see the variations of complaints numbers from neighborhood to neighborhood during different seasons. The total complaint number of each neighborhood will show up by clicking the bubble of complaint.

## PROCESS   

### CHOOSE DATASETS     

Before we determined to research the noise complaint, we search the internet for available dataset about noise. As we desire to show the spatial variances of noise in Manhattan, the dataset must have location information which can be identified in ArcGIS. However, at the beginning of our research we encountered that the available data sets were scarce, which prompted us to look for a means to find indirect insigths into the soundscape of the city. This in turn, brought our attention to the data for noise complaints reported to _311_ in 2017. This dataset has rich information and expresses people’s feelings about surrounding noise. 

Besides the distribution of noise complaint in the aspects of space and time, we also wnant to find out the context of people’s complaints. We searched and downloaded the census tract demographic data in NYC Open Data.

Datasets:

Noise Complaint Dataset

https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9 

Neighborhood Demographics

https://factfinder.census.gov/faces/nav/jsf/pages/searchresults.xhtml?refresh=t

Neighborhood Tabulation Area

https://data.cityofnewyork.us/City-Government/Neighborhood-Tabulation-Areas/cpf4-rkhq/data

Lion Dataset

https://www1.nyc.gov/site/planning/data-maps/open-data/dwn-lion.page

### EXPLORE THE DATA    

#### Jialin Zhai, jz2893 & Qianyu Xiang, qx2170 & Kate Wang, kw2673   

At first, we look at the general distribution of noise complaint in space, time and category. Our statistics suggest that most of the complaints clustering in Manhattan and Brooklyn. After careful consideration the team decided to narrow the focus of our analysis over music complaints in Manhattan, since the data set was too rich for the given time constraints and scope of our final assignment. We focused on music complaints because they comprise _47%_ of the total number of noise complaints in Manhattan, and greatly outnumber the second-most common type of complaint, which is construction sounds, by an almost twofold margin. For the purpose of specificity, we decided to analize the loud music complaints throughout an area that would cover Manhattan from North to South, which is why we chose to follow the trail of complaints over the length of _Broadway Avenue_. 

<img width='971' alt='123' src="https://github.com/dataviz2018/final-group3/blob/master/chart1.png">

<img width='971' alt='123' src="https://github.com/dataviz2018/final-group3/blob/master/chart2.png">

We selected the demographic variables of income, education, and population, hoping to find connections between our subject and other measurements.Form the graph, we can find the interest correlation between the number of the complaints and the total population, the educational level, and the median income.

<img width='971' alt='123' src="https://github.com/dataviz2018/final-group3/blob/master/data01.png">

<img width='971' alt='123' src="https://github.com/dataviz2018/final-group3/blob/master/data02.png">

<img width='971' alt='123' src="https://github.com/dataviz2018/final-group3/blob/master/data03.png">

### Find and visualize characters of loud music complaint
#### Jiacheng ZHOU, jz2866
The map shows the census tracts that are affected by sound noise. People generally can perceive a noise level change that is three decibels (dB), the unit used to measure the intensity of a sound, or greater. 
According to Traffic Noise Basics Fact Sheet provided by KeepSanDiegoMoving project, 200 feet is the ‘effective’ noise spreading radius. Thus, we select 200ft as the buffer radius of the Broadway to find out what census tracts are contained in the affected area. Then, I select all the Loud of Music points located in those census tracts and the neighborhoods that contain these census tracts. After that, I downloaded NTA(Neighborhood Tabulation Area) data and spatial join the point data to the selected(affected) neighborhoods  to find out how many points are located in each affected neighborhood. 
<img width='971' alt='123' src="https://github.com/dataviz2018/final-group3/blob/master/123.jpg">

### Sketching ideas before final visualization 
#### Kate Wang (kw2673)

For the sketch, we draft our ideas using AI and PS so that any changes could be easily made before finalization into codings. The coding part is the hard core of the project, which is accomplished through using Atom and Git Bash. Both of them provide us the possibility to collaborate and to work as a team on our project as well as to look through and correct the coding job of everyone. Below is the graph that was drafted when we come up with a claer idea of incorporating three indicators, numbers of complaints in different neighborhoods, and seasonal changes into a same graph. 

<img width='971' alt='123' src="https://github.com/dataviz2018/final-group3/blob/master/Scrn-3.png">

### DESIGN AND IMPLEMENTATION
#### Oskar Garcia, og2236

#### – The Site

As someone who has been programming for less than 7 months, I considered that the final project was the best way to gain practice over HTML5 and CSS3, which we touched upon briefly during the beginning of the course before we shifted into P5.js as our main technology. This meant having to learn about the CSS grid layout and its integration with JavaScript (JS) and HTML, as opposed to relying on solutions like pre-made wordpress templates, or Bootstrap. Thus the final layout for our site, though humble because of the time constraints, was custom designed and custom coded for the course.

The fonts were paired from Google Fonts, and the color palette was kept simple for brevity and ease of use. Our header was produced with an open sourced image from <unsplash.com>, and a bit of manipulation with Photoshop.

#### – The Visualizations

Though we focused mostly on using P5.js as a jumping off framework for learning JS, we had few opportunities for building a fully functional interactive chart from scratch, and our project needed something more robust to achieve the type of visualizations we wanted to implement.

Thus, after researching specialized JS frameworks and libraries, I decided to learn how to use an open source library called <chartjs.org>. The library holds many features that allow for many degrees of creative freedom when producing interactive charts, but unfortunately, the learning curve is still very steep.

However, the library allowed for us to visually express the data in the way we had prototyped. For example, for the graph below we had envisioned a stack of line graphs over a series of circles whose area represents the total quantity of complaints per neighborhood. The intent is for the users to be able to explore the complaints alongside the demographic variables per neighborhood, and gain some insight or correlation from their values. Though not loaded with interactive bells and whistles, our graphs translated our sketches and protoypes into real, working designs with a clean aesthetic.

Graph 1


<img width="917" alt="scrn-1" src="https://user-images.githubusercontent.com/38872082/39655504-f6265906-4fc7-11e8-8e89-ceee1b6708bc.png">


For our second graph we wanted to show the correlation of loud music complaints across the four seasons for every neighborhood, which we represented again as the area of a circle with different colors for every season.


Graph 2


<img width="971" alt="scrn-3" src="https://user-images.githubusercontent.com/38872082/39655951-b05ec73e-4fca-11e8-8efc-c9c029407798.png">

### Editing 
#### Qianyu Xiang, qx2170 & Jialin Zhai, jz2893
The final documentation editing is about the explanation and reflection of the whole project. We reviewed the whole process of our design, data exploring as well as coding, finding the advantages and disadvantages of our projects as well as the flaws to be improved in the future.
