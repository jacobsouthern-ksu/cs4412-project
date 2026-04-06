# cs4412-project
M1:
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

M3:
Discovery Question 1:
What are the specific characteristics of anomalous
hours where energy demand significantly deviates
from the historical seasonal norm, and do these
anomalies occur simultaneously across regions?

Discovery Question 2:
After using PCA to remove the dominant sea-
sonal noise, what latent operational signatures
remain, and do these clusters represent shifts in
industrial vs. residential behavior over the decade?

I have split the github into two notebooks. One includes the preprocessing and initial visualization + implementation of discovery question 1. The other notebook contains the implementation of discovery question 2.

Not exactly the cleanest code, but at the very least it will run.
