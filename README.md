# Electoral Framing in U.S. Historical Newspapers (1930–1945)


This project utilizes the American Stories dataset, a structured historical newspaper dataset 
corpus developed by Melissa Dell and collaborators, to investigate the relationship 
between media sentiment and electoral behavior in the United States from 1930 to 1945.
By using Dell’s enhanced pipeline, we gain access to a cleaner, more legible, and highly 
structured dataset of full-text newspaper articles from cities and rural communities alike.

# Research Focus

This project aims to quantify the influence of newspaper tone and vocabulary on electoral support for 
Franklin D. Roosevelt (FDR) across the 1932–1944 election cycles. Specifically, it examines:

1. General sentiment analysis of pre-election media coverage
2. The framing of political and economic language.
3. Regional variation in media tone and its impact on voting behavior

# Methodological Robustness Test**

The document tests three different analytical approaches to measure how newspaper content correlates with Roosevelt's vote share across 10 regional election pairs (1932–1944):

Approaches Tested:

| Approach                             | Description                                       | Correlation (r) | R²    | Notes                 |
| ------------------------------------ | ------------------------------------------------- | --------------- | ----- | --------------------- |
| **Pre-Election Articles (6 months)** | All articles from 6 months before each election   | -0.702          | 0.493 | Strongest correlation |
| **Full Election Year Articles**      | All articles from the entire election year        | -0.504          | 0.254 | Moderate correlation  |
| **Pre-Election Headlines Only**      | Only headlines from the 6 months before elections | -0.490          | 0.240 | Most interpretable    |

Conclusion: Results are method-dependent. None of the approaches yield a strongly reliable predictive model, but the Pre-Election Articles approach shows the strongest statistical signal.



# Sentiment Analysis (VADER) → Roosevelt Vote Share

 Key Results:

* Correlation**: **+0.370** (Moderate positive)
* Sample Size**: 10 region-election combinations
* Insight: Positive newspaper sentiment in a region before an election tends to correlate with **higher vote share for Roosevelt.

 Regional Breakdown:

| Region  | Avg Sentiment | Avg Roosevelt Vote Share |
| ------- | ------------- | ------------------------ |
| Midwest | 0.172         | 54.7%                    |
| West    | 0.173         | 62.0%                    |
| South   | 0.237         | 80.6%                    |

Results: Media sentiment may have modestly influenced voter behavior in Roosevelt’s favor.

---

# Political Language → Roosevelt Vote Share**

 Key Results:

 Correlation**: -0.782 (Strong negative)
 Positive/Negative Ratio: 3.13 (much more positive political language than negative)
 Insight: Surprisingly, more positive political language** in newspapers correlated with **lower vote shares for Roosevelt.

By Year:

| Year | Net Political Sentiment | Avg Roosevelt Vote Share |
| ---- | ----------------------- | ------------------------ |
| 1932 | 5,434                   | 58.0%                    |
| 1936 | 5,725.5                 | 63.5%                    |
| 1940 | 2,997.7                 | 63.0%                    |
| 1944 | 4,284.7                 | 65.4%                    |

  Interpretation:

   Possibly, opposition papers** were using positive political terms to critique Roosevelt indirectly.
   Rhetorical positivity might not equate to endorsement of Roosevelt’s policies.


# Economic Language → Roosevelt Vote Share**

Key Results:

Correlation: -0.768 (Strong negative)
Recovery/Crisis Ratio: 2.67 (more positive economic coverage)
Insight: Like political language, more positive economic terms (e.g., "growth", "recovery") were linked with lower Roosevelt support.

Regional Analysis:

| Region  | Avg Economic Sentiment | Avg Vote Share |
| ------- | ---------------------- | -------------- |
| Midwest | 3,993.5                | 54.7%          |
| West    | 1,835.2                | 62.0%          |
| South   | 50.0                   | 80.6%          |

   Interpretation:

   Positive economic news may reflect less urgency for Roosevelt's New Deal policies**.
   Opposition media** might have downplayed crises by emphasizing recovery narratives.

---

# Roosevelt-Specific Language Impact**

  Key Results:

  Correlation: +0.066 (Very weak)

  Sample Size: Over 5.7 million articles

  Insight: Direct mention or praise of Roosevelt had **little predictive power** on actual votes.

  Interpretation: Roosevelt's support may have been more **personality- or policy-driven**, rather than based on how frequently he was mentioned or how favorably.

---

#  Sentiment Evolution Over Time

This section analyzes how newspaper sentiment evolved across the four elections and compares it to Roosevelt’s vote share.

Summary Table:

| Election Year | Sentiment Score | Vote Share | Number of Articles |
| ------------- | --------------- | ---------- | ------------------ |
| 1932          | -0.400          | 56.3%      | 418,329            |
| 1936          | +0.300          | 60.3%      | 340,131            |
| 1940          | +0.100          | 54.4%      | 219,975            |
| 1944          | +0.200          | 51.6%      | 311,512            |

  Trend: While sentiment improved, vote share slightly declined.

  Correlation: +0.053(essentially negligible)

Interpretation: Sentiment may not directly explain electoral shifts; other factors, such as war, policy, or opposition narratives, likely played a role.


# Overall Research Significance**

  This analysis demonstrates the **complex relationship** between newspaper content and voter behavior:

  Not all positive language helps**: In both political and economic contexts, upbeat coverage sometimes correlated negatively with Roosevelt's support.
  Sentiment influence is real but nuanced: While general sentiment showed a moderate correlation, word choice and context mattered deeply.
  Methodology impacts results: How data is selected and processed significantly alters the strength and direction of correlations.


# Project Contribution
This project contributes empirical evidence to the long-standing hypothesis that media framing influences 
electoral behavior. By leveraging large-scale structured historical data, it sheds light on how sentiment, 
political vocabulary, and economic discourse impacted voter choices during one of the most turbulent eras in 
American history. It also underscores the critical role of methodological design in computational media studies, 
with implications for political economy, communication, and historical NLP.

# Code Repository

Main Codebase: Preprocessing, VADER sentiment scoring, lexicon-based counting

Visualization Script: Generates election-cycle plots, scatter matrices, regional trend lines


# Reference:
1. @misc{dell2023american, title={American Stories: A Large-Scale Structured Text Dataset of Historical U.S. Newspapers}, author={Melissa Dell and Jacob Carlson and Tom Bryan and Emily Silcock and Abhishek Arora and Zejiang Shen and Luca D'Amico-Wong and Quan Le and Pablo Querubin and Leander Heldring}, year={2023}, eprint={2308.12477}, archivePrefix={arXiv}, primaryClass={cs.CL} }

# Output 
The output includes all the images and visualizations of the data analysis. An important image for viewing is output 14. 

# This is an independent work and does not have a paper written for an explanation.


