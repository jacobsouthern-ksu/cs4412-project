# cs4412-project
This project explores twenty years of hourly electricity consumption data (1998–2018) from the PJM Interconnection grid. Moving beyond simple forecasting, the goal is to discover the underlying "DNA" of grid stress and long-term shifts in regional operational signatures.

Source: Hourly Energy Consumption dataset via Kaggle (PJM Interconnection).
Size: Over 178,000 hours of data across multiple US utility regions.
Challenge: Asynchronous start dates across utilities require robust alignment and synchronization during preprocessing.

Characterizing Grid Stress: What are the specific multi-regional rules that define an "anomalous" hour versus a standard seasonal peak? 
Latent Operational Signatures: After filtering seasonal noise, do regional energy signatures show mathematical evidence of shifting from industrial to residential profiles over the 20-year span? 

Data Mining Techniques 
Classification (Decision Trees): Used for rule extraction to define the logical combinations of regional variance that characterize grid anomalies.
Dimensionality Reduction (PCA): Applied to isolate latent residuals by filtering out dominant diurnal and seasonal cycles.
Clustering (K-Means/DBSCAN): Used to group regional signatures and detect behavioral shifts over time.
