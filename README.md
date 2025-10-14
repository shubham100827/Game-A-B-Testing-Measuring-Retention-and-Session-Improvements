# Game-A/B-Testing Measuring Retention and Session Improvements
This project performs an A/B test to analyze the impact of game design changes in the Cookie Cats mobile game on player behavior. The experiment compares two versions of the game, a control group (current design) and a treatment group (with modified features).
The main goal is to determine whether the modification improves player engagement and retention metrics.

<img width="350" height="150" alt="image" src="https://github.com/user-attachments/assets/589545d1-3158-42f1-b49f-48189a72e79d" />

🎯 **Objectives**
The experiment aims to answer three key questions:
1. Average Sessions:
    Has the average number of game sessions increased by 5 sessions in the treatment group?
2. 1-Day Retention:
    Has player retention increased by 2% after one day?
3. 7-Day Retention:
    Has player retention increased by 5% after seven days?

| Metric                     | Type       | Null Hypothesis (H₀)      | Alternative Hypothesis (H₁) | Test Used          |
| -------------------------- | ---------- | ------------------------- | --------------------------- | ------------------ |
| Average number of sessions | Continuous | No increase by 5 sessions | Increased by 5 sessions     | Independent t-test |
| 1-Day Retention            | Binary     | No increase by 2%         | Increased by 2%             | Proportion z-test  |
| 7-Day Retention            | Binary     | No increase by 5%         | Increased by 5%             | Proportion z-test  |

📊 **Data**
The dataset (Cookie_Cats_cleaned_v01.csv) contains anonymized user-level data with fields such as:
- userid — unique identifier for each player
- version — control or treatment group
- sum_gamerounds — number of game rounds played
- retention_1 — retention after 1 day
- retention_7 — retention after 7 days

The dataset was preprocessed to:
- Remove duplicate users
- Handle missing values
- Standardize column formats

🧠 **Statistical Analysis**
- Statistical tests were applied as follows:
- T-test for continuous metrics (sum_gamerounds)
- Proportion Z-tests for retention metrics (retention_1, retention_7)
- 95% confidence intervals and effect size estimation for interpretability

📈 **Results Summary**
| Metric           | Result                        | Interpretation                                            |
| ---------------- | ----------------------------- | --------------------------------------------------------- |
| Average Sessions | *not significantly increased* | Gate change did not raise engagement in terms of sessions |
| 1-Day Retention  | *slightly decreased*          | Possible friction introduced by gate change               |
| 7-Day Retention  | *decreased*                   | Lower long-term retention for the treatment group         |

**Conclusion:**
Although intuitively the change aimed to improve player retention, the experiment indicates that moving the gate earlier negatively impacted retention, suggesting that players were discouraged by the added friction.

-----
🚀 **How to Run**

Clone this repository:  
```
git clone https://github.com/shubham100827/Game-A-B-Testing-Measuring-Retention-and-Session-Improvements.git
```

Navigate to the folder: 
```
cd Game-A-B-Testing-Measuring-Retention-and-Session-Improvements
``` 

Install dependencies: 
```
pip install -r requirements.txt
```

Open the notebook: 
```
jupyter notebook game_optimization_ab_testing.ipynb
```
-----
