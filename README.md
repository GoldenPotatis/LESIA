# LESIA  building load culstering analysis tool

The full name of LESIA project is: **Community-based Local Energy System in Industrial Areas in Sweden**.  
Introduction of LESIA project can be found at RISE website [LESIA](https://www.ri.se/en/what-we-do/projects/community-based-local-energy-system-in-industrial-areas-in-sweden).

The Working Package 3 (WP3) of LESIA project aims at the investigation, evaluation, and analysis of current energy systems of industrial areas in Sweden in general and one specific case study (Viared industrial area in Borås). Two tasks in WP3 are to gather energy data from stakeholders and map the current energy systems in Viared. After collecting the electricity consumption data, there is a need to analyse the energy data for mapping the system. Therefore, this repository is intended to fill this gap.  

This repository contains a tool that can automatically take in a building's electricity consumption data and perform electricity load profile clustering analysis.
The building's electricity consumption data should be a time series data that contains 8760 hours recordings.
The tool can take in the data and perform the following tasks:
### 1. Data cleaning and preperation
* **Check missing values**  
  Detect and remove missing values and set to 0
* **Check outliers**  
  Using IOR method to detect outliers and set to 0
* **Fill missing values and outliers**  
  Using simple moving average method to fill the detected missing values and outliers with a window size 3
* **Data segmentation**  
  Segment the 8760 hours time series data into daily form of 365 days $\times$ 24 hours
* **Data normalisation**  
  Using annual electricity consumption max to normalise the raw data  
  $x_{normalised} = \Large\frac{x_{raw}}{x_{annual max}}$

### 2. Clustering analysis and visualisation

