# ici_template [This section can be removed in the submission version]111
This GitHub repository offers a template specifically designed to teach students how to write effective README.md files and create a well-organized file structure. The template provides clear instructions and exampls, helping students to learn the basics of GitHub and how to create professional-looking repositories.
12345678

# Earthquake-Impact-on-Housing-Prices

Earthquake-Impact-on-Housing-Prices

## Project Description

[Enter a brief description of your project, including the data you used and the analytical methods you applied. Be sure to provide context for your project and explain why it is important.]

### Introduction
Taiwan is located on the Pacific Ring of Fire, making it prone to frequent and significant earthquakes. These seismic events can have substantial impacts on various aspects of society, particularly the housing market. Understanding how earthquakes affect housing prices is essential for policymakers, investors, and urban planners to develop strategies that enhance resilience and preparedness.

This study focuses on the 2016 Meinong Earthquake, which had a magnitude of 6.4 and struck Kaohsiung, Taiwan, on February 6, 2016. This earthquake caused extensive damage and highlighted the vulnerability of Taiwan's housing infrastructure. By analyzing real estate data from 2014 to 2018, focuses on areas that experienced earthquake magnitudes of four or above, including cities such as Miaoli, Taichung, Changhua, Nantou, Yunlin, Chiayi City, Chiayi County, Tainan, Kaohsiung, Pingtung, Hualien, and Taitung., this project aims to determine the earthquake's impact on housing prices and trading activities in the affected regions, and provides valuable insights for future urban planning and investment strategies, ensuring better preparedness for similar events in the future.
### Objectives
1. Assess the Impact of Earthquakes on Housing Prices:
   Determine whether the 2016 Meinong Earthquake significantly affected housing prices and geographic mobility from 2016 to 2018.
2. Analyze Contributing Factors:
   Explore the relationships between earthquake intensity, housing prices, and geographic mobility, considering other influencing factors such as population size, medical resources, and education levels.
3. Provide Strategic Insights:
   Offer recommendations for future urban planning and investment decisions based on the findings.
### Hypotheses
1. Did the 2016 Meinong Earthquake significantly impact housing prices and geographic mobility in areas with a magnitude of four or above from 2016 to 2018?
2. What are the relationships between earthquake occurrences, housing prices, and geographic mobility, and how are these relationships influenced by factors such as population dynamics, medical resources, and education levels?

## Getting Started

[Provide instructions on how to get started with your project, including any necessary software or data. Include installation instructions and any prerequisites or dependencies that are required.]

### Prerequisites
To get started with this project, you will need the following:

1. RStudio
- R (version 3.6.3 or later)
- Required R packages: dplyr, tidyr, ggplot2, lmtest

### Installation
1. Install R and RStudio:
- Download and install R from CRAN.
- Download and install RStudio from RStudio.
2. Install the necessary R packages:

Open RStudio and run the following commands in the console:
```
install.packages("dplyr")
install.packages("tidyr")
install.packages("ggplot2")
install.packages("lmtest")
```
### Raw Data
The raw data used in this project includes:

- 20160206 Meinong Earthquake (Seismic Intensity Classification Table)
- Housing prices: Taiwan All Region Real Estate Transaction Dataset 2014-2018
- Taiwan All Region Geographic Mobility 2016
- Number of Medical Clinics in Townships and Towns in 2016
- Education Level of Taiwanese Population 2016

These datasets are crucial for performing the regression analysis and understanding the various factors affecting housing prices.


## File Structure

[Describe the file structure of your project, including how the files are organized and what each file contains. Be sure to explain the purpose of each file and how they are related to one another.]

The project is organized into the following directories and files: 


## Analysis

[Describe your analysis methods and include any visualizations or graphics that you used to present your findings. Explain the insights that you gained from your analysis and how they relate to your research question or problem statement.]

The analysis employs regression models to examine the relationship between earthquake intensity and housing prices. Specifically, we use two primary models:

1. Housing Transaction Volume Model: Uses housing transaction volume as the dependent variable.
2. Housing Price Difference Model: Uses housing price differences as the dependent variable.

Independent variables include:

- Earthquake intensity
- Population size (2016)
- Social increase rate (migration rates)
- Aging index
- Medical resources
- Education levels

### Methodology
1. Data Cleaning: Preprocess the raw data to ensure accuracy and consistency.
2. Regression Analysis: Build regression models to analyze the impact of earthquakes on housing prices.
3. Visualization: Create plots to visually represent changes in housing prices and earthquake intensity.
### Visualization
We provide visualizations such as simple plots showing changes in housing prices and earthquake intensity, helping to illustrate the findings clearly.

<img src="https://github.com/Anne-ccl/Big-Data-Final-Earthquake-Impact-on-Housing-Prices/assets/172906972/ab9b7e37-107d-4cda-9a4c-9939126db27e" alt="image" width="200"/>

**Figure 1. Earthquake Intensity of Meinong Earthquake (2016)**

___________________________________________________________________


<img src="https://github.com/Anne-ccl/Big-Data-Final-Earthquake-Impact-on-Housing-Prices/assets/172906972/3e0f58e1-df36-4448-8931-8e592215d3e1" alt="image" width="400"/>

**Figure 2. Variations in Property Prices & Earthquake Intensity (2015-2017)**

___________________________________________________________________


<img src="https://github.com/Anne-ccl/Big-Data-Final-Earthquake-Impact-on-Housing-Prices/assets/172906972/f8a34d52-6fb8-4861-b437-e1cdac2eca72" alt="image" width="400"/>

**Figure 3. Variations in Property Transaction Volumes & Earthquake Intensity (2015-2017)**



## Results

[Provide a summary of your findings and conclusions, including any recommendations or implications for future research. Be sure to explain how your results address your research question or problem statement.]

<img src="https://github.com/Anne-ccl/Big-Data-Final-Earthquake-Impact-on-Housing-Prices/assets/172906972/ab9b7e37-107d-4cda-9a4c-9939126db27e" alt="image" width="200"/>




## Contributors

[List the contributors to your project and describe their roles and responsibilities.]

## Acknowledgments

[Thank any individuals or organizations who provided support or assistance during your project, including funding sources or data providers.]

## References

[List any references or resources that you used during your project, including data sources, analytical methods, and tools.]
