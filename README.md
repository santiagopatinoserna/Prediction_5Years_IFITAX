# French IFI tax: recursive projection experiment

An exploratory notebook that extends municipal IFI tax histories using XGBoost and a separate Prophet treatment for selected outlier cities.

## What is implemented

[Projection notebook](Script/Prediction_5year_IFI_TA.ipynb):

- Load and clean the bundled tax and commune data.
- Reuse the modelling approach from [the companion model-comparison project](https://github.com/santiagopatinoserna/TensorFlow_Prediction_5YearFrench_IFI).
- Fit XGBoost and feed predicted values back into subsequent forecast steps.
- Export projection tables, growth-rate summaries and inputs for maps and Power BI.

## What the results do not establish

This is a scenario-generation exercise, not an investment recommendation or a deployed forecasting service. Recursive forecasts compound prediction errors. The companion model comparison uses a random split rather than chronological backtesting and fits scaling before splitting. Its reported scores do not validate the multi-year projections here.

A follow-up needs rolling-origin backtests, naive baselines, prediction intervals and explicit treatment of changing tax rules and commune coverage. Training on all available observations is not itself a production deployment.

## Reproduction notes

The notebook uses Google Colab, a Drive mount and absolute paths. Update its input/output paths and adapt the Colab mounting cell for local execution. Dependencies imported in the notebook include pandas, NumPy, scikit-learn, XGBoost, Prophet, matplotlib, seaborn, GeoPandas, Folium and Branca. Compatible Excel readers are also required. There is no locked original environment or verified one-command reproduction.

## Files to inspect

- `Dataout/PowerBI/df_ificom_generated_data.csv`: saved historical/projected records. Distinguish observed years from generated years before analysing them.
- `Dataout/PowerBI/average_growth_rates.csv`: derived growth summaries.
- `Dataout/PowerBI/PowerBI_tax_IFI.pbix`: historical Power BI artifact. Its compressed binary model and connections have not been fully audited in this review. Do not assume that reading the CSV exports validates the PBIX.

## Project status

Historical exploratory work using the 2019 to 2022 IFI input files kept in `DataIn/`. This is a research notebook, not a deployed service. The notebooks and exported results have not been rerun end to end in the current environment.

## Data and reuse

The tax input files are attributed in the project notebooks to the French public dataset *Impôt de solidarité sur la fortune / Impôt sur la fortune immobilière par collectivité territoriale*. Commune coordinates and lookup tables are included in `DataIn/`. Source files and derived tables retain their applicable upstream terms; this repository does not grant a new licence over those datasets. Check the original publisher and the terms for each input before redistribution.

## Author

Santiago Patiño Serna. [LinkedIn](https://www.linkedin.com/in/santiago-patino/) · [Godi.AI](https://godi.ai).
