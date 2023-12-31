# 🚀  Welcome to Godi.AI's Predictive 5-Year Analysis with XGBoost (the best model previously identified for this project).

Hello, business innovator! 🌎 I'm [Santiago PATINO SERNA](https://www.linkedin.com/in/santiago-patino/), the CEO and data scientist at [Godi.AI](https://godi.ai/). This notebook showcases the deployment of the Xgboost model, identified as the optimal choice for this dataset in a previous notebook. There, various models were tested and the best one selected, along with its hyperparameters. [Notebook for model selection on Github](https://github.com/santiagopatinoserna/TensorFlow_Prediction_5YearFrench_IFI/blob/main/Script/Model_selection_ML_NN.ipynb). In this notebook, we will read and clean the data using the previously developed code. Following this, the model will be trained using the Xgboost algorithm and the best hyperparameters identified earlier. The focus will be on deploying the model for production, which involves training the model with the entire dataset. Additionally, we'll construct a dataframe containing data to predict unknown values. This process will include a loop where each iteration uses the latest prediction to forecast the next value.

## 📊 Notebook Overview 
[Notebook on Github](https://github.com/santiagopatinoserna/Prediction_5Years_IFITAX/blob/main/Script/Prediction_5year_IFI_TA.ipynb)  

### Deployment of the IFI Tax Model for Predicting 5-Year Trends in French Cities

- **Data Loading/Cleaning/Feature Engineering Construction**: The code for this process is replicated here from the previously mentioned project. This stage involved developing the base for our predictive analysis.
- **Construction of the Prediction DataFrame**: We create the X variables from past data to predict the unknown Y values, focusing on how historical trends can inform future outcomes.
- **Training the Algorithm with All Data**: The model training utilized 100% of the known data, following prior validations. Outlier city data, which could skew the model, were excluded to ensure accuracy.
-**Prediction for Year+1**: We employ the trained model to predict the first year, initiating our forward-looking analysis.
-**Prediction Loop**: A loop for predicting X years is initiated, using the previously predicted value as the X variable for the next year's prediction. This iterative process builds upon each successive prediction.
-**Visualization of Predictions**: Graphical representations of the predictions are created, providing a visual understanding of the projected IFI tax trends in French cities.
-**Outlier Prediction**: Since outliers were excluded from the main model, a rapid auxiliary model, Prophet, is used specifically for these cities. This approach strictly follows their historical trends to forecast their future IFI tax values.

## 📸 Key Visual Insights
![Comparative analisys of anual groth rate](https://drive.google.com/uc?export=view&id=1Q9LoDcBf3y0L6Sd-E-thehrBdz8ZLZ69)  
*Based on the five-year predictions starting from 2023, what is the annual growth rate of the IFI tax across all cities in France?*

![Where to invest in France based on the annual growth of the IFI tax?](https://drive.google.com/uc?export=view&id=1QDWiHDt0677bMQwyboFA8cx38t_-cOoJ)  
*A dynamic chart that provides a quick overview of which cities in France are favorable or unfavorable for investment, based on the IFI tax growth rate from 2023 over a period of 5 years.*

![Actual vs Predicted for 10 random cities](https://drive.google.com/uc?export=view&id=1Q7F7M3UKmtSztHyQdI22JaUCCCAuJ2m9)  
*Analysis of the Continuity of IFI Tax Prediction in Ten Randomly Selected Cities.*

![Yearly Growth rate per city (TOP 5 cities)](https://drive.google.com/uc?export=view&id=1QG5kQcS6l4f9lL3H6tmGiAaxiAfPRKoQ)  
*Detailed Analysis of the Top Cities and Their Growth*

![Graphic Analysis of the Top and Flop Cities Based on Their Growth Rate](https://drive.google.com/uc?export=view&id=1QOUo40Jnefq9innVrkNThmp3Qm7iJOq7)
*Visualization Available by Canton, Where Only the Concerned Cities are Highlighted with Color*

![Global Map of France Showing the Top and Flop Cities](https://drive.google.com/uc?export=view&id=1QGArpq8fYlVokxHVKhN7QxLrcNGQ4CzQ)
*This map graphically represents points at the midpoint of the coordinates of each region.*

---

## 🤖 About Godi.AI

Godi.AI is the startup reshaping how businesses experience AI. We focus on speed, ROI, and guiding businesses on their digitalization journey. Dive into our standout apps, or explore tailored solutions with our Godi.AI Freelancer method.

**Special Note:** For businesses seeking an even more customized experience, reach out to me directly. As a proud Polytechnique Paris graduate, I am here to turn your data into insightful, actionable decisions.

📩 **Get Started:** Ready to embark on this transformative journey with Godi.AI? [Reach out to us!](https://godi.ai/freelancing/)

📔 **Explore the Notebook:** For a detailed dive, explore the [Notebook in Github](https://github.com/santiagopatinoserna/Prediction_5Years_IFITAX/blob/main/Script/Prediction_5year_IFI_TA.ipynb) on GitHub.
