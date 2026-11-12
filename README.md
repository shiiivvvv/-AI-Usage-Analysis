# AI Usage Analysis

## Goal
Analyse how students and professionals use AI tools, and which tools, purposes and habits go with higher productivity, satisfaction and time saved.

## Data
- Source: ai_usage_and_impact_on_students_And_professional & link is -"https://www.kaggle.com/datasets/eishatuzzuhra/ai-usage-and-impact-on-students-and-professionals"
- 300 rows and 19 columns in the raw file; 288 rows after cleaning
- Columns include user type, country, AI tool, purpose, daily usage hours, monthly cost, productivity, satisfaction and time saved

## Data Cleaning
- Duplicates: 12 rows were exact copies (all 19 columns identical) and were dropped (300 to 288 rows)
- Inconsistent text: standardised Gender, Country and AI_Tool (e.g. `Chat GPT`/`chatgpt` to `ChatGPT`, `U.K.` to `United Kingdom`) and grouped 16 Education_Level spellings into 6 levels
- Mixed languages: translated Portuguese and French job titles to English
- Text to numbers: removed `$`, `,` and `hrs` from income, cost and hours columns and converted them to numeric
- Outliers: set to missing a student income of 250000 (next highest 10311), a usage value of 23 hrs/day (next highest 9.9), and two Age values of 97 (next highest 64)
-- Missing values: 5 to 37 per column out of 288 rows (highest is Age at about 13%); only User_ID and User_Type are complete. Left as missing and excluded per chart when needed

## Key Insights
1. Time_Saved_Hours_Per_Week - 
- for the student is -> 6.0 hrs per week
- for the Professional -> 5.6 hrs per week

2. Productivity_Score -
- ChatGPT has 5.23 avg productivity score
- Claude has 5.29  avg productivity score
- Copilot has 5.51 avg productivity score
- DeepSeek has 5.53 avg productivity score
- Gemini has 5.06 avg productivity score
- Grammarly has 5.11 avg productivity score
- Meta AI has 5.15 avg productivity Score
- Perplexity AI has 4.64 avg productivity score

3. I found that average satisfaction is similar across AI tools (5.7 to 6.3 out of 10). Copilot (6.30, 33 users), Grammarly (6.29, 14 users) and ChatGPT (6.26, 115 users) are effectively tied, so the choice of tool seems to matter less than how people use it. Gemini scored lowest (5.68, 38 users). DeepSeek, Meta AI and Grammarly have under 15 users each, so their averages are less reliable.

4. Copilot ranks near the top on both satisfaction and productivity, while Gemini and Perplexity rank near the bottom on both. Scores are close overall, and tools with under 15 users (DeepSeek, Meta AI, Grammarly) are too small to rank confidently.
 

## Charts
![Satisfaction vs productivity by tool](svp.png)
![Hours saved by user type](time saved.png)
![Co relation map](co relation map.png)
![age and ai ](age and ai.png)


## Tools
Python, pandas, NumPy, matplotlib, seaborn, Jupyter Notebook

## Files
- `AI_usage_analysis.ipynb`: full notebook
- `AI usage.csv`: raw data
- `AI_usage_clean.csv`: cleaned data
