
# 🧾 User Engagement Analysis

_Analyzing user engagement patterns across reviews, tips, and check-ins to understand restaurant success drivers and unlock insights for improving visibility, ratings, and customer interaction using SQL, Python & Statistics._

---

## 📌 Table of Contents
- <a href="#overview">Overview</a>
- <a href="#business-problem">Business Problem</a>
- <a href="#dataset">Dataset</a>
- <a href="#tools--technologies">Tools & Technologies</a>
- <a href="#project-structure">Project Structure</a>
- <a href="#data-cleaning--preparation">Data Cleaning & Preparation</a>
- <a href="#Analysis">Analysis</a>
- <a href="#research-questions--key-findings">Research Questions & Key Findings</a>
- <a href="#how-to-run-this-project">How to Run This Project</a>
- <a href="#final-recommendations">Final Recommendations</a>
- <a href="#author--contact">Author & Contact</a>

---
<h2><a class="anchor" id="overview"></a>Overview</h2>

This project investigates how reviews, check-ins, tips, sentiment scores, and elite user activity influence restaurant performance. A complete analytical workflow was built using SQL for data extraction and processing, and Python for correlation analysis, sentiment evaluation, statistical analysis, trend evaluation and behavioral insights.

---
<h2><a class="anchor" id="business-problem"></a>Business Problem</h2>

The restaurant industry is highly competitive, and business success depends heavily on how effectively a restaurant attracts and engages its customers. This project aims to:
- Understand how user engagement (reviews, tips, check-ins) influences key success metrics like review count and average rating
- Identify whether higher engagement actually translates into better business visibility and customer trust
- Analyze differences in engagement patterns between high-rated and low-rated restaurants
- Examine how engagement trends vary across cities, seasons, and time periods
- Evaluate the behavioral impact of elite users and sentiment-driven interactions
- Determine which engagement factors contribute most to sustained restaurant performance


---
<h2><a class="anchor" id="dataset"></a>Dataset</h2>

- The dataset used in this project is stored in the data/ folder. The original Yelp Open Dataset can be downloaded from:

```bash
https://business.yelp.com/data/resources/open-dataset/
```
- It includes five JSON files — business, review, user, tip, and checkin — which together form the complete dataset used for this analysis.

---

<h2><a class="anchor" id="tools--technologies"></a>Tools & Technologies</h2>

- SQL (Common Table Expressions, Joins, Filtering)
- Python (Pandas, Matplotlib, Seaborn)
- Statistics
- GitHub

---
<h2><a class="anchor" id="project-structure"></a>Project Structure</h2>

```
vendor-performance-analysis/
│
├── README.md
├── .gitignore
├── User Engagement Report.pdf
│
├── notebooks/             # Jupyter notebooks
│   ├── user_engagement_analysis.ipynb
│
├── data/                  # Yelp dataset
│   └── data_url.txt
```

---
<h2><a class="anchor" id="data-cleaning--preparation"></a>Data Cleaning & Preparation</h2>

- Filtered the dataset with conditions:
   - Categories containing “restaurant”
   - is_open = 1
- Merged datasets using business_id to create a unified engagement view (reviews, check-ins, tips, and ratings).
- Converted data types, handled outliers, merged lookup tables

---
<h2><a class="anchor" id="Analysis"></a>Analysis</h2>

**Negative or Zero Values Detected:**
- Review Count: Minimum = 0 (restaurants with zero engagement)
- Check-ins: Minimum = 0 (no physical footfall recorded)
- Tip Count: Minimum = 0 (no user interaction beyond reviews)
- Rating Values: Minimum = 1.0 (valid Yelp lower rating limit, no invalid negatives)

**Outliers Identified:**
   - High Review Counts: Certain highly popular restaurants show extremely high review activity, indicating viral or long-standing businesses
   - Large Check-in Spikes: A few locations exhibit unusually high check-in volumes, suggesting nightlife hubs or peak-event venues
   - Elite User Interactions: Elite users generate disproportionately higher engagement, skewing interaction metrics for some restaurants

**Correlation Analysis:**
   - Positive correlation between review count and check-ins
   - Positive correlation between review count and tip count
   - Higher-rated restaurants (4.0+) show higher engagement, validating the hypothesis
   - Elite user activity strongly linked to higher review count and restaurant visibility

---
<h2><a class="anchor" id="research-questions--key-findings"></a>Research Questions & Key Findings</h2>

1. **Engagement vs Ratings**: Higher review, tip, and check-in activity is strongly associated with higher restaurant ratings (3.5–4.5 stars).
2. **Engagement Saturation**: Restaurants with a perfect 5.0 rating show a drop in engagement, indicating selective customers or low review motivation.
3. **Elite User Impact**: Elite users contribute a disproportionately high share of total reviews, boosting visibility and credibility for top restaurants.
4. **Sentiment Influence**: Higher counts of useful / funny / cool reactions correlate with better average ratings, suggesting positive sentiment drives trust.
5. **Interlinked Engagement Metrics**: Reviews, check-ins, and tips exhibit strong positive correlations — activity in one metric usually predicts high activity in others.
6. **Time-Based Trends**: User engagement peaks between 4 pm – 1 am, confirming evening/night dining as the primary driver of interaction.


---

<h2><a class="anchor" id="how-to-run-this-project"></a>How to Run This Project</h2>

1. Clone the repository:
```bash
git clone https://github.com/tariqk-analytics/user-engagement-analysis-sql-python-statistics.git
```
2. Download the JSONs and ingest into database:

3. Open and run notebook:
   - `notebook/user_engagement_analysis.ipynb`

---
<h2><a class="anchor" id="final-recommendations"></a>Final Recommendations</h2>

- Prioritize high-engagement restaurants (4.0–4.5★ range)
- Engage elite users to boost visibility and review volume
- Strengthen review, tip, and check-in activity together for higher reach
- Improve service quality for low-rated restaurants (<3.5★)
- Use peak hours (4 PM – 1 AM) for targeted promotions
- Focus marketing efforts on top-performing cities (Philadelphia, Tampa, Indianapolis, Tucson)
- Encourage “useful/funny/cool” style reviews to improve sentiment and ratings

---
<h2><a class="anchor" id="author--contact"></a>Author & Contact</h2>

**Mohd Tariq Khan**  
Data Analyst  
📧 Email: tariqk.analytics@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/tariqk-analytics/?trk=opento_sprofile_details)
