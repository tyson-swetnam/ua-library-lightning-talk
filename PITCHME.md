---

<span style="font: fsmall-caps bold 24px/1 sans-serif; font-size: 150%">Leveraging CyVerse for GIS on HPC and Cloud</span>

###### November 15, 2017
###### Tyson Lee Swetnam
###### Science Informatician

---

### Contact

[http://www.cyverse.org/](http://www.cyverse.org/)

email: tswetnam@cyverse.org

github: tyson-swetnam

twitter: tswetnam

---

### Research at scale beyond the laptop or local desktop solution

---

<img src="https://developers.google.com/earth-engine/images/Playground.png" height="250">
<img src="assets/imagery/planet.png" height="250">
<img src="https://pbs.twimg.com/media/DN5ZyIbVwAA7BLB.png" height="250">
<img src="https://pbs.twimg.com/media/C6U9LTQVAAE_j0b.png" height="250">


---

Okay, well now what?

---

<span style="font: fsmall-caps bold 24px/1 sans-serif; font-size: 150%">Use CyVerse to build your own GIS Data Scientist workbench!</span>

---

### A data science workbench allows: 

- Work in preferred environment, language, and libraries 
- Select tools you want to use
- Write in a computational notebooks  
  - Python, R, C++, Matlab, Spark, etc. 

---

## Data Science Software

---

<img src="https://www.vectorlogo.zone/logos/docker/docker-official.svg" height="350">

---

<img src="http://singularity.lbl.gov/images/logo/logo.svg" height="350">

---

<img src="https://www.python.org/static/community_logos/python-logo-inkscape.svg" height="150"> <img src="http://jupyter.org/assets/hublogo.svg" height="150">

<img src="https://mybinder.org/static/logo.svg" height="150"><img src="https://upload.wikimedia.org/wikipedia/en/thumb/6/6e/Esri_logo.svg/1280px-Esri_logo.svg.png" height="150">

---

<span style="padding-right:3px; padding-top: 3px; display:inline-block;">
<img src="http://amsantac.co/images/2016-06-29-reproducibility-arcpy-jupyter-notebook-r-fig-8.jpg"></img>
</span>

---

<span style="padding-right:3px; padding-top: 3px; display:inline-block;">
<img src="http://esri.github.io/arcgis-python-api/notebooks/nbimages/landing_arcgis_python_api_in_5_mins_thumbnail.png">
</img>
</span>

---

<img src="https://boundlessgeo.com/wp-content/themes/boundlessgeo/assets/images/BoundlessLogoTag.svg" height="250">

---

<img src="https://qgisblog.files.wordpress.com/2016/12/qgis-logo_anita02.png" height="200">

---

<span style="padding-right:3px; padding-top: 3px; display:inline-block;">
<img src="https://underdark.files.wordpress.com/2016/01/screenshot-2016-01-06-17-11-27.png"></img>
</span>

---

<img src="https://grass.osgeo.org/uploads/images/logo_variant_nobg.png" height="200">

---

<span style="padding-right:3px; padding-top: 3px; display:inline-block;">
<img src="https://grass.osgeo.org/uploads/images/grass_gis721.png"></img>
</span>

---

<img src="https://www.r-project.org/logo/Rlogo.svg" height="150"> <img src="https://www.rstudio.com/wp-content/uploads/2014/07/RStudio-Logo-Blue-Gradient.png" height="150">

---

## CyVerse [Atmosphere](https://cyverse.org/atmosphere)
## NSF [Jetstream](https://use.jetstream-cloud.org)
<img src="http://www.cyverse.org/sites/default/files/Jetstream_logo_hi_res_cropped.jpg" height="150"> 

+++

- Linux (Centos, Ubuntu)
- 1 CPU  to 16 CPU 
- 4 GB to 128GB RAM 
- Attach (swap) TB size storage volumes    
- emulated web shell and desktop 

---

@title[EZ Install]


## <span style="color: #e49436">EZ Install</span>
[http://learning.cyverse.org/](http://learning.cyverse.org/)
<br>

```shell
$ ez
$ ezd
$ ezs
$ ezj -R -3
```

@[1](View option menu for `ez`)
@[2](Install latest version of Docker)
@[3](Install latest version of Singularity)
@[4](Install Anaconda and Jupyter Notebooks w/ Python3 and the R Kernel)

---

@title[Docker RStudio]

## <span style="color: #e49436">Docker + RStudio</span>
<br>

```shell
$ ezd
$ sudo usermod -aG docker $USER
$ exit
$ docker pull rocker/geospatial
$ docker run -d -p 8787:8787 rocker/geospatial

Done!

```

@[1](install Docker)
@[2](change `sudo` privileges)
@[3](exit and restart terminal window)
@[4](pull the Rocker/Geospatial Rstudio-Server from DockerHub)
@[5](Run the Container in detached mode `-d` on port `-p 8787:8787`)
@[7](Open the Instance's IP address w/ port number in a new browser window)

---

@title[QGIS-GRASS-RStudio native build]

## <span style="color: #e49436">QGIS + GRASS + RStudio</span>
<br>

```shell
$ git clone https://github.com/cyverse-gis/focus-forum.git
$ cd focus-forum/atmo
$ . install_qgis.sh
$ . build_grass.sh
$ . install_rstudio.sh

```

@[1](Clone a public Github Repo)
@[2](Change into the directory with the installation scripts)
@[3](Install QGIS)
@[4](Build GRASS 7.2 from source)
@[5](Install RStudio)
@[6](Open the Instance's IP address w/ port number in a new browser window)
@[7](Launch Web Desktop with Apache Guacamole)

---

<img src="assets/imagery/cyverse.png" height="100%">

---


