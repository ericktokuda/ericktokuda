![I am a machine learning/data science enthusiastic](https://github.com/ericktokuda/ericktokuda/blob/main/img/banner_github2.png)

#### I am a machine learning/data science enthusiastic actively looking for new challenges

Skills: Algorithms / Linux / Python / C

- I’m currently working on the characterization of cities through street networks. 
- I’m currently learning algorithm optimization and Pytorch. 
- I’m looking to collaborate on computer vision and network science projects. 
- I’m looking for help with the Chinese language. 
- How to reach me: [LinkedIn](https://www.linkedin.com/in/https://www.linkedin.com/in/tokudaek/ "LinkedIn")  

---
#### Some of my projects:

---

<p align="center">
<img src="https://github.com/ericktokuda/ericktokuda/raw/main/img/greendiff_animation.gif" alt="Diffusion of the green regions" width="500">
</p>

[2021] This work is motivated by the expansion of the constructions over the green regions in a city. I identify the identify the constructed areas (non-green) using satellite images and simulate the isotropic diffusion of these regions. The constructed regions are identified using a DL-based semantic segmentation method. The output is a binary mask with the same of the input image. Starting from the binary mask, I evaluate successive convolutions with a mean kernel and at each step I restore the original constructed regions to the maximum value, 1. This modification of the regular diffusion is motivated by the scenario where the constructions are not destroyed but just expanded. The same procedure is performed on six brazilian cities and the impact of the destruction of green areas can be studied. The opposite can also be studied, i.e., the expansion of the green regions over the constructed areas.

This work has been carried out in collaboration with my colleagues FASS, HFA, GSD, CHC, LFC, RMCJ. You can check more details [here](https://arxiv.org/abs/2103.11998) and the source code [here](https://github.com/tokudaek/citydiffusion).

---

[2020] The mathematical modelling of infectious diseases is an important piece in the epidemiology field. It allows one to study in principle an infinite number of epidemic scenarios in a safe way for the population. The Scottish researchers A. G. McKendrick and W. O. Kermack published in the 30's the foundation stone of the compartimental models research. They proposed a set of differential equations that allowed one to mathematically define the transmission stage, by determining the number of Succeptibles, Infected and Recovered. That gave risen to the famous SIR model, which is widely studied and extended in the current days.

![Missing image](https://github.com/ericktokuda/ericktokuda/raw/main/img/epidmodel_animation.gif)

Different from the homogeneous distibution of individuals, *metapopulation models* assume the existence of conglomerates of individuals, the populations, such that the transmission process occurr just inside the populations, i.e., among individuals in the same population and inviduals are allowed to move from one population to the other.

This scenario can be modeled by a graph using an ABM model, with populations represented by vertices and agents that *are* in a particular vertex at a particular time. Agents are allowed to move among vertices, but just agents at the same vertex may transmit or be infected. Additionaly, assume that these vertices are placed over a vector field with local minima and maxima of *attraction*. Agents move stochastically according to the vector field. How would the dynamics of the disease would change in such a scenario? That is que question that drives this research.

The bulk of the code in Python. Given the large number of repetitions required by this kind of project, key parts of the code have been ported to C (Cython). The source code is available [here](https://github.com/tokudaek/epidspread).

This work has been done in collaboration with my colleagues from USP, FA Rodrigues, LF Costa and PCV Silva.

---
2020

{{< figure src="/images/hieclust_bimodal.png" alt="Missing image." position="center" style="border-radius: 8px;" caption="Clusterization based on density.">}}


Hierarchical clustering differ from regular clustering by providing the a hierarchy (order) in which the clusters are formed. It allows for instance that that the cut of groups be defined a posteriori.


In this project, I analyze classical hierarchical clustering algorithms, namely single, average, median, complete, centroid, and Ward's, with respect to the Type II error (false positives) in the problem of trying to separate unimodal and bimodal distributions. I created a synthetic dataset for this task, with points following uniform, gaussian, exponential and power-law distributions in 2d, 3d, ... , 10d.

{{< figure src="/images/hieclust_dendrogram.png" alt="Missing image." position="center" style="border-radius: 8px;" caption="On the right, a hierarchical clustering of the points on the left.">}}

The results showed that the single-linkage, often seen as a method leading to unreliable results due to the chaining effect, lead to one of the best results considering the error typeII.

The source code is available [here](https://github.com/tokudaek/hieclust).

This work has been produced in collaboration with my colleagues from USP and from UFSCAR, namely LF Costa and CH Comin.

---
2019

{{< figure src="/images/graffiti_wall.jpg" alt="Missing image." position="center" style="border-radius: 4px;" caption="Tagging occurences in Brazil.">}}

Tagging is present in most big cities and there is no knowledge about where they are primarily concentrated. Manually inspecting the regions with graffiti may be expensive. In this project I estimate the tagging distribution in a region using public images. Important to notice in this work we are not focused on paintings on the walls.

For this task I used the Google Street View REST api to acquire the visual data. I concentrated in a city which is known for having lots of occurences of tagging - Sao Paulo, Brazil. I sampled the city region in a grid with four view orientations, which resulted in ~275,000 images.

I used the Mask-RCNN pretrained on Image NET and finetuned in our data to segment the images. I manually annotated ZZZ images.

{{< figure src="/images/graffiti_segmentation.png" alt="Missing image." position="center" style="border-radius: 4px;" caption="Tagging identification in sample images. Images from Google Maps.">}}

The results was used to create a map of tagging occurences in the analyzed city. I we recall the Broken Window theory, the tagging distribution can be used as an indicator of other features of the city. I matched the results with a socioeconomical indicator, the HDI and resulted in a resonably well correlation.

The source code is available [here](https://github.com/tokudaek/Mask_RCNN).


This work has been produced in collaboration with my colleagues from NYU and from USP, CT Silva and RM Cesar-Jr. I also supervised, with RM Cesar-Jr, an graduate final work from USP from FS Silva.

---
2019

One can say that we live in the sensor era. That is because we are surrounded all kinds of sensors, measuring a great variety of signals and generating even more types of data. When these sensors are somehow organized as a group, they are a called a sensor network. A special type of these systems consists in mobile units, the sensors, that are periodically sense the environment.

The idea of using mobile sensors may be promissing, but isn't it dependent on the sensor accuracy? That is what we have studied in this project. In this work, we simulated mobile sensors moving in a closed region and sensins the nearby elements. However, the measurements carry erros, both systematic and random ones.


We started using [LibPedSim](http://pedsim.silmaril.org/download/) in our implementation. It is a great framework for pedestrian simulation. See below an example of what I have implemented using the framework. We can imagine it was in a black friday!

{{< youtube xuy1AGblv4A >}}

After a while, considering our personalizations and the costs associated, we prefered to implement our own version of the simulation. We deployed a set of sensors that were able to count with potential error the pedestrians nearby. We compared it with the real count, given by the number of pedestrians deployed.

{{< figure src="/images/sensornet_simu.png" alt="Missing image." position="center" style="border-radius: 4px;" caption="Real and sensed count of pedestrians.">}}

This work has been produced in collaboration with my colleagues from NYU, from Carmera and from the University of Sao Paulo, namely, Y Lockerman, GBA Ferreira, E Sorrelgreen, D Boyle, RM Cesar-Jr and CT Silva.

---
2019

{{< figure src="/images/peddens_heatmap420.png" alt="Missing image." position="center" style="border-radius: 8px;" caption="Pedestrian heatmap across 2016.">}}

The distribution of pedestrians in the city is a valuable information for different activities, such as for business, urban planning and disasters control. For instance, one may want to understand why a few streets have very low densities of people comparing to the neighbour streets or, conversely, why apparently common strets have a peak on the flow of people in specific hours.

The initial approaches consisted in manually counting the people passing through a given region. Despite accurate, it is a laborious task and unfeasiable in a large city-scale. With the increasing availability of images coming from static monitoring cameras, and with the advances in computer vision, this task can be done automatically. Monitoring cameras, however are limited to the locations they are installed.

Considering the above limitations, [Carmera](https://www.carmera.com) provides images wigh spatial and temporal variation. Their fleets continuously travels across the city acquiring images. In a collaboration with this company, I had access to the more than 40M images captured across a year in the New York city. Such a large amount of data demanded smart procedures in terms of store, search, and processing. For instance, slight modifications in a SQL query resulted in dozens of hours of difference in processing.

Another fundamental task concerns the counting of people. Fortunately, one of the more evident areas in machine learning is computer vision. We tested some of the available approaches and used a convnet with a residual network backbone.


{{< youtube ngihdYfW5Ok >}}

This work has been produced in collaboration with my colleagues from NYU, from [Carmera](https://www.carmera.com/about/) and from the University of Sao Paulo: Y Lockerman, G Ferreira, E Sorrelgreen, D Boyle, R Cesar-Jr and C Silva.

---
2018

Weather affects our visual system and as such, it also impacts the imaging sensors. This has a strong implications for the vision systems of autonomous vehicles, for instance. For this reason, the degradation imposed by the weather are heavily studied by the computer vision/graphics community.

{{< figure src="/images/derain_synthetic.png" alt="Missing image." position="center" style="border-radius: 4px;" caption="Original image and synthetically added rain.">}}

In this project, we study how the rain affects the object detection task. We consider two scenarios: (a) images with synthetically generated rain and (b) real rain. The advantage of the former is that we can treat the problem as an image restoration task, with a ground-truth. Conversely, the latter exhibit the real changes caused by the rain, and not a simple model of it.

{{< figure src="/images/derain_gmm_idcgan.png" alt="Missing image." position="center" style="border-radius: 4px;" caption="Input image and removal of rain by GMM and IDCGAN.">}}

We tested different deraining methods and subsequently applied state-of-the-art object detection approaches. The results were counter-intuitive, despite deraining methods may improve the visual appearance of the images, it does not consistently improve the posterior object detection task.

The source code is available [here](https://github.com/lsy17096535/Single-Image-Deraining).

This work has been done in collaboration with my colleagues from Texas A\&M, the Chinese Academy of Sciences and from USP, S Li, IB Araujo, W Ren, Z Wang, R Hirata-Jr, R Cesar-Jr, J Zhang, X Guo, and X Cao.

---
2017

{{< figure src="/images/cloudserv_hackaton.jpg" alt="Missing image." position="center" style="border-radius: 8px;" caption="Global AI hackaton.">}}

There is a large variety of cloud services today, spanning the IaaS, PaaS, and SaaS. In this hackaton, we were asked to use cloud services to build a _useful_ web application. Our team was composed of three members: me, Chuck, and Stevens.

In this one day and a half hackaton, we built an application that automatically analyzed your message (in voice or in text) and replyied according to the _sentiment_ of the message left.  The application used Twilio as a communication API; MS Azure cognitive services, to identify the mood of the SMS or the audio message; and a flask web server. The programming language of choice was python.

Our project, called BYTEOVER2 won the Twilio hack at the  [Global AI NYC 2017](https://devpost.com/software/byteover2/). In it, [Twilio](https://www.twilio.com/docs/sms/quickstart/python#set-up-a-twilio-messaging-service) is used as a front end interface to users, capturing both SMS and voice communication which is passed to a Flask backend running on Amazon EC2. The backend server is responsible for querying Microsoft Azure for speech to text and sentiment analysis, and implements logic for selecting the appropriate text response or mixing the appropriate music with the user's recorded voice according to their emotional valence. Twilio is again used to serve the [text](https://www.twilio.com/docs/sms/quickstart/python#set-up-a-twilio-messaging-service) / [audio](https://azure.microsoft.com/en-us/services/cognitive-services/speech-services/) back to the user. All operation occur synchronously.

The source code is available [here](https://github.com/chuckyee/byteover2).

{{< figure src="/images/cloudserv_byteover2.jpg" alt="Missing image." position="center" style="border-radius: 8px;" caption="Our winner project, byteover2.">}}

---
2017


If before the surveillance cameras were used primarily for traffic rules enforcement, nowadays they are part of the urban environment. It is fastly changing, but a decade ago the images generated by surveillance cameras were static, of low quality, of low sampling rate.

{{< figure src="/images/survcam_grid.png" alt="Missing image." position="center" style="border-radius: 8px;" caption="Surveillance cameras in Brazil.">}}

Manually inspecting the data generated by these cameras is almost unfeasible and automatic methods are generally employed to help in this task. These methods, though, may be impacted by the varying illumination, weather, and noise.

In this project, we improved the detection model with a self-supervised learning approach. The model feeds itself with new training samples to generate a more robust comptuer vision method. Our vision task was the object detection of cars. With this approach, we generated a method with much higher recall with the expense of a small loss of precision.

{{< figure src="/images/survcam_animation.gif" alt="Missing image." position="center" style="border-radius: 8px;" caption="Surveillance cameras are generally static and of low quality.">}}

This work was produced in collaboration with my colleagues from NYU and from USP, [C Silva](https://engineering.nyu.edu/faculty/claudio-silva), [RM Cesar-Jr.](https://bv.fapesp.br/en/pesquisador/397/roberto-marcondes-cesar-junior/) and G Ferreira.

---
2012

Have you ever seen images such as below? 

{{< figure src="/images/gui_seismic.jpg" alt="Missing image." position="center" style="border-radius: 8px;" caption="Seismic imaging">}}

It represents one the main objects of study by the geophysicists. It is seismic image, a consequence of the reflection and refraction of seismic waves by the Earth underground layers. It has many applications, including the study of earthquakes, and exploration of oil and gases.

The goal of this project was to create an interface to facilitate the cumbersome organization of parameters in the execution of seismic processing commands as a free software. There are tools that handles geophysical data in an excelent way, however, the cost may be prohibitive for academy research centres. That was the motivation to create such a tool that is free of charge and more than that, open source. I was lucky to be part of the (brilliant) team that developed GêBR. The project was headed by [Ricardo Biloti](https://www.linkedin.com/in/ricardo-biloti-07329577/) and partly funded by [Petrobras](https://en.wikipedia.org/wiki/Petrobras). Below is a screenshot of the final product.

{{< figure src="/images/gui_gebr1.jpg" alt="Missing image." position="center" style="border-radius: 8px;" caption="Interface created (GêBR).">}}

I joined the team in 2011 and learned several concepts related to User Interface (UI), User Experience (UX), as well as the signal-callback paradigm. I also had to learn about the agile development and the iterative delivery of products. I programmed mostly in C, with the use of the GLib and Gtk+ libraries, but also had to use scripting languages (bash) for file handling. Also, I helped in the packaging for Linux distributions and I was also responsible for the update of the product documentation, given my interest for writing.

The source code is not maintained anymore but a copy is archived at [Google Code](https://code.google.com/archive/p/gebr/source/default/commits?page=5).

---
2012

Digital forensics is a branch of the Forensics Science that encompasses the use of digital data in court. For instance, the [Ashcroft v. Free Speech Coalition, 2002](https://www.law.cornell.edu/supct/html/00-795.ZO.html) considered that despite child pornography  in the format of media (pictures, videos) was prohibited, manually generated, including computer generated images were allowed. The consequence of that law was that if a child pornography image was proven to be generated by computer, the defendant was considered not guilty.

Now suppose you are analyzing a case and you need to differentiate between a picture and a computer generated image. The task could be easy a while ago, but not today. For instance, try to identify which of these image is generated by computer.

{{< figure src="/images/forensics_cameras.png" alt="Missing image." position="center" style="border-radius: 8px;" caption="A picture on the left and a computer generated image on the right.">}}


Not easy, huh? If you want to test your expertise, take a look at [Fake or Foto](https://area.autodesk.com/fakeorfoto/play/). This was the driving challenge in this project. In my Masters, back in 2013, I studied the problem of differentiating between these two categories of images by using machine learning. I searched the computational methods that did such things, implemented many of them and compared them. For instance, we implement the [method](https://ieeexplore.ieee.org/abstract/document/1381784/) proposed by Lyu and Farid, which explored the pyramidal wavelet decomposition and order statistics of the coefficients.

{{< figure src="/images/forensics_grid.png" alt="Missing image." position="center" style="border-radius: 8px;" caption="Computer generated images and pictures in the 1st and 2nd rows respectively.">}}

I also proposed my own method, based on ensemble of classifiers. Take a look at a summary of the analysis below, including all analyzed methods.

{{< figure src="/images/forensics_roc.png" alt="Missing image." position="center" style="border-radius: 8px;" caption="ROC curve of all methods.">}}

I learned multiple things along the way, such as related to algorithms, Expectation Maximization ([EM](https://en.wikipedia.org/wiki/Expectation%E2%80%93maximization_algorithm)), pattern recognition, classifier performance analysis and ensemble of classifiers. Also, I used multiple tools in this projects, including Matlab, Perl, and R. This project was developed in collaboration with my colleagues from [Unicamp](https://www.unicamp.br/unicamp/english), [H Pedrini](https://ic.unicamp.br/docente/helio-pedrini/) and [A Rocha](https://www.ic.unicamp.br/~rocha/). The source code is available [here](https://github.com/tokudaek/cgvspg).

---
2009

<!--{{< figure src="/images/coffee_workflow.png" alt="Missing image." position="center" style="border-radius: 8px;" caption="Workflow of the joint work.">}}-->

Coffee is included in the routine of millions of people worldwide. Understanding the factors associated to its cup taste and resistance to pests has economical value and is studied by different research centres.

We study the gene expression of the two most common species of coffee, namely _Coffea arabica_ and _Coffea canephora_. We utilize the transcriptomic data generated by the Nestle-Cornell and the Brazilian Coffe Genome Project and a wide range of bioinformatics tools in this analysis.


The results identify genes that are specific or prevalent of each specie which help to explain characteristics of each of the two crops. For instance, this analysis brought an understanding with genomic foundations of the better cup taste of the _C. arabica_ and the high tolerance to stress of the _C. canephora_.  If you want further details, please refer to the [article](https://www.ncbi.nlm.nih.gov/pubmed/21303543 "An EST-based analysis identifies new genes and reveals distinctive gene expression features of Coffea arabica and Coffea canephora").

{{< figure src="/images/coffee_clustering.png" alt="Missing image." position="center" style="border-radius: 8px;" caption="Hierarchical clustering of the C. canephora.">}}

This work has been  conducted in collaboration with J. Mondego, G. Pereira and my friends from the [Laboratory of Genomics and Expression](http://143.106.232.3/) at UNICAMP.

---
2006

Space Invaders is a 70's game developed by Taito, in Japan, for Arcade and for Atari. You are the commander of spaceship responsible to protect your planet by destroyoing the invading alliens.

{{< figure src="/images/game_si2.png" alt="Missing image." position="center" style="border-radius: 8px;" caption="Space invaders cartridge and screenshot.">}}

In my programming 101 course, back in *2008*, me and a colleague, Pedro de Andrade, developed our version inspired in this classical game. We had no notion of game programming and most of the excelent tools for game development did not exist at the time, so we had to learn lots of concepts in the process, such as physics, (basic) AI and design.

For instance, one the main functions regards the calculation of the intersection between pairs of objects. It was used to calculate the collisions among our ship, the enemies, the shields, and the shots.

The code is far from following all the good rules of programming, given that we were just in our first year and that we developed it in 4 days in a row. The code is composed of almost 1,000 lines in a single file, with no OO and with many global variables. The code is entirely writen in C, with the OpenGL and the GLut libraries.

{{< figure src="/images/game_animation.gif" alt="Missing image." position="center" style="border-radius: 8px;" caption="Gameplay of the game.">}}

The result can be seen above. I know, it is not quite the same as the original, but we can definitely have some fun with it. The source code is available [here](https://github.com/tokudaek/spaceinvaders).

