# SCT_DS_4
Analyse traffic accident data to idntity patterns related to road conditions,weather, and time of day.Visualize accident hotspots and contributing factors.
# ------------------------------------------------------------
# PROJECT: TRAFFIC ACCIDENT DATA ANALYSIS
# GOAL: IDENTIFY PATTERNS BASED ON ROAD CONDITIONS, WEATHER, AND TIME OF DAY
#        AND VISUALIZE ACCIDENT HOTSPOTS & CONTRIBUTING FACTORS
# ------------------------------------------------------------

# 1. Import Required Libraries
#    - pandas & numpy: for data loading and manipulation
#    - matplotlib & seaborn: for visualizations
#    - folium or plotly: for geographic hotspot mapping
# ------------------------------------------------------------

# 2. Load the Dataset
#    - Read the accident dataset (CSV or Excel file) into a pandas DataFrame
#    - Example: df = pd.read_csv("traffic_accidents.csv")
#    - Display first few rows using df.head()
#    - Check basic info and structure with df.info()

# 3. Inspect the Data
#    - Identify key columns such as:
#         * Date/Time of accident
#         * Weather condition
#         * Road condition
#         * Location (Latitude, Longitude)
#         * Severity of accident
#    - Use df.describe() for numeric summary
#    - Use df['column'].unique() to check unique categories

# 4. Data Cleaning
#    - Handle missing or inconsistent data:
#         * Fill missing values with mode/median where appropriate
#         * Drop rows with critical missing values (like location or time)
#    - Convert date/time column to datetime format using pd.to_datetime()
#    - Extract useful time features:
#         * Hour, Day, Month, and Weekday from datetime column
#    - Remove duplicates and invalid entries if any

# 5. Feature Engineering
#    - Create new columns for analysis:
#         * “Time_of_Day” (Morning, Afternoon, Evening, Night) based on hour
#         * “Weather_Category” (Clear, Rain, Snow, Fog, etc.)
#         * “Road_Status” (Dry, Wet, Icy, etc.)
#    - Helps in grouping and visualization

# 6. Exploratory Data Analysis (EDA)
# ------------------------------------------------------------
# 6.1 Univariate Analysis
#     - Analyze individual factors using:
#         * Count plots of weather, road condition, and accident severity
#         * Distribution of accidents across time of day
# ------------------------------------------------------------
# 6.2 Bivariate Analysis
#     - Study relationships between two factors:
#         * Weather vs Accident Severity
#         * Road Condition vs Accident Count
#         * Time of Day vs Accident Frequency
# ------------------------------------------------------------
# 6.3 Multivariate Analysis
#     - Combine multiple factors:
#         * Weather + Road Condition + Severity
#         * Use grouped bar charts or heatmaps for better understanding

# 7. Visualization of Patterns and Trends
# ------------------------------------------------------------
# 7.1 Time-based Analysis
#     - Plot number of accidents by hour, day, and month
#     - Identify peak accident hours and dangerous times of day
# ------------------------------------------------------------
# 7.2 Weather and Road Condition Analysis
#     - Create bar plots or stacked plots to compare accident severity under different weather types
#     - Use seaborn countplot and boxplot to visualize distributions
# ------------------------------------------------------------
# 7.3 Severity Distribution
#     - Use pie charts or bar graphs to show proportions of accident severity levels (e.g., minor, major, fatal)

# 8. Hotspot Visualization (Geospatial Analysis)
# ------------------------------------------------------------
#     - Use folium or plotly to map accident locations using Latitude and Longitude
#     - Create a heatmap layer to visualize accident hotspots
#     - Example:
#         import folium
#         from folium.plugins import HeatMap
#         map = folium.Map(location=[mean_lat, mean_lon], zoom_start=10)
#         HeatMap(df[['Latitude', 'Longitude']].dropna(), radius=8).add_to(map)
#         map.save("accident_hotspots.html")
#     - This helps identify high-risk areas or intersections

# 9. Identify Contributing Factors
# ------------------------------------------------------------
#     - Analyze which factors contribute most to accidents:
#         * Poor weather (rain, fog)
#         * Poor road conditions (wet, icy)
#         * Night-time driving or rush hours
#     - Use correlation analysis or feature importance (if building predictive models)

# 10. Insights and Interpretation
# ------------------------------------------------------------
#     - Identify the most dangerous weather conditions and time periods
#     - Determine which road conditions cause severe accidents
#     - Detect geographic areas with high accident frequency
#     - Provide possible recommendations (e.g., better lighting, warning signs, traffic control)

# 11. Visualization Summary
# ------------------------------------------------------------
#     - Bar charts → Compare categorical factors (weather, road)
#     - Line plots → Show trends over time (hours/days)
#     - Heatmaps → Display geographic accident hotspots
#     - Correlation plot → Show relationships among numerical features

# 12. Summary of Findings
# ------------------------------------------------------------
#     - Accidents more frequent during specific hours (e.g., rush hour)
#     - Wet or icy roads contribute to higher accident severity
#     - Rain and fog increase the risk significantly
#     - Certain intersections or road segments act as consistent hotspots

# 13. Conclusion and Recommendations
# ------------------------------------------------------------
#     - Use insights to suggest safety improvements:
#         * Install warning signs or lights at hotspot areas
#         * Increase patrol presence during peak accident hours
#         * Improve drainage systems to reduce wet/icy roads
#         * Enhance driver awareness programs about risky conditions

# ------------------------------------------------------------
# END OF TRAFFIC ACCIDENT ANALYSIS PROJECT
# ------------------------------------------------------------
