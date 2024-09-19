+++
title = "Time Series Forecasting of Housing Prices" 
description = "Python, Pandas, NumPy, Scikit-Learn, OpenCV. using publicly available data from zillow and the federal government, i created predictions on what the price would be in the next quarter."
weight = 1

[extra]
# you can also crop the image in the url by adjusting w=/h=
remote_image = "https://images.unsplash.com/photo-1523821741446-edb2b68bb7a0?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80"
+++


painpoints of being my first model. not knowing the difference between tabular vs time-series data. for a long time i was cross validating the model just as i would for tabular data, with k-fold sliding window. however, the temporal nature and order of the data is imperative and must be maintained for all train test splits. so i used expanding window k-fold.

__updated__: 09/19/2024

__todo__: finish explanation, provide metric images