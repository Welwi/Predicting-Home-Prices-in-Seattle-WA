# Live Kingly, LLC - a Real Estate Company
-Group members: Alex Benedict, Edna Fernandes, Frank Kornet, Mayank Phanse, and David Walkup
​
# Business Problem
-Maximize profit in the King County real estate market (either via selling, buying, or both [flipping])
​
# Project Goals
-Identify target properties in the King County real estate market that are ideal for flipping (low cost, high return, quick turnaround)
-Perform EDA on provided dataset, highlight any data impurities, clean and transform data for modeling
-Highlight features that are essential in building an appropriate model
-Build model with at least 90% pricing accuracy
-Provide end-user with leading questions identified throughout the data analysis
​
# Project Metrics
-Models were evaluated on TEST data using r-squared and mean squared error values. Model highlighted 23 zip codes in King County that had >90% accuracy and were thusly selected for future analyis and refinement.
​
# Step 1: EDA
-'clean_data.ipynb' includes comments on how EDA was performed. Essentially, exploration noted that there were null values and discrepancies in three key columns: Waterfront property, renovation year, and view. These values were then approximated and replaced by categorical values (explicit notes can be found in file). Some datapoints in the far eastern portion of King County are removed due to geographical isolation and known outliers are removed. Cleaned data is reconverted into a CSV file and reuploaded to Github.
​
# Step 2: Modeling
-Two models are built: GAM and MARS. GAM provides more accurate results (gam_model.ipynb), so is our model of choice for this purpose.
​
# Step 3: Refining Models based on Zip Code
-Using the GAM model, we were able to highlight 23 specific zip codes that have higher than the average 90% accuracy for the model. Our assumption is that these zip codes have more complete data, fewer outliers, and more consistent throughput. We keep the zip code GAM model if it is better than the general GAM model over all the zip codes. At the end we remove all the zip codes for which we have a better model from the general GAM model, and then we then train the general GAM model with the zip codes for which we have better models excluded.
​
# Findings and Recommendations
-Current model is stable enough to move to next phase.
-Build a prototype to:
    -Collect daily new published houses
    -Determine which houses are undervalued
-Engage a real estate professional with extensive experience in flipping houses
-Optional: refine Seattle housing data (i.e. whether house is or is not on the waterfront.
​
​
# Next Steps
-Build prototype system for collecting new house prices, determining undervalued houses, validate model output with real estate professional, and clean additional data.
​
# Presentation Link
https://drive.google.com/file/d/1hbO0bsDN3AxZ-cBlaQgkWhX1Pu0GeKR4/view?usp=sharing
