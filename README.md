# Smartprix-Smartphone-analysis
### Highlights and Key Points from the SMARTPRIX SMARTPHONES Project
#### Project Overview:
**Objective:** Gathered, cleaned, and analyzed smartphone data from the Smartprix website through web scraping to gain insights into the smartphone market.
#### Web Scraping:
**Tools:** Used Selenium to automate browser interaction and BeautifulSoup to parse HTML content.
**Data Extracted:** Collected information such as model names, prices, operating systems, SIM card types, processors, RAM, battery capacity, display details, camera specifications, and memory card support.
**Challenge:** Handling dynamic content on the Smartprix website, solved by automating clicks and using Selenium.
#### 2. Data Cleaning:
	**Issues Identified:**
**Inconsistent brand names:** Differences in case sensitivity (e.g., "SAMSUNG" vs. "Samsung").
**Irrelevant or misplaced data:** Information such as OS, Bluetooth, and FM radio appeared incorrectly in columns like memory card.
**Outliers:** Some extreme values, like the inclusion of gold- and diamond-made phones, were removed as they didn’t represent regular smartphone pricing.
#### 3.  Steps Taken:
Converted object columns (e.g., price, RAM, and internal memory) to appropriate data types for analysis.
Filled missing values using techniques like KNNImputer for numerical data and SimpleImputer for categorical data.
Created new columns for features like 5G, NFC, and IR blasters based on SIM information.
#### 4. Splitting Columns:
	**Multi-Value Columns:** Separated data like battery, processor, display, and camera 
	specs into individual columns for better analysis.
#### 5. Outliers and Inconsistent Data:
Outliers (such as phones made of precious materials like gold or diamond) were removed.
Misplaced data was shifted to the correct columns (e.g., battery data in the wrong column was shifted).
#### 6. Exploratory Data Analysis (EDA):
	Key Insights:
**Price and 5G:** Smartphones with 5G have a median price 130.67% higher than those without 5G. 56.85% of smartphones in the dataset are equipped with 5G.
**Brand Market Share:** Xiaomi and Samsung dominate the market by covering 29.8% of smartphone models. Additionally, 75% of smartphone brands offer more 5G models than non-5G models.
**Processor and Price:** Apple’s hexa-core processors, found in 95.12% of iOS devices, contribute to the highest average (median) prices, making these smartphones 325.25% more expensive than octa-core models. Snapdragon covers 43.57% of Android models, followed by Dimensity, focusing on mid- to high-end price ranges.
**Battery:** 51.76% of smartphones have a 5000mAh battery capacity. Smartphones with larger battery capacities tend to have higher prices, with those offering fast charging priced 121.05% higher than those without.
**NFC and Price:** Smartphones with NFC are 166.67% more expensive than those without. NFC is present in 97.83% of Apple’s models, while 34.86% of Android models feature it.
**Camera and Price:** 57.4% of smartphones have 3 rear cameras, and prices increase with the number of cameras up to 3. Models with 4 rear cameras are slightly cheaper but still priced higher than those with 2 cameras.
**Operating System:** 93.9% of smartphones run on Android, while iOS models account for 5.2%. iOS smartphones are priced 347.37% higher than Android models on average.
**Memory:** 63.8% of smartphones offer extended memory options, but smartphones without extended memory are priced 166.68% higher.
#### 7. Statistical Analysis:
**Spearman's Rho Test:** Used to assess the strength and direction of the association between variables.
**Kendall's Tau Correlation:** Employed to measure the ordinal association between two quantities.
**Point-Biserial Correlation Coefficient:** Applied to understand the relationship between binary and continuous variables.
**Cramer's V Coefficient:** Used to measure the strength of association between two nominal variables.
**Shapiro-Wilk Test for Normality:** Conducted to assess the normality of the data distribution.
**Kruskal-Wallis Test Statistic:** Used to determine if there are statistically significant differences between three or more independent groups.
**Chi-square Statistic:** Utilized to assess the relationships between categorical variables.
**Dunn Test:** Performed as a post-hoc test to determine which specific groups' means (or medians) are different after a Kruskal-Wallis test.
**Spearman Correlation Coefficient:** Bootstrapping Analysis: Used to validate the robustness of the Spearman correlation coefficient through resampling methods.
#### 8. Challenges and Solutions:
**Missing Values:** Used advanced imputation techniques such as KNNImputer for numerical data and SimpleImputer for categorical data to handle missing values.
**Inconsistent Data:** Standardized text fields, removed irrelevant information, and ensured all numerical data was in the correct format.
**Impact of Data Cleaning:**
**Improved Data Quality**: The cleaned dataset is more reliable for analysis, with improved accuracy, completeness, and relevance.
**Outliers and Inconsistencies:** Removed, corrected, and addressed.
#### Final Dataset:

The final dataset was structured, clean, and ready for further analysis with reduced rows, corrected values, and consistent data types.


