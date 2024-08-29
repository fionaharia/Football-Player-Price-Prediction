# Modeling Market Valuation in Football

## :soccer: **Project Overview**

> This project aims to develop a machine learning model capable of predicting the transfer market value of football players. The transfer market is a multi-million dollar industry, and accurate player valuation is critical for clubs to make informed transfer decisions. By analyzing historical transfer data, player performance metrics, and other relevant factors, this project provides valuable insights to help clubs evaluate players' market value.

##  :pushpin: **Dataset Description**
> The dataset used in this project is fifaindex_21.csv, which includes data on over 18,000 players in the FIFA league. The dataset contains 42 features that are used to train the model. These features are categorized into the following groups:

    - Player Description 
    - Technical Skills
    - Defense
    - Aptitude
    - Passes
    - Physical Attributes
    - Shots
    - Goalkeeper Abilities

##  :bar_chart: **Dataset Preprocessing and EDA**

> Data preprocessing involved addressing inconsistencies, errors, and missing values to prepare the data for analysis. Key steps included:

1. **Handling Missing Values** : Approximately 1.4% of data had missing values in the Value column, which were dropped for testing purposes.
2. **Correlation Matrix** : Created to identify the relationship between in-game attributes and player value.
   
   ![image](https://github.com/user-attachments/assets/a6f293df-c96b-4545-b9b2-f99f95b60fd7)

3. **Age Classification Encoding** : Players were encoded into age categories to analyze age-related trends.
   
    ![image](https://github.com/user-attachments/assets/956c8858-5ef8-4464-b848-d27b4e64a1c0)

   The difference in reaction score descreases significantly the age of 40. Composure appears to increase with age. This could be because older players have more experience in dealing with pressure situations

4. **Player Rating Classification**: Encoded players based on skill levels, simplifying the analysis by grouping them into performance tiers.
5. **Skill Profiles** : By analyzing these skill profiles, it can be ensured that the players clubs acquire are well-suited to their tactical needs and overall strategy. The skill profile also allows for a nuanced comparison of players, helping to identify those who excel in specific areas and might command higher market values due to their specialized abilities.

   ![image](https://github.com/user-attachments/assets/d5923cee-72f6-420d-8833-04180965d571)


## :bulb: Model Selection and Evaluation
> Various regression models were employed to predict player prices, including:

| Model             | Accuracy          |
| ----------------- | -----------------|
| Linear Regression | 71% |
| Random Forest Regressor | 90% |
| Decision Tree Regressor | 80% |
| Support Vector Regression | 43% |

Performance evaluation showed that the Random Forest Regressor outperformed other models due to its robustness and ability to handle non-linear relationships.

## :wrench: Deployment

The final model was deployed using Flask. The deployment includes two pages:

- **Player Selection**: A dropdown list of all 18,000 players.
- **Price Prediction**: Once a player is selected, clicking the "Predict" button redirects to a page displaying the predicted market value of the player.

### Deployment Preview

![image](https://github.com/user-attachments/assets/d8f8531a-6981-4d7b-95c8-ae17b6e89d41)

![image](https://github.com/user-attachments/assets/d35279d8-c11b-4b71-abc5-6b6edf1ddacb)

![image](https://github.com/user-attachments/assets/ca89875c-13ca-4936-b3fb-59194da22d54)




