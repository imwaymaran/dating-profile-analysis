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

Before wrapping up the analysis, it's important to reflect on the dataset's methodology and its impact on the validity and generalizability of our findings.

This dataset is **inherently biased**, and that shapes how its insights should be interpreted. The profiles were gathered using two male test accounts, which could only view users recommended by Lovoo’s matching algorithm. Despite creating two distinct profiles, the same limited set of user profiles repeatedly appeared. As a result:

- The dataset contains **only female users**, specifically those who are **heterosexual or bisexual**.
- The age range is narrow - users are between **18 and 28 years old**.
- Other gender identities and orientations are completely excluded.
- The dataset is skewed toward certain **regions and countries** (e.g., France, Denmark, China), likely influenced by the location or settings of the accounts used for scraping.

Additionally, since the app relies on **location-based recommendations**, it's likely that only the most "visible" or algorithmically favored users were included. This introduces further bias in favor of users with more complete profiles or higher in-app activity.

These constraints were evident throughout our EDA - particularly when analyzing demographics and user intent. For example, any comparisons based on country, language, or dating interest should be interpreted within the context of this selection bias.

While the dataset still offers valuable insights into the behavior of a specific user segment, it is **not representative of the broader dating app population**.  
Future analyses would benefit from a more diverse dataset including additional attributes such as gender identity, education, hobbies, and dating outcomes.

## Summary / Key Findings

Our exploratory data analysis focused on understanding how user behavior, profile content, and engagement metrics vary across dating interest, user intent, and profile features.

### 1. Dating Interest Behavior Differences

- Only **38.7%** of users in the dataset indicated they were interested in dating.
- Users who are interested in dating tend to be slightly more active and intentional:
  - They fill out more profile sections.
  - They are more likely to write bios (`freetext`) or status messages (`whazzup`).
  - They receive more profile visits and kisses on average.
- However, **age is not a strong differentiator** between the two groups — both have a median age of 22 and similar age ranges (20–25).

### 2. Profile Characteristics and Engagement

- The **number of profile pictures** is the strongest predictor of profile visibility.
  - Top 5 most visited users had an average of **9.6 photos**, compared to **2.2** for the bottom 5.
  - All top users had at least 3 pictures; 60% of bottom users had none.
- Other factors like **age**, **gender preference**, and **country** showed **minimal variation** between highly and rarely visited profiles.
- Pearson correlation between pictures and profile visits was **0.37** (weak positive), and **0.09** with kisses (very weak).
- **Age and profile visits** showed a **strong negative correlation (-0.70)** — younger users (especially around 23–24) tend to get more views and fans.

### 3. Heterosexual vs. Bisexual Women

- Bisexual women were **more likely to have complete location info** (e.g., filled city fields), while heterosexual women showed more missing data.
- Bisexual users were **slightly more likely to allow profile sharing**, possibly reflecting greater comfort or intentional visibility on the app.
- Heterosexual women showed **greater interest in finding friends**, suggesting more casual or social use of the app.
- Bisexual women received **more kisses and gifts**, potentially reflecting interactions from both male and female users, expanding their engagement pool.
- Heterosexual users made up **all FlirtStars**, though the criteria for this status is unclear.

### 4. Demographics and User Intent

- The average user in the dataset is a **female between ages 20–25**, interested in men, and speaking 1 language.
- Language count had **no significant correlation** with engagement metrics like gifts.
- Profile sharing and chat/friend/dating interest combinations varied but were not strong predictors of overall engagement.

---

These findings suggest that **visual completeness (photos)** and **dating intent** are the clearest signals linked to profile visibility and interaction, while other factors like age or language play a smaller role. Differences between heterosexual and bisexual users also highlight varying platform use patterns, potentially tied to user goals and community dynamics.

## Contributors

This project was a group collaboration. Each team member focused on specific analytical questions:

- [**Zahrea Franklin**](https://github.com/zahreafranklin) —  
  - Q1: What is the demographic profile of an average dating app user?  
  - Q3: What differentiates the top 5 most visited profiles from the bottom 5?
  - Q6:  How does the data collection methodology affect the representativeness of this dataset?  
         What potential biases should we be aware of?

- [**Darylisha Williams**](https://github.com/dwilliams170) —  
  - Q2: What profile characteristics are associated with higher attractiveness or engagement?  
  - Q6:  How does the data collection methodology affect the representativeness of this dataset?  
         What potential biases should we be aware of?

- [**Gennadii Ershov**](https://github.com/imwaymaran) —  
  - Q4: How do users seeking relationships behave differently compared to those looking for friendships or casual chats?  
  - Q6: How does the data collection methodology affect the representativeness of this dataset?  
        What potential biases should we be aware of?

- [**Nadya Tseitlina**](https://github.com/NadyaT-hub) —  
  - Q5: Are there any notable behavioral differences between heterosexual and bisexual women?
  - Q5.2: Are there notable differences in the users' behavior towards these two groups, specifically amount of "tokens" received by heterosexual and bisexual women, such as "gifts" and "kisses"?

Special thanks to our instructors and The Knowledge House for guidance and feedback throughout the project.
