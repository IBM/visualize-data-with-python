# Visualize and analyze data from the 2017 flood in Houston, TX using a Jupyter Notebook on IBM Watson Studio

In this Code Pattern we will use some standard techniques for data science and data engineering running on IBM Watson Studio to analyze publicly available data for the 2017 flooding in Houston, TX. Watson Studio is an interactive, collaborative, cloud-based environment where data scientists, developers, and others interested in data science can use tools (e.g., RStudio, Jupyter Notebooks, Spark, etc.) to collaborate, share, and gather insight from their data.

When the reader has completed this Code Pattern, they will understand how to:

* Use [Jupyter Notebooks](https://jupyter.org/) to load, visualize, and analyze data
* Run Notebooks in [IBM Watson Studio](https://dataplatform.cloud.ibm.com/)
* Leverage [PixieDust](https://github.com/pixiedust/pixiedust) as a python notebook helper
* Build a dashboard using [PixieApps](https://pixiedust.github.io/pixiedust/pixieapps.html)
* Find, curate, and display publicly available data
* Create an interactive map with [Mapbox GL](https://www.mapbox.com/mapbox-gl-js/api/)

The intended audience for this Code Pattern is application developers and other stakeholders who wish to utilize the power of Data Science quickly and effectively.

## Flow

![architecture](doc/source/images/architecture.png)

1. Load the Jupyter notebook onto the IBM Watson Studio platform.
1. USGS data from the Houston flood of 2017 is loaded into the notebook.
1. The notebook is used to clean the data, and then  display it.
1. A PixieApp dashboard is created and can be interacted with.
1. Mapbox and Folium are used for map visualizations

## Included technologies

* [IBM Watson Studio](https://www.ibm.com/cloud/watson-studio): Analyze data using RStudio, Jupyter, and Python in a configured, collaborative environment that includes IBM value-adds, such as managed Spark.
* [Jupyter Notebooks](https://jupyter.org/): An open-source web application that allows you to create and share documents that contain live code, equations, visualizations and explanatory text.
* [PixieDust](https://github.com/pixiedust/pixiedust) Python helper library for python notebooks
* [PixieApps](https://pixiedust.github.io/pixiedust/pixieapps.html): Python library used to write UI elements for analytics, and run them directly in a Jupyter notebook.
* [Mapbox GL](https://www.mapbox.com/mapbox-gl-js/api/): JavaScript library that uses WebGL to render interactive maps.

## Prerequisites

* An account on IBM Cloud to access [Watson Studio](https://www.ibm.com/cloud/watson-studio)
* Get a [Mapbox Token](https://www.mapbox.com/) for use in the notebook

## Steps

Follow these steps to setup and run this Code Pattern. The steps are
described in detail below.

1. [Sign up for the Watson Studio](#1-sign-up-for-watson-studio)
2. [Create the notebook](#2-create-the-notebook)
3. [Run the notebook](#3-run-the-notebook)

### 1. Sign up for Watson Studio

Sign up for IBM's [Watson Studio](https://dataplatform.cloud.ibm.com/). By creating a project in Watson Studio a free tier ``Object Storage`` service will be created in your IBM Cloud account. Take note of your service names as you will need to select them in the following steps.

> Note: When creating your Object Storage service, select the ``Free`` storage type in order to avoid having to pay an upgrade fee.

### 2. Create the notebook

* In [Watson Studio](https://dataplatform.cloud.ibm.com/), click `New Project +` under Projects or, at the top of the page click `+ New` and choose the tile for `Data Science` and then `Create Project`.
* In [Watson Studio](https://dataplatform.cloud.ibm.com/) using the project you've created, click on `+ Add to project` and then choose the  `Notebook` tile, OR in the `Assets` tab under `Notebooks` choose `+ New notebook` to create a notebook.
* Select the `From URL` tab. [1]
* Enter a name for the notebook. [2]
* Optionally, enter a description for the notebook. [3]
* Under `Notebook URL` provide the following url: [https://raw.githubusercontent.com/IBM/visualize-data-with-python/master/notebooks/HoustonFlood2017.ipynb](https://raw.githubusercontent.com/IBM/visualize-data-with-python/master/notebooks/HoustonFlood2017.ipynb) [4]
* For `Runtime` select the `Spark Python 3.6` option. [5]
* Click the `Create notebook` button. [6]

![Create Notebook](doc/source/images/DataVisualizationCreateNotebook.png)

### 3. Run the notebook

> NOTE: See the points in the notebook where you will have to enter your [Mapbox Token](https://www.mapbox.com) to render the map.

When a notebook is executed, what is actually happening is that each code cell in
the notebook is executed, in order, from top to bottom.

Each code cell is selectable and is preceded by a tag in the left margin. The tag
format is `In [x]:`. Depending on the state of the notebook, the `x` can be:

* A blank, this indicates that the cell has never been executed.
* A number, this number represents the relative order this code step was executed.
* A `*`, this indicates that the cell is currently executing.

There are several ways to execute the code cells in your notebook:

* One cell at a time.
  * Select the cell, and then press the `Play` button in the toolbar.
* Batch mode, in sequential order.
  * From the `Cell` menu bar, there are several options available. For example, you
    can `Run All` cells in your notebook, or you can `Run All Below`, that will
    start executing from the first cell under the currently selected cell, and then
    continue executing all cells that follow.
* At a scheduled time.
  * Press the `Schedule` button located in the top right section of your notebook
    panel. Here you can schedule your notebook to be executed once at some future
    time, or repeatedly at your specified interval.

## Sample Output

> Note: Some interactive map functionality, like ```Options``` and ```Layers``` will not work. To see these, you must run the notebook itself.

## License

This code pattern is licensed under the Apache Software License, Version 2.  Separate third party code objects invoked within this code pattern are licensed by their respective providers pursuant to their own separate licenses. Contributions are subject to the [Developer Certificate of Origin, Version 1.1 (DCO)](https://developercertificate.org/) and the [Apache Software License, Version 2](https://www.apache.org/licenses/LICENSE-2.0.txt).

[Apache Software License (ASL) FAQ](https://www.apache.org/foundation/license-faq.html#WhatDoesItMEAN)
