# Cricketer-Retirement-Prediction
## Introduction
Cricket is a sport where individual performances of players can impact the outcome of a match. This research paper proposes an LSTM-based approach for predicting the retirement age of test batters in cricket. The aim is to build a model that can accurately predict the retirement age of a player using their historical performance data. The proposed model can assist cricket teams in selecting and managing players more effectively, as well as aid cricket analysts in understanding the factors that influence the retirement age of test batters.
## Long Short-Term memory model
LSTM (Long Short-Term Memory) is a type of recurrent neural network (RNN) architecture that is designed to address the vanishing gradient problem, which can occur when training traditional RNNs. In an LSTM network, the model can selectively remember or forget information over time, making it particularly useful for processing sequential data such as natural language text, speech, or time series data.
<br>
The architecture of an LSTM network includes a series of memory blocks that interact with each other, with each block containing several "gates" that regulate the flow of information. These gates are responsible for selectively adding or removing information from the memory block, based on whether it is deemed relevant or not.
<br>
LSTMs have been successfully applied in a wide range of tasks, such as language modeling, speech recognition, and time series forecasting, among others.
## Methodology
### The proposed approach for prediction consists of two LSTM models:
* To predict the total number of innings a player will play in their career.
* To predict the retirement age with the help of data predicted by the first model.
## Data Analysis
### Data Collection
* We collected the data for this study from a publicly available source on the [HowSTAT](http://www.howstat.com/cricket/home.asp) website which includes cricket archives and statistical databases.
* The dataset consists of a total of 100 retired test batters and 10 active batters, with each player having different number of innings.
* The batting statistics for each innings include runs scored, balls faced, cumulative runs and other relevant metrics.
### Data Preprocessing
It involves the following stages:
1. Discretization: Fetching the data relevant for the research.
2. Normalization: Normalizing the values of the attributes on the same scale to make the assessment easier.
3. Cleaning: Filling the missing values in the data to avoid any discrepancy.
4. Integration: Integration of data files.
<br>
After the transformation the dataset is divided into training and testing dataset. Testing data is kept only 25% of the training data.
</br>

### Feature Extraction
The final Features given to the first model are: <br>
1. Current Age (in years)<br>
2. Debut Age (in years)<br>
3. Innings Played till date<br>
4. Cumulative runs scored<br>
5. Number of fifties scored<br>
6. Number of innings in last 3 years<br>

The final features given to the second model are:<br>
1. Debut Age (in years)<br>
2. Total innings predicted from model 1<br>
3. Cumulative runs scored<br>
4. Number of fifties scored<br>
