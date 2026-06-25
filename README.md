# CS175 Project
## Demo Code
To run the demo, first run `pip install -r requirements.txt` in a new environment.  
Then run all the cells in project.ipynb in order. Be sure to run each cell only **once**!
## File Descriptions
**src/pretrained_models/**:
This directory contains the pretrained models for all clusters.  
**src/sentiment_stock_data/**:
This directory contains the preprocessed data of the stocks and their average sentiment.  
**src/stock_data/**:
This directory contains the raw (unprocessed) data of the stocks.  
**src/DTB3.csv**:
This csv file contains the raw data of the risk-free rate.  
**src/risk_free_rates.csv**:
This csv file contains the risk-free rate used in the Sharpe ratio.  
**src/stock_clustering.ipynb**:
This file clusters the stocks based on their price trajectories.  
**src/stock_and_tweet_preprocessing.ipynb**:
This file preprocesses the stock data, sentiment data, and the risk-free rate data.  
**src/StockTrader.ipynb**:
This file contains the custom Gym environment, and also trains and evaluates the models.  
**project.ipynb**:
This file contains a demo of the trained models running on test data.  
**project.html**:
This html file is a version of project.ipynb in html format.  
**requirements.txt**:
This file lists required modules to run project.ipynb.  
