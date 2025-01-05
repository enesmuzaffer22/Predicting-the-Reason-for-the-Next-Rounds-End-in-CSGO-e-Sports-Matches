# Introduction

In this project, a machine learning model has been developed to predict the reason for the end of the next round using a dataset from CS:GO e-sports matches. The aim of the project is to understand the game dynamics by performing analyses on specific maps and economic models and to predict future rounds based on these dynamics. Various machine learning models have been employed in this context, and the outputs are presented through an interface.

# Literature Review

In recent years, the application of data analytics and machine learning in complex team-based games like CS:GO has increased. Studies on game data generally focus on map balance, economic strategies, and player behavior. For example, research has been conducted on the advantages of CT and T sides on maps, player clustering behavior, and round success rates. Unlike these studies, this project presents an approach focused on prediction by combining both map and economic factors.

# Dataset

The project uses a dataset consisting of approximately 70,000 rows. Although the original dataset contains more attributes, only the necessary ones have been selected for this study. The dataset includes the following columns:

- **Row ID**: A unique ID that defines each round.
- **Map Name (mapName)**: The map on which the round was played.
- **Round Number**: The round number in the match.
- **T-side Score (tScore) and CT-side Score (ctScore)**: The score status at the beginning of the round.
- **CT-side and T-side Economy Status (ctBuyType, tBuyType)**: The economic status of the teams (low, medium, high).
- **Round End Reason (roundEndReason)**: The reason the round ended (bomb planted, defused, all players eliminated, etc.).
- **Winning Side (winningSide)**: The winning side, either CT or T.

Preprocessing was applied to the dataset, and categorical variables were transformed using label encoding. The score and economy data were standardized. The dataset was obtained from the Kaggle platform \[1\].

# Method

Three different machine learning models were used in the project:

1. **Random Forest Classifier**: A ensemble model based on decision trees. This model is effective in learning complex relationships between attributes in the dataset and often provides fast predictions.
2. **Logistic Regression**: A linear classification model. Logistic Regression was used to model the linear relationships between dependent and independent variables in the dataset.
3. **Gradient Boosting Classifier**: An ensemble model that combines weak learners to create a strong model. This model stands out, especially for improving accuracy, by using sequential learning methods.

The models learned the relationships between the independent variables (map, score status, and economy status) and the dependent variable (round end reason). The data was split into 80% training and 20% testing, and accuracy rates were calculated using various metrics on the dataset.

# Experimental Results

The obtained accuracy rates are as follows:

| Model               | Accuracy Rate |
|---------------------|---------------|
| Random Forest       | 39%           |
| Logistic Regression | 41%           |
| Gradient Boosting   | 44%           |

Additionally, an interactive interface was designed as part of the project, and in this interface:

- The round end reasons specific to the map were visually presented,
- The round end reasons for specific economy statuses were analyzed,
- The reason for the next round's end was predicted based on user input.

# Conclusion and Evaluation

The project was able to make meaningful predictions based on maps and economy statuses using CS:GO match data. It was observed that the Gradient Boosting model achieved the highest accuracy rate. Additionally, thanks to the interactive interface, users are able to both understand the game dynamics and predict potential reasons for the end of future rounds. Future work could further improve these models by processing larger datasets and incorporating player behavior.

# Information

The project was developed using the Python programming language. The following libraries were used:

- **Pandas**: Data processing and analysis.
- **NumPy**: Numerical computation.
- **Scikit-learn**: Machine learning models and data preprocessing.
- **Matplotlib and Seaborn**: Data visualization.
- **Ipywidgets**: Interactive interface design.

These libraries were used for processing the dataset, training the models, calculating accuracy rates, and allowing users to experience the project interactively on the Google Colab platform.

# References

[1] CS:GO esport matches: round data - HLTV.org, Accessed: 02.01.2025, [https://www.kaggle.com/datasets/livanoff/csgo-esport-matches-round-data](https://www.kaggle.com/datasets/livanoff/csgo-esport-matches-round-data)

# Appendix

[Google Colab Project Link](https://colab.research.google.com/drive/15YozWUYVQqfxdenIl_jmyBJZeFbwOlGr?usp=sharing)
