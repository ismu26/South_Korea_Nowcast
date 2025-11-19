# South_Korea_Nowcast
This script implements a GDP nowcasting framework using MIDAS regression in R. It integrates monthly high-frequency indicators with quarterly GDP data, allowing for real-time estimation of economic activity.

Key features:
Imports and preprocesses monthly and quarterly macro indicators from Excel.
Applies log-differencing to generate stationarity-consistent monthly transformations.
Aligns data across mixed frequencies using zoo objects.
Includes shock dummy variables (e.g., GFC, COVID-19) for structural adjustment.
Fits a MIDAS regression with Almon lag polynomials, combining:
Quarterly GDP growth (y_ts)
Shock dummy (dum_ts)
Lagged GDP
Monthly indicators via mls()
Generates in-sample fitted values and visualizes actual vs fitted GDP growth.

The framework replicates EViews-style MIDAS logic, including example implementation of monthly–quarterly data alignment, shock dummy construction, and lag weighting via Almon polynomial structure.

> **Note:** The data file (`data/example_inputs.xlsx`) is not provided.  
Users can replace it with their own dataset following the same structure.
