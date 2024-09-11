# Data-Analysis

**Project Overview**

I conducted an extensive data analysis project using raw JSON data from an online environment, analyzing over 180 days' worth of interaction logs. This exercise focused on turning complex, unstructured data into meaningful insights through data cleaning, transformation, and visualization techniques.

**Key Data**

The data consisted of player interaction logs with fields including player identifiers, timestamps, locations (x, y, z coordinates), event types, and metadata about actions taken (such as the tools or methods used). This unstructured data required significant cleanup and filtering to extract useful insights.

**Data Transformation Process**

The dataset was processed using R and Excel, where each event was categorized into variables such as:

- Kill, death, or suicide counts
- Weapon usage frequency
- Player location-based interactions (including proximity to key locations)
- Temporal analysis (active hours and days)

I also implemented tier-based filtering to classify player actions according to their levels, allowing deeper analysis of patterns in player behavior across different groups.

**Data Analysis**

Several metrics were computed from the cleaned data, including:

- Frequency Analysis: Daily kill, death, and suicide rates
- Spatial Analysis: Interaction heat maps overlaid onto grids, calculating the kill-to-death ratio (KDR) and economic impact (deaths resulting in penalties)
- Temporal Trends: Identifying peak periods of activity, weapon usage patterns across time, and shifts in behavior
- Player Classification: Segmentation of high-skill players using clustering algorithms based on performance data

**Visualizations**

Using R's ggplot2 library, I developed several visualizations:

- Heat Maps: Generated spatial maps of player interactions, highlighting high-activity zones and the financial impact of deaths
- Altitude Maps: Analyzed player interactions across different elevation levels using geospatial techniques
- Trend Analysis: Temporal patterns in activity, showing spikes in interactions and changes in behavior over time

**Outcomes and Insights**

Through this project, I gained extensive experience in transforming unstructured data into a structured format suitable for advanced analysis. This project allowed me to hone my skills in:

- Cleaning and transforming large, unstructured datasets
- Performing complex frequency and spatial analysis
- Utilizing visualization tools for clear communication of insights
