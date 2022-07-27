# stock_market_predictions
Purpose of this project:
========================
This is an attempt to predict stock prices based on the shares of the Johannesburg Stock Exchange.
My development environment is Python through Jupyter Notebook on Windows.

My dependent variable is a 'trend' calculated from the returns between day and day-1.
I tested only 1 algorithm 'Decision tree'.
For more details see this document : (to follow)

Structure of files :
====================
Root :
	Stock_market_predictions.ipynb
Input
	get_historical_stock_data_JSE.csv
	get_stock_data_JSE.csv
	Market_data_inflation
		csv
			Growth Rate Previous Period Monthly South_Africa.csv
	Market_data_volatility
		EPU
			csv
				EPU_index_Global.csv
		VIX
			csv
				CBOE Crude Oil ETF Volatility Index.csv
				CBOE Emerging Markets ETF Volatility Index.csv
				CBOE Energy Sector ETF Volatility Index.csv
				CBOE Equity VIX on Amazon.csv
				CBOE Equity VIX on Apple.csv
				CBOE Equity VIX on Google.csv
				CBOE Equity VIX on IBM.csv
				CBOE Gold ETF Volatility Index.csv
				CBOE Gold Miners ETF Volatility Index.csv
				CBOE Silver ETF Volatility Index.csv
				CBOE Volatility Index VIX.csv
	Markets
		markets_JSE.csv
	Tickers_by_market
		JSE.csv

Output
	Tickers_completed
	Tickers_norm_cleanuped_skewed
	Tickers_not_skewed
	Tickers_splitted
	Tickers_standardized
	Tickers_std_cleanuped_skewed
	Tickers_with_MACD
		JSE
	Tickers_wo_outliers

Parameters :
============
Inside Stock_market_predictions.ipynb
set the parameters (verbose level, part of the program to execute):
# Init market set
markets_set = pd.read_csv('Input\\Markets\markets_JSE.csv', encoding='latin1', sep = ';')
# Init variables
KDD2 = 'X' # 2nd Step of KDD process : Creating a target data set
KDD3 = 'X' # 3rd Step of KDD process : Data cleaning and preprocessing
KDD4 = 'X' # 4th step of KDD process : Data reduction and projection
horizon = 14 # horizon of predictions
V = 1 # Verbose mode of logs : 3 very detailed, 2 detailed, 1 synthetic
KDD6 = 'X' # 6th step of KDD process : "exploratory analysis and model and hypothesis selection"
KDD6_3 = 'X' # Decision tree

Execution :
===========
Just run the program Stock_market_predictions.ipynb
It will output the accuracy at the end.
