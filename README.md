# The Relationship Between Earthquakes and Housing Prices

## Project Description

### Introduction
Taiwan is located on the Pacific Ring of Fire, making it prone to frequent and significant earthquakes. These seismic events can substantially impact various aspects of society, particularly the housing market. Understanding how earthquakes affect housing prices is essential for policymakers, investors, and urban planners to develop strategies that enhance resilience and preparedness.

This project focuses on the 2016 Meinong Earthquake, which had a magnitude of 6.4 and struck Kaohsiung, Taiwan, on February 6, 2016. This earthquake caused extensive damage and highlighted the vulnerability of Taiwan's housing infrastructure. By analyzing real estate data from 2015 to 2017, this study examines areas that experienced earthquake magnitudes of four or above. These areas include Miaoli, Taichung, Changhua, Nantou, Yunlin, Chiayi City, Chiayi County, Tainan, Kaohsiung, Pingtung, Hualien, and Taitung. The goal is to determine the earthquake's impact on housing prices and trading activities in the affected regions, providing valuable insights for future urban planning and investment strategies to ensure better preparedness for similar events in the future.

Earthquakes can directly affect housing prices, but other factors, such as medical resources and education levels, can also influence them. Therefore, we used regression analysis to process relevant data from 2014 to 2018. This method can reveal the relationship between earthquakes and housing prices while exploring how population dynamics, medical resources, and education levels influence these relationships. The results of such an analysis can provide scientific evidence for policymakers, helping them formulate more effective strategies to enhance urban resilience and promote sustainable socio-economic development. Additionally, regression analysis can identify key factors, aiding in the rational allocation of resources and precise policy-making.

By utilizing data sources from the Ministry of the Interior's National Land Surveying and Mapping Center, the Social and Economic Data Service Platform, and the Central Weather Bureau's Seismological Center, we aim to conduct a comprehensive analysis. This analysis will assess the direct impacts of earthquakes on housing prices and explore the broader socio-economic factors, such as population dynamics, medical resources, and education levels, that contribute to these effects. By integrating diverse datasets and applying advanced regression analysis techniques, we seek to provide a detailed understanding of the multifaceted influences on the housing market, ultimately offering valuable insights for policymakers, investors, and urban planners.

### Objectives
1. Assess the Impact of Earthquakes on Housing Prices: Determine whether the 2016 Meinong Earthquake significantly affected housing
   prices and geographic mobility from 2016 to 2017.
2. Analyze Contributing Factors: Explore the relationships between earthquake intensity, housing prices, and geographic mobility,
   considering other influencing factors such as population size, medical resources, and education levels.
3. Provide Strategic Insights: offering practical recommendations based on the insights gained from the study.

### Hypotheses
1. Did the 2016 Meinong Earthquake significantly impact housing prices and geographic mobility in areas with a magnitude of four or       above from 2016 to 2017?
2. What intricate relationships exist between earthquake occurrences, housing prices, and geographic mobility, and how are these          relationships intricately influenced by population dynamics, medical resources, salary income, and education levels?

## Getting Started

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
install.packages("leaflet")
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
.
├── Folder 1:Population growth and decline statistics between 2015-2017
├── Folder 2:Population growth and decline statistical indicators 2015-2017
├── Folder 3:Other Demographic Indicators/
│   ├── a.Administrative District Population Indicators
│   ├── b.Gender Demographics of three age groups in December 2016
│   ├── c.Statistical indicators of low and middle income households in December 2016
│   ├── d.Individual Income Tax Statistics in December 2016
│   └── e.Statistics on the Education Level of the Population 2016
├── Folder 4:Medical Resources 
├── Folder 5:Visualization Results
├── File: House Price 2014_2018
├── File: 2016 Meinong Earthquake Intensity Record
└── File: Earthquake-Impact-on-Housing-Prices (R Code File)


## Analysis

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

3. Regression Models

In regression analysis, the purpose of introducing interaction terms is to explore the mutual influence between two variables. Specifically, interaction terms help us understand how one variable affects the effect of another variable. In your analysis, the interaction term between earthquake magnitude and social growth rate was included in the model, which helps us understand how these two variables jointly impact housing price differences and transaction case differences.


**(1) Housing Price Difference Regression Analysis (With Interaction Terms)**

<img src= "https://github.com/Anne-ccl/Big-Data-Final-Earthquake-Impact-on-Housing-Prices/assets/172912236/400efab4-8ef0-4d21-a09a-638a669709cf)" alt="image" width="400"/>

Model Summary:

Formula: Housing Price Difference 15_17 ~ Earthquake Magnitude * Social Growth Rate 2016 + Population Density 2016 + EDU_RATE + Aging Index 2016 + Labor Force Participation Rate 2016 + Total Population 2016 + Low-Income Household Ratio 2016 + Income and Salary Earnings 2016 + Medi_Service

Housing Price Difference Regression Analysis
The interaction term (Earthquake Magnitude * Social Growth Rate 2016) is **significantly positively correlated**, indicating that the interaction between earthquake magnitude and social growth rate significantly affects housing price differences. This means that in areas with higher social growth rates, the impact of earthquakes on housing price differences is more pronounced. In other words, the higher the social growth rate, the greater the impact of earthquakes on housing prices.

**(2) Transaction Case Difference Regression Analysis (With Interaction Terms)**

<img src= "https://github.com/Anne-ccl/Big-Data-Final-Earthquake-Impact-on-Housing-Prices/assets/172912236/32437372-b2fb-4ced-a2c5-11f1c5fde376)" alt="image" width="400"/>

Model Summary:

Formula: Transaction Case Difference ~ Earthquake Magnitude * Social Growth Rate 2016 + EDU_RATE + Aging Index 2016 + Labor Force Participation Rate 2016 + Total Population 2016 + Population Density 2016 + Low-Income Household Ratio 2016 + Income and Salary Earnings 2016 + Medi_Service

In the transaction case difference regression analysis, although the interaction term is **not significant**, considering the interaction between total population and income levels still shows significant effects. This highlights the importance of population and income levels in explaining transaction case differences.

**Comprehensive Analysis**
1. Interaction Between Social Growth Rate and Earthquake Magnitude:

In the housing price difference analysis, the social growth rate is significantly negatively correlated, but the interaction term (Earthquake Magnitude: Social Growth Rate 2016) is significantly positively correlated. This indicates that in areas with a higher social growth rate, the impact of the earthquake on housing price differences is more pronounced.
In the transaction case difference analysis, the interaction term between social growth rate and earthquake magnitude does not have a significant effect, but total population and income levels significantly affect transaction case differences.

2. Total Population:

In the transaction case difference analysis, total population is significantly positively correlated, indicating that higher total population is associated with greater differences in transaction cases. This may reflect more frequent trading activity in areas with larger populations.

3. Various Income Amounts_Salary Income:

In the transaction case difference analysis, various income amounts are significantly negatively correlated, indicating that higher income levels are associated with smaller differences in transaction cases. This may suggest that real estate markets in higher-income areas are more stable, with less transaction volatility.

4. Earthquake Magnitude:

In the housing price difference analysis, the main effect of earthquake magnitude is not significant, but its interaction with the social growth rate is significant, suggesting that the impact of the earthquake on housing price differences is significant in the context of social growth rate.

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

**Social Growth Rate** and **Total Population** are important factors influencing housing price and transaction differences.
Earthquake Impact has a significant effect on housing price differences through its interaction with social growth rate, indicating that in areas with higher social growth rates, the impact of earthquakes on housing prices is more pronounced.
Various Income Amounts: Salary Income has a significant stabilizing effect on transaction case differences, suggesting that real estate markets in higher-income areas experience less volatility.

The preliminary results suggest that housing prices are more closely related to the social increase rate (net migration) than to earthquake intensity. Specifically, the analysis indicates that areas with higher rates of population influx tend to experience more significant changes in housing prices, irrespective of earthquake intensity. These findings highlight the importance of social and demographic factors over purely geological ones in influencing the housing market.

## Project Limitations

This project mainly analyzes the data on house price differences and transaction case differences. If we want to optimize data processing, we believe that we should collect the actual housing price registration prices in various places to make it more complete. In addition, due to the limited time for collecting data and the difficulty of collecting commercial data, this became the limitation of this project.

### Future Research
Given the initial findings, future research should delve deeper into the impact of social changes, such as migration patterns and demographic shifts, on housing prices. Further studies could investigate:

1. Long-Term Effects: Examining the long-term impacts of population dynamics on housing prices beyond the immediate aftermath of an earthquake.
2. Detailed Demographic Analysis: Analyzing the specific characteristics of migrating populations, such as age, income level, and occupation, to understand their influence on housing market trends.
3. Comparative Studies: Conducting comparative studies between regions with similar seismic activity but different social dynamics to identify the relative impact of each factor.

By expanding the scope of research to include these aspects, we can gain a more comprehensive understanding of the factors influencing real estate markets in areas prone to natural disasters. This knowledge will support better decision-making for urban planning, investment strategies, and disaster preparedness initiatives.

## Contributors

Data Collection： Yvonne, Nina, Anne, Nora

Programmer of the Project (Including Data Cleaning and Analysis): Yvonne, Nina

Writer: Anne, Nora

## Acknowledgments

We are deeply thankful to Professor Pien Chung-Pei for his invaluable guidance and support throughout the semester, which greatly influenced the development of our project. We also extend our appreciation to the organizations and individuals whose contributions and assistance were essential to our success, including our funding sources and data providers. His insightful feedback and constructive criticism were pivotal in shaping the direction and refining the methodologies of our project.

Furthermore, we express our sincere appreciation to the government open data platforms. Their funding enabled us to access essential resources and tools, facilitating our research and analysis. Special thanks are also due to our data providers on these platforms, whose reliable datasets and cooperation were essential in conducting thorough and meaningful analyses.

## References

### Data Sources

| Resource | File Name |
|-------------|-------------------------------|
| 氣象署地震測報中心 | 20160206美濃各地震度原始資料(ASCI) |
| 內政部不動產成交案件實際資訊資料供應系統| 縣市鄉鎮不動產成交案件資訊(含不動產買賣+預售屋買賣+不動產租賃) |
| 衛生福利部 | Medical Resources File |
| 社會經濟資料服務平台 | 105年12月行政區人口指標_鄉鎮市區 |
| | 105年12月行政區三段年齡組性別人口統計_鄉鎮市區 |
| |105年行政區15歲以上人口教育程度統計_鄉鎮市區 | 
| |105年綜合所得稅各類所得金額統計_鄉鎮市區 |
| |104-106年行政區人口消長統計_鄉鎮市區 |
| |104-106年行政區人口消長統計指標_鄉鎮市區 |
| 內政部國土測繪中心 | 台灣鄉鎮市區界線(TWD97經緯度) |

### Tools
- R Studio
