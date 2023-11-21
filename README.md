# Predictability of Music Trends in Time

This project aims to analyze the correlation of a singer's songs with important parameters over decades using the Python programming language and the pandas library. The main goal is to understand the development of music taste in society, the predictability of popular music, and the musical features that make a hit.

## Data

The data used in this project is the [Spotify Hit Predictor Dataset (1960-2019)](https://www.kaggle.com/datasets/theoverman/the-spotify-hit-predictor-dataset/data) which includes over 40,000+ tracks labeled hit or flop, with their features such as danceability, energy, key, loudness, mode, speechiness, acousticness, instrumentalness and others.

## Methodology

The methodology for this project involves several steps:

1. **Data Exploration**: The first step involves exploring the data to understand its structure and basic statistics. This includes importing the data, converting the release date to datetime format, cleaning the data by removing all rows with release date before 1960, sorting the dataframe by release date, and visualizing the correlation and histogram pairgrid.

2. **Data Splitting**: The data is then split into training, validation, and test subsets for each timeframe of interest using an 80/10/10 ratio. The data is also scaled to minimize the effect of features that are on scales in different orders of magnitude.

3. **Model Training**: A logistic regression model is trained on the training data and tested on the validation and test data. The model's accuracy is then evaluated on all the available timeframes of interest.

4. **Feature Importance Analysis**: The correlation coefficients for each feature are calculated and visualized as a heatmap. This helps to understand which features have the most positive influence on a song being a hit or not.

5. **Artist Adherence Analysis**: The code also includes a section to analyze whether a popular artist adheres to the trends in the features that have the most positive influence on a song being a hit.

6. **SHAP Value Analysis**: SHAP values are used to investigate the influence of different features on the predictive accuracy of the produced models.

7. **Song Prediction**: Finally, the code includes a function to predict if an input song is a hit in a given timeframe. This is done using the Spotify API to get the song's features and the trained logistic regression model to make the prediction.

   The methodology is implemented in Python using libraries such as pandas, numpy, matplotlib, seaborn, sklearn, and spotipy. The code is organized into functions, each performing a specific task, to make it modular and easy to understand.

## Results

The results are visualised using line graphs and heat maps for the main parameters. The project shows that popular music is becoming less variable and fairly predictable, meaning that performers do follow somefeatures.

## Dependencies

- Python
- pandas
- numpy
- pickle
- requests
- matplotlib
- seaborn
- scikit-learn
- psynlig
- shap
- statsmodels
- spotipy

## Usage

To use this project, clone the repository to your local machine and run the Python script. The script will load the data, perform the analysis, and generate the plots.

## Contributing

Maxim Velli: Brainstorming, Data Extraction, Predictive Accuracy & Feature Correlation Analysis, Data Visualisation, Hit Predictor
Eva Koskova: Brainstorming, SHAP Feature Importance Analysis, Artist Feature Trend Analysis
Marc Santolini: Brainstorming, consultations

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

