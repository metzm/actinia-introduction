# A gentle introduction to actinia

<center>
<img src="img/actinia_intro.png" width="60%">
</center>

Authors: Markus Neteler, Carmen Tawalika, Anika Weinmann, Guido Riembauer, Markus Metz, mundialis GmbH & Co. KG, Bonn

<!-- **** Begin Fork-Me-On-Gitlab-Ribbon-HTML. See MIT License at https://gitlab.com/seanwasere/fork-me-on-gitlab **** -->
<a href="https://github.com/metzm/actinia-introduction/">
    <span id="fork-me" style="font-family: tahoma; font-size: 18px; position:fixed; top:50px; right:-45px; display:block; -webkit-transform: rotate(45deg); -moz-transform: rotate(45deg); color:white; padding: 4px 30px 4px 30px; z-index:99; opacity:0.6">Fork Me On GitHub</span>
</a>
<!-- **** End Fork-Me-On-Gitlab-Ribbon-HTML **** -->


URL of this dcument: [https://metzm.github.io/actinia-introduction/](https://metzm.github.io/actinia-introduction/)

This workshop is a fork of [https://mmacata.github.io/actinia-introduction/](https://mmacata.github.io/actinia-introduction/). The initial workshop has more exercises. This workshop focuses on the "bare" HTTP API from actinia and jupyter notebooks to interact with actinia.

*Last update: 13 jun 2022*

## Abstract

<img src="img/actinia_logo.svg" width="30%" align="right">

Actinia ([https://actinia.mundialis.de/](https://actinia.mundialis.de/)) is an open source REST API for processing of geographical data in cloud computing systems that uses mainly GRASS GIS for computational tasks. Core functionality includes the processing of single scenes and time series of satellite images, of raster and vector data. With the existing big geodata pools growing day by day (e.g. Landsat and the Sentinel family), actinia is designed to follow the paradigm of bringing algorithms to the cloud stored geodata.

<!--
Nonsense: actinia is currently nowhere near the original cloud stored data. Instead, actinia requires the transfer of original cloud stored data to the cloud of the actual actinia instance.
-->

Actinia is an [OSGeo Community Project](https://www.osgeo.org/projects/actinia/) since 2019.

In this course we will give a short introduction to REST API and cloud processing concepts. This is followed by an introduction to actinia processing along with hands-on to get more familiar with the topic by means of exercises.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.2631917.svg)](https://doi.org/10.5281/zenodo.2631917)

## Required software for this tutorial

We will use an HTTP client to try out some REST commands. This can be a command line tool, code editor plugin or browser plugin.
This requires some software to be installed:

* REST client (one of the options below):
    * Command line tool: [cURL](https://curl.haxx.se/docs/manpage.html), to be used on command line
    * Extensions for Chrome/Chromium browser:
        * [RESTman extension](https://chrome.google.com/webstore/detail/restman/ihgpcfpkpmdcghlnaofdmjkoemnlijdi)
        * and a nice [JSON Formatter](https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa)
    * Extension for code editor, here for VS Code
        * [Thunderclient plugin](https://www.thunderclient.io/)
        * If you use a different editor, a similar plugin might exist

* Not required for this workshop but nice to have:
    * [jq](https://stedolan.github.io/jq/download/), a lightweight and flexible command-line JSON processor
    * <a href="https://www.qgis.org/en/site/forusers/download.html">QGIS</a>

The "ace - actinia command execution" section is a demonstration only. To dive deeper into this topic,
you can follow [these installation instructions](https://neteler.gitlab.io/actinia-introduction/#preparation_1).

Note: We will use the demo actinia server at [https://actinia.mundialis.de/](https://actinia.mundialis.de/) - hence Internet connection is required.

## actinia tutorial overview

**Content**

* Concepts of actinia, cloud computing, REST API
    * Why cloud computing?
    * Overview actinia
    * REST API and geoprocessing basics
* Explore
    * First Hand-on: working with REST API requests
    * Exploring the API: finding available actinia endpoints
* Client implementations
    * ACE - Controlling actinia from a running GRASS GIS session
    * actinia Connector - a QGIS plugin
    * actinia python client
* actinia with jupyter notebooks
    * Getting started with jupyter notebooks
    * actinia jupyter notebooks
* Conclusions and future
* About the trainers

<!--
## Warming up

(duration: 20 min)

To make you familiar with a few concepts, let's take a look at the "graphical intro to actinia" - [GRASS GIS in the cloud: actinia geoprocessing](https://mundialis.github.io/foss4g2019/grass-gis-in-the-cloud-actinia-geoprocessing/index.html) (note: it requires the Chrome/ium browser; presentation provided by <a href="https://github.com/mmacata/">Carmen Tawalika</a>, mundialis).

-->
