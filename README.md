<p align="center">
<a href="https://github.com/ericktokuda/">
<img src="https://github.com/ericktokuda/ericktokuda/blob/main/img/banner_github2.png">
</a>
</p>

## Eric K. Tokuda
Skills: Algorithms / Linux / Python / C

- I’m currently working on the characterization of cities through street networks. 
- I’m currently learning algorithm optimization and Pytorch. 
- I’m looking to collaborate on computer vision and network science projects. 
- I’m am passionate about the Japanese and the Chinese languages (while I don't know much). 
- How to reach me: [LinkedIn](https://www.linkedin.com/in/tokudaek/ "LinkedIn")  

Here are some of my projects:

---

### Diffusion of the constructed areas (2021)

<a href="https://github.com/tokudaek/citydiffusion">
<img src="https://github.com/ericktokuda/ericktokuda/raw/main/img/greendiff_animation.gif" title="Diffusion of the green regions" width="640">
</a>

This work is motivated by the expansion of the constructions over the green regions in a city. I identify the identify the constructed areas (non-green) using satellite images and simulate the isotropic diffusion of these regions. The constructed regions are identified using a DL-based semantic segmentation method. The output is a binary mask with the same of the input image. Starting from the binary mask, I evaluate successive convolutions with a mean kernel and at each step I restore the original constructed regions to the maximum value, 1. This modification of the regular diffusion is motivated by the scenario where the constructions are not destroyed but just expanded. The same procedure is performed on six brazilian cities and the impact of the destruction of green areas can be studied. The opposite can also be studied, i.e., the expansion of the green regions over the constructed areas. This work has been carried out in collaboration with my colleagues from USP and UFSCAR. If you want more details, please refer to [here](https://arxiv.org/abs/2103.11998).

---

### Epidemy contagion simulation (2020)

<a href="https://github.com/tokudaek/epidspread/">
<img src="https://github.com/ericktokuda/ericktokuda/raw/main/img/epidmodel_animation.gif" title="Simulation of the contagion process" width="640">
</a>

The mathematical modelling of infectious diseases is an important piece in the epidemiology field. It allows one to study in principle an infinite number of epidemic scenarios in a safe way for the population. The Scottish researchers A. G. McKendrick and W. O. Kermack published in the 30's the foundation stone of the compartimental models research. They proposed a set of differential equations that allowed one to mathematically define the transmission stage, by determining the number of Succeptibles, Infected and Recovered. That gave risen to the famous SIR model, which is widely studied and extended in the current days. In this ABM, agents are allowed to move among vertices, but just agents in the same vertices may transmit or be infected. Additionaly, assume that these vertices are placed over a vector field with local minima and maxima of *attraction*. Agents move stochastically according to the vector field. How would the dynamics of the disease would change in such a scenario? That is que question that drives this research. This work has been done in collaboration with my colleagues from USP, in particular PCV Silva. Code is mostly in Python, with critical parts ported to C (Cython).

---

### Hierachical agglomerative clustering (2020)

<a href="https://github.com/tokudaek/hieclust/">
<img src="https://github.com/ericktokuda/ericktokuda/raw/main/img/hieclust_teaser_vio.jpg" title="Multiple distributions" width="640">
</a>

Hierarchical clustering differ from regular clustering by providing the a hierarchy (order) in which the clusters are formed. It allows for instance that that the cut of groups be defined a posteriori.  In this project, I analyze classical hierarchical clustering algorithms, namely single, average, median, complete, centroid, and Ward's, with respect to the Type II error (false positives) in the problem of trying to separate unimodal and bimodal distributions. I created a synthetic dataset for this task, with points following uniform, gaussian, exponential and power-law distributions in 2d, 3d, ... , 10d.  The results showed that the single-linkage, often seen as a method leading to unreliable results due to the chaining effect, lead to one of the best results considering the error typeII. I thank my collaborators from USP and from UFSCAR for the joint work.

---

### Tagging detection (2019)

<a href="https://github.com/tokudaek/graffutils/">
<img src="https://github.com/ericktokuda/ericktokuda/raw/main/img/graffiti_teaser_ind.jpg" title="Tagging detection" width="640">
</a>

Tagging is present in most big cities and there is no knowledge about where they are primarily concentrated. Manually inspecting the regions with graffiti may be expensive. In this project I estimate the tagging distribution in a region using public images. Important to notice in this work we are not focused on paintings on the walls. For this task I used the Google Street View REST api to acquire the visual data. I concentrated in a city which is known for having lots of occurences of tagging - Sao Paulo, Brazil. I sampled the city region in a grid with four view orientations, which resulted in ~275,000 images. The results was used to create a map of tagging occurences in the analyzed city. I we recall the Broken Window theory, the tagging distribution can be used as an indicator of other features of the city. I matched the results with a socioeconomical indicator, the HDI and resulted in a resonably well correlation. This work has been produced in collaboration with my colleagues from NYU and from USP. I also supervised, with RM Cesar-Jr, a graduate final work from FS Silva.

---

### Sensor networks (2019)

<a href="https://youtu.be/ngihdYfW5Ok">
<img src="https://github.com/ericktokuda/ericktokuda/raw/main/img/sensornet_youtube.jpg" title="Sensor networks" width="640">
</a>

One can say that we live in the sensor era. That is because we are surrounded all kinds of sensors, measuring a great variety of signals and generating even more types of data. When these sensors are somehow organized as a group, they are a called a sensor network. A special type of these systems consists in mobile units, the sensors, that are periodically sense the environment.  The idea of using mobile sensors may be promissing, but isn't it dependent on the sensor accuracy? That is what we have studied in this project. In this work, we simulated mobile sensors moving in a closed region and sensins the nearby elements. However, the measurements carry erros, both systematic and random ones.  We deployed a set of sensors that were able to count with potential error the pedestrians nearby. We compared it with the real count, given by the number of pedestrians deployed. This work has been produced in collaboration with my colleagues from Bloomberg, NYU, from Carmera and from USP.


---

### Pedestrian detection (2019)

<a href="https://github.com/VIDA-NYU/carmera-modelling">
<img src="https://github.com/ericktokuda/ericktokuda/raw/main/img/peddens_heatmap420.png" title="Pedestrian detection" width="250">
</a>

The distribution of pedestrians in the city is a valuable information for different activities, such as for business, urban planning and disasters control. For instance, one may want to understand why a few streets have very low densities of people comparing to the neighbour streets or, conversely, why apparently common strets have a peak on the flow of people in specific hours.  The initial approaches consisted in manually counting the people passing through a given region. Despite accurate, it is a laborious task and unfeasiable in a large city-scale. With the increasing availability of images coming from static monitoring cameras, and with the advances in computer vision, this task can be done automatically. Monitoring cameras, however are limited to the locations they are installed. Considering the above limitations, [Carmera](https://www.carmera.com) provides images wigh spatial and temporal variation. Their fleets continuously travels across the city acquiring images. In a collaboration with this company, I had access to the more than 40M images captured across a year in the New York city. Such a large amount of data demanded smart procedures in terms of store, search, and processing. For instance, slight modifications in a SQL query resulted in dozens of hours of difference in processing. Another fundamental task concerns the counting of people. Fortunately, one of the more evident areas in machine learning is computer vision. We tested some of the available approaches and used a convnet with a residual network backbone. This work has been produced in collaboration with my colleagues from Bloomberg, from NYU, from [Carmera](https://www.carmera.com/about/) and from the USP.

---

### De-raining (2018)

<a href="https://github.com/lsy17096535/Single-Image-Deraining">
<img src="https://github.com/ericktokuda/ericktokuda/raw/main/img/derain_gmm_idcgan_gray.jpg" title="De-raining" width="640">
</a>

Weather affects our visual system and as such, it also impacts the imaging sensors. This has a strong implications for the vision systems of autonomous vehicles, for instance. For this reason, the degradation imposed by the weather are heavily studied by the computer vision/graphics community. In this project, we study how the rain affects the object detection task. We consider two scenarios: (a) images with synthetically generated rain and (b) real rain. The advantage of the former is that we can treat the problem as an image restoration task, with a ground-truth. Conversely, the latter exhibit the real changes caused by the rain, and not a simple model of it. We tested different deraining methods and subsequently applied state-of-the-art object detection approaches. The results were counter-intuitive, despite deraining methods may improve the visual appearance of the images, it does not consistently improve the posterior object detection task.  This work has been done in collaboration with my colleagues from U. Austin, from the Chinese Academy of Sciences and from USP.

---

### Cloud services (2017)

<a href="https://devpost.com/software/byteover2/">
<img src="https://github.com/ericktokuda/ericktokuda/raw/main/img/cloudserv_teaser_red.jpg" title="Cloud services" width="640">
</a>

There is a large variety of cloud services today, spanning the IaaS, PaaS, and SaaS. In this hackaton, we were asked to use cloud services to build a _useful_ web application. Our team was composed of three members: me, Chuck, and Stevens.

In this one day and a half hackaton, we built an application that automatically analyzed your message (in voice or in text) and replyied according to the _sentiment_ of the message left.  The application used Twilio as a communication API; MS Azure cognitive services, to identify the mood of the SMS or the audio message; and a flask web server. The programming language of choice was python.

Our project, called BYTEOVER2 won the Twilio hack at the  [Global AI NYC 2017](https://devpost.com/software/byteover2/). In it, [Twilio](https://www.twilio.com/docs/sms/quickstart/python#set-up-a-twilio-messaging-service) is used as a front end interface to users, capturing both SMS and voice communication which is passed to a Flask backend running on Amazon EC2. The backend server is responsible for querying Microsoft Azure for speech to text and sentiment analysis, and implements logic for selecting the appropriate text response or mixing the appropriate music with the user's recorded voice according to their emotional valence. Twilio is again used to serve the [text](https://www.twilio.com/docs/sms/quickstart/python#set-up-a-twilio-messaging-service) / [audio](https://azure.microsoft.com/en-us/services/cognitive-services/speech-services/) back to the user. All operation occur synchronously.

---

### Surveillance cameras (2016)

<a href="https://ieeexplore.ieee.org/abstract/document/8470307/">
<img src="https://github.com/ericktokuda/ericktokuda/raw/main/img/survcam_animation.gif" title="Surveillance camera in Brazil" width="640">
</a>

<!--<img src="https://github.com/ericktokuda/ericktokuda/raw/main/img/survcam_grid.png" title="Surveillance cameras in Brazil" width="640">-->
If before the surveillance cameras were used primarily for traffic rules enforcement, nowadays they are part of the urban environment. It is fastly changing, but a decade ago the images generated by surveillance cameras were static, of low quality, of low sampling rate. Manually inspecting the data generated by these cameras is almost unfeasible and automatic methods are generally employed to help in this task. These methods, though, may be impacted by the varying illumination, weather, and noise. In this project, we improved the detection model with a self-supervised learning approach. The model feeds itself with new training samples to generate a more robust comptuer vision method. Our vision task was the object detection of cars. With this approach, we generated a method with much higher recall with the expense of a small loss of precision. This work was produced in collaboration with my colleagues from NYU and from USP.

---

### Image forensics (2013)
<a href="https://github.com/tokudaek/cgvspg">
<img src="https://github.com/ericktokuda/ericktokuda/raw/main/img/forensics_cameras.png" title="Which one is real?" width="640">
</a>

Digital forensics is a branch of the Forensics Science that encompasses the use of digital data in court. For instance, the [Ashcroft v. Free Speech Coalition, 2002](https://www.law.cornell.edu/supct/html/00-795.ZO.html) considered that despite child pornography  in the format of media (pictures, videos) was prohibited, manually generated, including computer generated images were allowed. The consequence of that law was that if a child pornography image was proven to be generated by computer, the defendant was considered not guilty. Now suppose you are analyzing a case and you need to differentiate between a picture and a computer generated image. The task could be easy a while ago, but not today.  If you want to test your expertise, take a look at [Fake or Foto](https://area.autodesk.com/fakeorfoto/play/). This was the driving challenge in this project. In my Masters, back in 2013, I studied the problem of differentiating between these two categories of images by using machine learning. I searched the computational methods that did such things, implemented many of them and compared them. For instance, we implement the [method](https://ieeexplore.ieee.org/abstract/document/1381784/) proposed by Lyu and Farid, which explored the pyramidal wavelet decomposition and order statistics of the coefficients.   also proposed my own method, based on ensemble of classifiers. Take a look at a summary of the analysis below, including all analyzed methods.  I learned multiple things along the way, such as related to algorithms, Expectation Maximization ([EM](https://en.wikipedia.org/wiki/Expectation%E2%80%93maximization_algorithm)), pattern recognition, classifier performance analysis and ensemble of classifiers. Also, I used multiple tools in this projects, including Matlab, Perl, and R. This project was developed in collaboration with my colleagues from Unicamp [1](https://ic.unicamp.br/docente/helio-pedrini/) and [2](https://www.ic.unicamp.br/~rocha/).

---

### Graphical interface (2012)

<a href="https://code.google.com/archive/p/gebr/source/default/commits?page=5">
<img src="https://github.com/ericktokuda/ericktokuda/raw/main/img/gui_gebr1.jpg" title="Interface created (GêBR)." width="640">
</a>

Have you ever heard about *seismic imaging*?  It represents one the main objects of study by the geophysicists. It is seismic image, a consequence of the reflection and refraction of seismic waves by the Earth underground layers. It has many applications, including the study of earthquakes, and exploration of oil and gases.  The goal of this project was to create an interface to facilitate the cumbersome organization of parameters in the execution of seismic processing commands as a free software. There are tools that handles geophysical data in an excelent way, however, the cost may be prohibitive for academy research centres. That was the motivation to create such a tool that is free of charge and more than that, open source. I was lucky to be part of the (brilliant) team that developed GêBR. The project was headed by [Ricardo Biloti](https://www.linkedin.com/in/ricardo-biloti-07329577/) and partly funded by [Petrobras](https://en.wikipedia.org/wiki/Petrobras). Below is a screenshot of the final product. I joined the team in 2011 and learned several concepts related to User Interface (UI), User Experience (UX), as well as the signal-callback paradigm. I also had to learn about the agile development and the iterative delivery of products. I programmed mostly in C, with the use of the GLib and Gtk+ libraries, but also had to use scripting languages (bash) for file handling. Also, I helped in the packaging for Linux distributions and I was also responsible for the update of the product documentation, given my interest for writing.


---

### Clustering (2009)

<a href="https://code.google.com/archive/p/gebr/source/default/commits?page=5">
<img src="https://github.com/ericktokuda/ericktokuda/raw/main/img/coffee_clustering_yellow.jpg" title="Coffee species clustering" width="640">
</a>

Coffee is included in the routine of millions of people worldwide. Understanding the factors associated to its cup taste and resistance to pests has economical value and is studied by different research centres. We study the gene expression of the two most common species of coffee, namely _Coffea arabica_ and _Coffea canephora_. We utilize the transcriptomic data generated by the Nestle-Cornell and the Brazilian Coffe Genome Project and a wide range of bioinformatics tools in this analysis. The results identify genes that are specific or prevalent of each specie which help to explain characteristics of each of the two crops. For instance, this analysis brought an understanding with genomic foundations of the better cup taste of the _C. arabica_ and the high tolerance to stress of the _C. canephora_.  If you want further details, please refer to the [article](https://www.ncbi.nlm.nih.gov/pubmed/21303543 "An EST-based analysis identifies new genes and reveals distinctive gene expression features of Coffea arabica and Coffea canephora"). This work has been  conducted in collaboration with my friends from the [Laboratory of Genomics and Expression](http://143.106.232.3/) at UNICAMP.

---

### Game development (2007)

<a href="https://github.com/tokudaek/spaceinvaders">
<img src="https://github.com/ericktokuda/ericktokuda/raw/main/img/game_animation.gif" title="Pseudo-space-invaders" width="397">
</a>

Space Invaders is a 70's game developed by Taito, in Japan, for Arcade and for Atari. You are the commander of spaceship responsible to protect your planet by destroyoing the invading alliens. In my programming 101 course, back in *2008*, me and a colleague, Pedro de Andrade, developed our version inspired in this classical game. We had no notion of game programming and most of the excelent tools for game development did not exist at the time, so we had to learn lots of concepts in the process, such as physics, (basic) AI and design. For instance, one the main functions regards the calculation of the intersection between pairs of objects. It was used to calculate the collisions among our ship, the enemies, the shields, and the shots. The code is far from following all the good rules of programming, given that we were just in our first year and that we developed it in 4 days in a row. The code is composed of almost 1,000 lines in a single file, with no OO and with many global variables. The code is entirely writen in C, with the OpenGL and the GLut libraries. The result can be seen above. I know, it is not quite the same as the original, but we can definitely have some fun with it.

---
Eric K. Tokuda

