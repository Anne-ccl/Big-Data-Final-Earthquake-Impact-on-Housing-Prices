# Earthquake-Impact-on-Housing-Prices

Earthquake-Impact-on-Housing-Prices

## Project Description

[Enter a brief description of your project, including the data you used and the analytical methods you applied. Be sure to provide context for your project and explain why it is important.]

### Introduction
Taiwan is located on the Pacific Ring of Fire, making it prone to frequent and significant earthquakes. These seismic events can have substantial impacts on various aspects of society, particularly the housing market. Understanding how earthquakes affect housing prices is essential for policymakers, investors, and urban planners to develop strategies that enhance resilience and preparedness.

This study focuses on the 2016 Meinong Earthquake, which had a magnitude of 6.4 and struck Kaohsiung, Taiwan, on February 6, 2016. This earthquake caused extensive damage and highlighted the vulnerability of Taiwan's housing infrastructure. By analyzing real estate data from 2015 to 2017, this study examines areas that experienced earthquake magnitudes of four or above. These areas include cities such as Miaoli, Taichung, Changhua, Nantou, Yunlin, Chiayi City, Chiayi County, Tainan, Kaohsiung, Pingtung, Hualien, and Taitung. The goal is to determine the earthquake's impact on housing prices and trading activities in the affected regions, providing valuable insights for future urban planning and investment strategies to ensure better preparedness for similar events in the future.

Earthquakes can directly affect housing prices, but other factors such as medical resources and education levels can also influence them. Therefore, we decided to use regression analysis to process relevant data from 2014 to 2018. This method can reveal the relationship between earthquakes and housing prices while also exploring how these relationships are influenced by population dynamics, medical resources, and education levels. The results of such an analysis can provide scientific evidence for policymakers, helping them formulate more effective strategies to enhance urban resilience and promote sustainable socio-economic development. Additionally, regression analysis can identify key factors, aiding in the rational allocation of resources and precise policy-making.

By utilizing data sources from the Ministry of the Interior's National Land Surveying and Mapping Center, the Social and Economic Data Service Platform, and the Central Weather Bureau's Seismological Center, we aim to conduct a comprehensive analysis. This analysis will not only assess the direct impacts of earthquakes on housing prices but also explore the broader socio-economic factors, such as population dynamics, medical resources, and education levels, that contribute to these effects. By integrating diverse datasets and applying advanced regression analysis techniques, we seek to provide a detailed understanding of the multifaceted influences on the housing market, ultimately offering valuable insights for policymakers, investors, and urban planners.
### Objectives
1. Assess the Impact of Earthquakes on Housing Prices:
   Determine whether the 2016 Meinong Earthquake significantly affected housing prices and geographic mobility from 2016 to 2017.
2. Analyze Contributing Factors:
   Explore the relationships between earthquake intensity, housing prices, and geographic mobility, considering other influencing factors such as population size, medical resources, and education levels.
3. Provide Strategic Insights:
   Offer recommendations for future urban planning and investment decisions based on the findings.
### Hypotheses
1. Did the 2016 Meinong Earthquake significantly impact housing prices and geographic mobility in areas with a magnitude of four or above from 2015 to 2017?
2. What are the relationships between earthquake occurrences, housing prices, and geographic mobility, and how are these relationships influenced by factors such as population dynamics, medical resources, and education levels?

## Getting Started

[Provide instructions on how to get started with your project, including any necessary software or data. Include installation instructions and any prerequisites or dependencies that are required.]

### Prerequisites
To get started with this project, you will need the following:

1. RStudio
- R (version 3.6.3 or later)
- Required R packages: dplyr, tidyr, ggplot2, lmtest, etc.

### Installation
1. Install R and RStudio:
- Download and install R from CRAN.
- Download and install RStudio from RStudio.
2. Install the necessary R packages:

Open RStudio and run the following commands in the console:
```
install.packages("dplyr")
install.packages("tidyr")
install.packages("readr")
install.packages("openxlsx")
install.packages("lmtest")
install.packages("ggplot2")
install.packages("sf")
install.packages("viridis")
install.packages("rnaturalearth")
install.packages("rnaturalearthdata")
install.packages("spData")
```
### Raw Data
The raw data used in this project includes:

- 20160206 Meinong Earthquake (Seismic Intensity Classification Table)
- Housing prices: Taiwan All Region Real Estate Transaction Dataset 2015-2017
- Taiwan All Region Geographic Mobility 2016
- Number of Medical Clinics in Townships and Towns in 2016
- Education Level of Taiwanese Population 2016
- Social increase rate (migration rates) 2016
- Population size 2016
- Aging index 2016
- Salary income 2016

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

3.Regression Models:
1. Housing Price Difference Regression Analysis (With Interaction Terms)
<img src= "https://github.com/Anne-ccl/Big-Data-Final-Earthquake-Impact-on-Housing-Prices/assets/172912236/400efab4-8ef0-4d21-a09a-638a669709cf)" alt="image" width="400"/>

Model Summary:
Formula: Housing Price Difference 15_17 ~ Earthquake Magnitude * Social Growth Rate 2016 + Population Density 2016 + EDU_RATE + Aging Index 2016 + Labor Force Participation Rate 2016 + Total Population 2016 + Low-Income Household Ratio 2016 + Income and Salary Earnings 2016 + Medi_Service

Adjusted R-squared: 0.09009
F-statistic: 4.308, p-value < 0.001, highly significant

Key Coefficients and Interpretation:
Social Growth Rate 2016: Coefficient = -1.394e+04, p-value < 0.001. Significant negative correlation, indicating that higher social growth rates are associated with smaller changes in housing prices.
Total Population 2016: Coefficient = 1.594e-03, p-value < 0.001. Significant positive correlation, indicating that higher total population is associated with greater changes in housing prices.
Income and Salary Earnings 2016: Coefficient = 7.941e-04, p-value < 0.001. 

Significant positive correlation, indicating that higher income and salary earnings are associated with greater changes in housing prices.





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



### Process

## Results

[Provide a summary of your findings and conclusions, including any recommendations or implications for future research. Be sure to explain how your results address your research question or problem statement.]

The preliminary results suggest that housing prices are more closely related to the social increase rate (net migration) than to earthquake intensity. Specifically, the analysis indicates that areas with higher rates of population influx tend to experience more significant changes in housing prices, irrespective of earthquake intensity. These findings highlight the importance of social and demographic factors over purely geological ones in influencing the housing market.


### Future Research
Given the initial findings, future research should delve deeper into the impact of social changes, such as migration patterns and demographic shifts, on housing prices. Further studies could investigate:

1. Long-Term Effects: Examining the long-term impacts of population dynamics on housing prices beyond the immediate aftermath of an earthquake.
2. Detailed Demographic Analysis: Analyzing the specific characteristics of migrating populations, such as age, income level, and occupation, to understand their influence on housing market trends.
3. Comparative Studies: Conducting comparative studies between regions with similar seismic activity but different social dynamics to identify the relative impact of each factor.

By expanding the scope of research to include these aspects, we can gain a more comprehensive understanding of the factors influencing real estate markets in areas prone to natural disasters. This knowledge will support better decision-making for urban planning, investment strategies, and disaster preparedness initiatives.

## Contributors

[List the contributors to your project and describe their roles and responsibilities.]

Data Collection： Yvonne, Nina, Anne, Nora

Programmer of the Project (Including Data Cleaning and Analysis): Yvonne, Nina

Writer: Anne, Nora


## Acknowledgments

[Thank any individuals or organizations who provided support or assistance during your project, including funding sources or data providers.]

We extend our gratitude to Professor Pien Chung-Pei for his invaluable guidance and support throughout the semester. His insights and feedback were instrumental in the development of this project.

## References

[List any references or resources that you used during your project, including data sources, analytical methods, and tools.]

### Data Sources

| Resource | File Name |
|-------------|-------------------------------|
| 氣象署地震測報中心 | 20160206美濃各地震度原始資料(ASCI) |
| 內政部不動產成交案件實際資訊資料供應系統| 縣市鄉鎮不動產成交案件資訊(含不動產買賣+預售屋買賣+不動產租賃) |
| | 醫療院所 |
| 社會經濟資料服務平台 | 105年12月行政區人口指標_鄉鎮市區 |
| | 105年12月行政區三段年齡組性別人口統計_鄉鎮市區 |
| |105年行政區15歲以上人口教育程度統計_鄉鎮市區 | 
| |105年綜合所得稅各類所得金額統計_鄉鎮市區 |
| |104-106年行政區人口消長統計_鄉鎮市區 |
| |104-106年行政區人口消長統計指標_鄉鎮市區 |
| 內政部國土測繪中心 | 台灣鄉鎮市區界線(TWD97經緯度) |

### Tools
- R Studio















