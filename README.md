## Introduction
The [dataset](https://www.kaggle.com/datasets/robikscube/hourly-energy-consumption/data) I am using explores twenty years of hourly electricity consumption data (1998–2018) from the PJM Interconnection grid. 

## Data Mining Techniques 
Classification (Decision Trees): Used for rule extraction to define the logical combinations of regional variance that characterize grid anomalies. 

Dimensionality Reduction (PCA): Applied to isolate latent residuals by filtering out dominant diurnal and seasonal cycles. 

Clustering (K-Means/DBSCAN): Used to group regional signatures and detect behavioral shifts over time.

## Discovery Question #1
```
What are the specific characteristics of anomalous hours where energy demand significantly deviates from the historical seasonal norm, and do these anomalies occur simultaneously across regions?
```

The first step was realizing that traditional outlier detection in IQR would not work as intended. Since the data is primarily composed of sinusoidal functions, it was optimal to use 'seasonal_decompose' to properly identify true outlier data.

Once each company's outlier data was recognized, I built a correlation matrix between all companies, intending to properly map which companies had simultaneous days or hours of anomalous readings.

I continued further, creating a dictionary with simultaneous anomalies, and mapped the 24 hour periods (+/- 12 hours) to identify specific characteristics that could explain the readings.

## Discovery Question #2
```
After using PCA to remove the dominant seasonal noise, what latent operational signatures remain, and do these clusters represent shifts in industrial vs. residential behavior over the decade?
```

The next phase of the implementation focused on isolating latent operational signatures by applying Principal Component Analysis (PCA). By targeting the components that captured 95% of the dataset's variance, I was able to effectively strip away dominant seasonal noise and highlight the underlying behavioral traits of the load profiles.

With the reduced feature set, I implemented K-Means clustering to categorize these signatures into five distinct archetypes. This transformed the raw megawatt readings into a taxonomy of grid behavior, allowing for the classification of each day based on its specific consumption signature, such as those dominated by industrial or residential demand.

Finally, I analyzed the long-term evolution of these signatures by calculating the annual proportion of specific clusters across the two-decade span. By applying a linear regression trend line to the "Industrial Signature," I was able to quantify a structural shift in the grid's operational identity, providing empirical proof of how consumption patterns have transitioned over time.