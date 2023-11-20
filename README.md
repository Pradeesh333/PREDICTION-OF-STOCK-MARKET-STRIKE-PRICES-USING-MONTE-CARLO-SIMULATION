# PREDICTION-OF-STOCK-MARKET-STRIKE-PRICES-USING-MONTE-CARLO-SIMULATION

## MINI PROJECT DONE BY PRADEESH S 212221240038
# ABSTRACT
The stock market is a dynamic and complex system that has intrigued investors, traders, and analysts for generations. While it's impossible to predict the market's every move with absolute certainty, there are statistical and computational techniques that can provide valuable insights and assist us in making more informed investment decisions. This project shows how the Monte Carlo method, a powerful computational technique, can be harnessed to model the uncertainties and complexities inherent in the stock market. The main objective of this project is to learn the mathematics behind Monte Carlo and the uncertainty in the stock market. And implement the simulation in real-world datasets and predict the trend. The purpose of this project is to leverage Monte Carlo simulations as a powerful computational tool to provide investors, traders, and financial institutions with a reliable and data-driven framework for stock market prediction, portfolio optimization, risk assessment, and volatility forecasting. By doing so, the project aims to enable users to make more informed investment decisions, manage risks effectively, and build well-balanced portfolios in the face of the inherent complexities and uncertainties of the stock market.\

# PROBLEM STATEMENT
The challenge of accurately predicting stock market strike prices poses a significant hurdle for investors seeking to optimize their option trading strategies and manage risk effectively. Traditional financial models often fall short in capturing the complexities and uncertainties inherent in market dynamics, making it imperative to explore alternative methods for strike price forecasting.
The primary problem addressed in this study is to develop a robust and reliable predictive model for stock market strike prices, utilizing the Monte Carlo simulation technique. The traditional models often assume static market conditions and overlook the dynamic nature of financial markets, resulting in less accurate predictions. Monte Carlo simulation, with its ability to incorporate randomness and simulate a multitude of potential future scenarios, offers a promising solution to enhance the precision of strike price forecasts.
Key aspects of the problem include 
Market Dynamics: The stock market is influenced by a myriad of factors, including economic indicators, geopolitical events, and market sentiment. Developing a model that accounts for the dynamic and interconnected nature of these variables is essential for accurate strike price prediction.
Uncertainties and Non-Linearity: Financial markets are inherently uncertain, and price movements often exhibit non-linear behavior. Constructing a predictive model that effectively incorporates uncertainties and non-linearities is crucial for generating reliable strike price forecasts.
Simulation Accuracy: The Monte Carlo simulation method relies on the generation of random samples to simulate possible future scenarios. Ensuring the accuracy and representativeness of these simulations is a key challenge in developing a dependable predictive model.

# CHALLENGES FACED BY STOCK MARKET PREDICTION
Predicting a value in a time series is almost impossible since simple mathematical models cannot replicate the real world. The main problem is the irregularity in the time series data. The trend, seasonality, and cyclic components can be analyzed using exploratory data analysis in Python. Stock prices often exhibit non-linear behavior, making it challenging to model and predict their movements accurately. Traditional linear models may not capture the complexity and nuances of market dynamics.
	Random Walk Theory:
“The random walk hypothesis suggests that stock prices follow a random path, making it difficult to predict future movements based on historical data alone. This theory challenges the effectiveness of using past price patterns to forecast future prices.”

Since regular time series forecasting models won't replicate the real world, The predictions can be based on random values. Hence adopting the Monte Carlo Simulation for better understanding and prediction. MCS is a powerful technique used to simulate the real world, The method generates N number of random numbers which helps in analyzing the randomness in stock price movement. This method provides a narrow range of predicted values. This helps in making a mature guess in investing. Even though MCS simulates with randomness the real world is still unpredictable.  Geopolitical events, natural disasters, and other external factors can have a significant impact on financial markets. These events are often unpredictable and can lead to sudden and dramatic market movements.
# SCOPE OF PROJECT
This project focuses on the implementation of the MCS and ARIMA models to predict the probability of the given strike price. And also focuses on the study of real-world time series analysis and forecasting techniques. The scope of this project encompasses the following domains:
ADFuller test: Finds the stationarity of the time series for analysis and choosing better forecasting methods. The p-value should be less than 0.05 for the time series to be stationary.
AutoCorrelation: Returns the factor at which the previous values affect the current value. The perfect number of lags is considered.
Auto Regression Moving Average: Implemented ARIMA for forecasting the stock price which is done by autoArima function. The “p” and “q” values are calculated iteratively for the optimal solution.
Monte Carlo Simulation: Generating random numbers to find the optimal upper and lower boundary for the predicted price.
Performance Evaluation: The RMSE is calculated for evaluation. The probability is found and compared with the real-world data.
Future Scope: Identification of potential areas for system improvement and extension. Consideration of scalability for deployment in different domains and applications.

# PROJECT WORKFLOW
Data Collection
	The initial step in this project is to import the time series data of a stock. In this project “Google stocks” are imported using the yfinance library. This dataset consists of the date and the closing stock price for the past 10 years.
Pre-processing
Preprocessing is a crucial step in preparing raw data for analysis or modeling. It involves cleaning and transforming the data to make it suitable for further processing. One common method of data preprocessing is dealing with missing values by imputing them with appropriate values or removing instances with incomplete information. Scaling and normalization are also important steps to ensure that numerical features are on a similar scale, preventing certain features from dominating others.
In this prediction model, the differencing method is used to normalize the data and convert the non-stationary data to stationary data.
Data Analysis
	The time series data is analyzed using multiple functions such as adfuller test and partial auto-correlation. This tells about the stationarity of the time series and the number of lags used to predict the value. 
Data splitting
Split the data into training and testing data, the testing data is again split into two parts - test data and residual distribution data. The residual distribution data is used in fitting the model and running the simulation.
Training the model
	The training data is fit in an ARIMA model which forecasts the next value. After multiple iterations, an array of predicted values is saved. Then the residual error is calculated for further process.
Monte Carlo Simulation
Generate N number of random numbers such that the values are within the limits. The limits are calculated by addition and subtraction of residual error with actual value. Take the max and min generated random number as the range.
Probability 
	Calculate the probability of the actual value falling under the calculated range and assign a strike price of the future value, the model returns the probability of the strike price in the forecasted range.

# CONCLUSION
In conclusion, the project on "Prediction of Stock Market Strike Prices using Monte Carlo Simulation" has explored a dynamic and probabilistic approach to forecasting stock market strike prices. Through the implementation of Monte Carlo simulation, the study has provided insights into the potential range of future stock prices, considering the inherent uncertainties in financial markets. While Monte Carlo simulation offers a powerful tool for capturing the complexity of stock price movements, it is essential to acknowledge its limitations and the need for continuous refinement in the model. This project contributes to the broader understanding of predictive modeling in financial domains, emphasizing the significance of probabilistic approaches in decision-making processes related to stock market investments. Further research and refinement of the Monte Carlo simulation methodology may enhance its applicability and accuracy in predicting stock market strike prices.

# REFERENCES
```
[1] Kroese, D. P., Brereton, T., Taimre, T., & Botev, Z. I. (2014). Why the monte carlo method is so important today. WIREs Computational Statistics, 6(6), 386-392.
[2] M. Hariadi, A. A. Muhammad and S. M. S. Nugroho, "Prediction of Stock Prices Using Markov Chain Monte Carlo," 2020 International Conference on Computer Engineering, Network, and Intelligent Multimedia (CENIM), Surabaya, Indonesia, 2020, pp. 385-390, doi: 10.1109/CENIM51130.2020.9297965.
[3] A. Sharma, D. Bhuriya and U. Singh, "Survey of stock market prediction using machine learning approach," 2017 International conference of Electronics, Communication and Aerospace Technology (ICECA), Coimbatore, India, 2017, pp. 506-509, doi: 10.1109/ICECA.2017.8212715.
[4] L. Ismail, S. Alhmoudi and S. Alkatheri, "Time Series Forecasting of COVID-19 Infections in United Arab Emirates using ARIMA," 2020 International Conference on Computational Science and Computational Intelligence (CSCI), Las Vegas, NV, USA, 2020, pp. 801-806, doi: 10.1109/CSCI51800.2020.00150.
[5] A. A. Ariyo, A. O. Adewumi and C. K. Ayo, "Stock Price Prediction Using the ARIMA Model," 2014 UKSim-AMSS 16th International Conference on Computer Modelling and Simulation, Cambridge, UK, 2014, pp. 106-112, doi: 10.1109/UKSim.2014.67.
[6] M. M. R. Majumder and M. I. Hossain, "Limitation of ARIMA in extremely collapsed market: A proposed method," 2019 International Conference on Electrical, Computer and Communication Engineering (ECCE), Cox'sBazar, Bangladesh, 2019, pp. 1-5, doi: 10.1109/ECACE.2019.8679216.
[7] P. Li, Y. Zhang and Q. Zhang, "Monte Carlo Location Algorithm Based on Model Prediction," 2018 International Symposium in Sensing and Instrumentation in IoT Era (ISSI), Shanghai, China, 2018, pp. 1-5, doi: 10.1109/ISSI.2018.8538228.
[8] P. S. Dewi, J. K. Widyanto and A. Tick, "Monte Carlo Simulation of Stock Movements – an Indonesian Case," 2021 IEEE 19th International Symposium on Intelligent Systems and Informatics (SISY), Subotica, Serbia, 2021, pp. 101-106, doi: 10.1109/SISY52375.2021.9582547.```
