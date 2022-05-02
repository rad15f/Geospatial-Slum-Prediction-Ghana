# Poverty-Mapping-using-ML
The overall objective of the work is to develop a reproducible, semi-automated approach to map the urban poverty level in Accra, Ghana. This model aims to detect poverty locations and their characteristics to assist urban planning and management. 

### Steps to Run 

1. Clone this repo
2. Install the necesary packages (Check Requirements)
3. Download the Data folder & Output Folder and put it on your path
4. Run Data_preprocessing.ipynb
5. Run Real_Training_Model.ipynb
6. Run and Enjoy!

### Background
The United Nations estimates that around 3 billion people might live in slums by 2030 if no action is taken. Slum areas lack adequate basic services, household assets, durable housing and are often located in hazardous areas with multiple deprivations. Additionally, slums are highly vulnerable to climate change due to their locations, such as flood zones, steep slopes, and low-quality building structures. It is believed that climate change impact will increasingly intensify deprived living conditions. To adequately map them requires data on their location, characteristics, and evolution. The absence of data on slums and their characteristics limits our capacity to plan and intervene in such areas. It is also required for Sustainable Development Goals 11 and 13 and local strategies.  This project will develop a start-of-the-art methodology that combines earth observation, open data, and machine learning to map urban poverty. The project will develop an innovative multi-dimensional approach that combines rich and diverse data to map urban poverty and prioritize hotspots supporting local action.

### Requirements
* Use a geopastial environment, Jupyter Hub and selecting Geospatial Environment is strongly recommended
! pip install seaborn
! pip install statsmodels
! pip install contextily
!pip install distancerasters
import requests
import json
import pandas as pd
import numpy as np
import geopandas as gpd
import os
import fiona
import contextily as ctx
from glob import glob
import geowombat as gw
from geowombat.ml import fit, fit_predict 
https://geowombat.readthedocs.io/en/latest/install.html

### Machine Learning Algorithmss:
- Random Forest
- Gradient Boosting

### Description of files:
Data_preprocessing: obtaining necessaries datasets, calculating eucleadian distance, ndvi 
Real_Training_Model: using our training set which we created on QGIS and using geowombat as a cookie cuter to combine the training set to the dataset with the bands and calculated bands(highway,market,industry) and running our models with sklearn and geowombat
