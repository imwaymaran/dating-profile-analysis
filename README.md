# Dating App User Profile Analysis

## Project Overview

This project analyzes a dataset from the Lovoo dating app with the goal of answering several analytical questions related to user behavior, profile engagement, and dating intent.

---

## Stack / Technologies Used

- Python 3
- pandas
- numpy
- matplotlib
- seaborn
- Jupyter Notebook

---

## Data

### Dataset Source

**Title:** [Dating App User Profiles' Stats – Lovoo v3](https://www.kaggle.com/datasets/jmmvutu/dating-app-lovoo-user-profiles/data)  
The dataset was collected from the Lovoo dating app in Spring 2015 (April–May), during its expansion in Europe. It captures user profile data, including engagement metrics like profile visits and kisses, for a sample of female users recommended by Lovoo’s algorithm.

Two CSV files are available in the dataset:

- `lovoo_v3_users_api-results.csv`
- `lovoo_v3_users_instances.csv`

Both contain similar user profile information, but with slight differences in column structure and completeness.  
**We decided to focus our analysis on the `lovoo_v3_users_api-results.csv` file**, as it contains more consistent and complete data for the features we wanted to explore.

### Dataset Context

The dataset was created to explore questions like:

- What makes a dating profile attractive or charismatic?
- How do presentation and profile content affect engagement?
- What traits might correlate with higher visibility (e.g., more visits or matches)?

### Selected Columns

| Column                  | Description                                             |
|-------------------------|---------------------------------------------------------|
| `gender`                | Gender of the user                                      |
| `genderLooking`         | Gender(s) the user is interested in                    |
| `age`                   | Age of the user                                         |
| `name`                  | Name of the user                                        |
| `counts_details`        | Number of profile details provided                      |
| `counts_pictures`       | Number of profile pictures uploaded                     |
| `counts_profileVisits`  | Number of profile views                                 |
| `counts_kisses`         | Number of kisses received                               |
| `counts_fans`           | Number of fans                                          |
| `counts_g`              | Number of gifts received                                |
| `flirtInterests_chat`   | Interested in chatting                                  |
| `flirtInterests_friends`| Interested in making friends                            |
| `flirtInterests_date`   | Interested in dating                                    |
| `country`               | User's country                                          |
| `city`                  | User's city                                             |
| `location`              | User’s general location or coordinates                  |
| `isVip`                 | Whether the user has VIP status                         |
| `lang_count`            | Number of languages spoken                              |
| `verified`              | Whether the user is verified                            |
| `shareProfileEnabled`   | Whether profile sharing is enabled                      |
| `freetext`              | User-provided bio (free text)                           |
| `whazzup`               | User status message (“what's up”)                       |

## Exploratory Data Analysis (EDA)

### Key Analytical Questions

1. What is the demographic profile of an average dating app user in this dataset?
2. What profile characteristics are associated with higher attractiveness or engagement?
3. What differentiates the top 5 most visited profiles from the bottom 5?
4. How do users seeking relationships behave differently compared to those looking for friendships or casual chats?
5. Are there any notable behavioral differences between heterosexual and bisexual women in this dataset?
6. How does the data collection methodology affect the representativeness of this dataset?  
   What potential biases should we be aware of?

## Methodology Thoughts

## Summary / Key Findings

## Contributors

This project was a group collaboration. Each team member focused on specific analytical questions:

- [**Zahrea Franklin**](https://github.com/zahreafranklin) —  
  Q1: What is the demographic profile of an average dating app user?  
  Q3: What differentiates the top 5 most visited profiles from the bottom 5?

- [**Darylisha Williams**](https://github.com/dwilliams170) —  
  Q2: What profile characteristics are associated with higher attractiveness or engagement?  
  Q6: How does the data collection methodology affect the representativeness of this dataset?

- [**Gennadii Ershov**](https://github.com/imwaymaran) —  
  Q4: How do users seeking relationships behave differently compared to those looking for friendships or casual chats?  
  Q6: What potential biases should we be aware of?

- [**Nadya Tseitlina**](https://github.com/NadyaT-hub) —  
  Q5: Are there any notable behavioral differences between heterosexual and bisexual women?
  Q5.2: Are there notable differences in the users' behavior towards these two groups, specifically amount of "tokens" received by heterosexual and bisexual women, such as "gifts" and "kisses"?

Special thanks to our instructors and The Knowledge House for guidance and feedback throughout the project.
