# Data Analysis

**Project Overview**

I conducted an extensive data analysis project using raw JSON data from an online game environment, analyzing over 180 days' worth of interaction logs of 2 factions totaling around 230 players. This exercise focused on turning complex, unstructured data into meaningful insights through data cleaning, transformation, and visualization techniques.

**Key Data**

The data consisted of player kill-death logs with fields including player names and IDs, timestamp, location (x, y, z coordinates), weapon used, interior and world ID, and players' factions IDs. This unstructured data required significant cleanup and filtering to extract useful insights.

**Data Transformation Process**

The dataset was processed using R and Excel, where each death was filtered to extract elements such as:

- Kill, death, suicides (dying to the environment, i.e. not to a player), and deaths while in NPC state (NPC state leaves a static player model for 5 minutes if the player quits the game).
- Weapon used (pistols, assault rifles, shotguns, melee, sniper, etc.)
- Player tier (tier 0, 1, 2, or 3): The tier's significance resides in determining whether players have access to a special weapon (Sniper) which has a big effect on gameplay, and therefore on the statistics. There are only 2 tier 0s and 4 tier 1s.
- Death fees: Upon death, players pay a death fee according to their tier and type of death (suicides and NPC deaths result in double the money lost)
- Player location-based interactions (proximity to key locations)
- Time variables (hour, day, week, month) extracted from a date-time format
- Formatting and plotting the coordinates on top of a map of the game world

I also implemented tier-based filtering to classify player actions according to their levels, allowing deeper analysis of patterns in player behavior across different groups.

**Data Analysis**

Several metrics were computed from the cleaned data, including:

- Frequency Analysis: Daily kill, death, and suicide rates
- Spatial Analysis: Interaction heat maps overlaid onto grids, calculating the kill-to-death ratio (KDR) and economic impact (deaths resulting in penalties)
- Temporal Trends: Identifying peak periods of activity, weapon usage patterns across time, and shifts in behavior
- Player Classification: Segmentation of high-skill players using clustering algorithms based on performance data (mainly kill-death ratio)

**Visualizations**

Using R's ggplot2 library, I developed several visualizations:

- Heat and Scatter Maps: Generated spatial maps of player interactions (kills, deaths, suicides, NPC deaths, etc.), highlighting high-activity zones and the financial impact of deaths per zone, this was done by splitting the map into 500x500 pixel grids and calculating KDSN (kills, deaths, suicides, NPC deaths) statistics and money lost.
- Altitude Map: Constructed an altitude map and used it to analyze player interactions across different elevation levels 
- Trend Analysis: Temporal patterns in activity, showing spikes in interactions and changes in behavior over time. For example, this was used to study the changes in the total death fee difference between the 2 factions over time (in real numbers and percentages).

**Outcomes and Insights**

Through this project, I gained extensive experience transforming unstructured data into a structured format suitable for advanced analysis. This project allowed me to hone my skills in:

- Cleaning and transforming large, unstructured datasets
- Performing complex frequency and spatial analysis
- Utilizing visualization tools for clear communication of insights
