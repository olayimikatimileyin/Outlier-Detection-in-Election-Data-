Outlier Detection in Election Data Using Geospatial Analysis

Case Study: Ensuring Election Integrity

In the recent election, the Independent National Electoral Commission (INEC) encountered numerous legal challenges related to the integrity and accuracy of the results. Allegations of vote manipulation and irregularities have been prevalent, necessitating a rigorous investigation into these claims.

Objective

My task was to aid in uncovering potential voting irregularities and ensuring the transparency of the election results. This was achieved by identifying outlier polling units where the voting results significantly deviate from those of neighboring units. Such deviations may indicate potential influences or manipulations in the voting process.

Approach

Data Preparation: Clean and preprocess the election dataset, converting necessary columns and handling duplicate entries.

Geospatial Analysis: Use geospatial techniques to examine voting patterns and detect anomalies in polling units.

Outlier Detection: Apply statistical methods to identify outlier polling units based on the deviation of voting results from neighboring units.

Visualization: Highlight and analyze significant outliers to ensure transparency and address potential irregularities.

Methodology

Stage 1: Data Preparation

I used Geocode by Awesome Table on Google Sheets to obtain the Longitude and Latitude of the polling units. This geospatial data is crucial for analyzing the geographic distribution of polling units and identifying potential anomalies in the voting results.

Stage 2: Neighbor Identification

I loaded my CSV file into Python (Jupyter Notebook) and utilized the geodesic method to identify neighboring polling units based on geographical proximity. This step involved grouping neighboring polling units into lists represented by their PU-Codes, providing a structured way to analyze proximity-based relationships.

Stage 3: Outlier Detection

I employed the Interquartile Range (IQR) proximity rule to identify outliers for each polling unit by comparing it with its neighboring units. This statistical method helped in pinpointing polling units where the voting results deviated significantly from the norm, highlighting potential anomalies in the data.

Stage 4: Analysis and Visualization

I sorted the data to identify the top five polling units with the most significant outliers for each party. A scatter plot was used to visualize these outliers, providing a clear representation of the most anomalous results. The output from this analysis highlighted the following significant outliers:

No	APC	LP	PDP	NNPP
1	562	521	392	60
2	518	508	272	54
3	500	499	243	44
4	482	490	239	31
5	453	460	224	28

Stage 5: Highlighting Top Outliers

For my top three outliers and their polling units from the different parties, the outliers are identified based on their deviation from the norm, either as exceptionally high or low values compared to neighboring polling units:

APC (All Progressives Congress)

PU-Code: 32-01-07-003, Outlier Value: 562.0

Reason: This polling unit’s vote count of 562 is significantly higher compared to its closest polling units. The discrepancy from neighboring polling units suggests this unit might have experienced an unusual voting pattern or error, making it a candidate for further investigation.
PU-Code: 32-06-11-020, Outlier Value: 518.0

Reason: With 518 votes, this polling unit stands out because the vote count is unusually high compared to its neighbors. This significant deviation raises questions about the accuracy of the reported votes or possible anomalies.
PU-Code: 32-21-10-007, Outlier Value: 500.0

Reason: This polling unit’s vote count of 500 is considerably higher than the majority of surrounding units. The high vote count in the context of nearby units suggests it may be an outlier, potentially due to reporting errors or discrepancies.
LP (Labour Party)

PU-Code: 32-15-15-023, Outlier Value: 521.0

Reason: This unit’s 521 votes are notably high relative to nearby units. Such a deviation could indicate reporting errors, unusual voter turnout, or other anomalies.
PU-Code: 32-15-02-001, Outlier Value: 508.0

Reason: A vote count of 508 is unusually high when compared to surrounding polling units. This significant difference might be due to errors in data entry or an irregular voting pattern.
PU-Code: 32-11-03-008, Outlier Value: 499.0

Reason: With 499 votes, this polling unit’s count is abnormally high compared to its neighbors. This could suggest a reporting error or an unusual increase in votes.
PDP (People’s Democratic Party)

PU-Code: 32-05-07-003, Outlier Value: 392.0

Reason: This unit’s vote count of 392 is unusually high compared to the surrounding units. Such a high count may indicate data entry issues or an irregular voting pattern.
PU-Code: 32-04-08-005, Outlier Value: 272.0

Reason: A vote count of 272 is quite high in comparison to neighboring units. This significant difference can suggest potential errors in data reporting or an abnormal voting trend.
PU-Code: 32-15-06-025, Outlier Value: 243.0

Reason: The 243 votes in this unit are notably higher than the vote counts in surrounding units, indicating possible data anomalies or unusual voting behavior.
NNPP (New Nigeria Peoples Party)

PU-Code: 32-21-10-007, Outlier Value: 60.0

Reason: With only 60 votes, this unit’s count is significantly lower compared to its nearby units. Such a low value could indicate missing data, reporting errors, or unusual voter turnout.
PU-Code: 32-03-12-007, Outlier Value: 54.0

Reason: This polling unit’s count of 54 is unusually low compared to surrounding units, which could suggest data reporting issues or an unusual pattern of voter turnout.
PU-Code: 32-03-07-005, Outlier Value: 44.0

Reason: A vote count of 44 is significantly lower than nearby polling units. This low count might indicate potential issues with data accuracy or unusual voting patterns.

Conclusion

This analysis provides a systematic approach to identifying potential voting irregularities by leveraging geospatial data and statistical methods. By pinpointing outlier polling units, it highlights areas where further investigation is warranted to ensure the integrity and accuracy of election results. This approach not only aids in uncovering potential anomalies but also enhances transparency in the electoral process.
