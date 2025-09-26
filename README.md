# EV Sentiment Analysis 🚗🔋

This project analyzes Reddit discussions about **Electric Vehicles (EVs)** to understand public sentiment and the main themes around EV adoption and technology. Using natural language processing (NLP) techniques, we collected, cleaned, and processed tens of thousands of Reddit comments, applied sentiment analysis, and explored common concerns through topic modeling.

---

## 📌 Project Goals
- Scrape EV-related Reddit comments from multiple subreddits
- Clean and preprocess text data
- Perform sentiment analysis (positive, neutral, negative)
- Explore topics within negative and neutral comments for deeper insights
- Summarize overall attitudes towards EV technology

---

## 📂 Repository Structure

```
EV-Sentiment-Analysis/
├── data/
│ ├── reddit_ev_comments.csv # raw dataset (scraped)
│ ├── reddit_ev_preprocessed.csv # cleaned dataset
│ ├── reddit_ev_preprocessed1.csv # alternate preprocessed dataset
│ └── sentiment_analysis_result.csv # final labeled results
│
├── notebooks/
│ └── Sentiment_Analysis_on_EV_Technology.ipynb # main analysis notebook
│
├── README.md
```
---

## ⚙️ Requirements
- Python 3.9 or newer  
- Jupyter Notebook / JupyterLab  

### Key Libraries
- `pandas`, `numpy`
- `nltk`, `langdetect`, `emoji`
- `textblob`
- `scikit-learn`
- `gensim`, `pyLDAvis`
- `tqdm`

Install dependencies with:
```bash
pip install pandas numpy nltk langdetect emoji textblob scikit-learn gensim pyLDAvis tqdm
```

🚀 How to Run

1. Clone this repository:
```
git clone https://github.com/Bhawanajoshi25/EV-Sentiment-Analysis.git
cd EV-Sentiment-Analysis
```
2. Open the notebook:
```
jupyter notebook notebooks/Sentiment_Analysis_EV_Technology.ipynb
```
3. Run all cells in order.

- The notebook will scrape Reddit data (via PRAW) and save the raw dataset into data/reddit_ev_comments.csv
- Preprocessing will generate cleaned CSVs inside data/
- Sentiment analysis will produce data/sentiment_analysis_result.csv

📊 Results

Total comments analyzed: 46,813
Sentiment distribution:
- Positive: 51.6%
- Neutral: 26.0%
- Negative: 22.5%

Key insights:
Most Reddit conversations around EVs are positive, reflecting enthusiasm for adoption and innovation.
Neutral discussions often include questions, factual information, or general conversations.

Negative discussions focus on:
⚡ Charging infrastructure limitations
🔋 Battery life and degradation
💰 High purchase and maintenance costs
🚗 Comparisons with ICE (internal combustion engine) vehicles
🏛️ Government policies and incentives

Topic modeling:
Using LDA (Latent Dirichlet Allocation) on negative and neutral comments, I discovered 5 recurring themes:
1. Charging infrastructure and wait times
2. Battery performance and degradation
3. EV affordability and cost concerns
4. Policy debates and government incentives
5. Tesla-specific issues and comparisons with ICE cars

Interactive visualization of topics was generated using pyLDAvis.

🔎 Reproducibility

- The notebook always scrapes Reddit first, then saves intermediate and final CSVs to data/.
- Preprocessing and sentiment steps also write their outputs into the same folder.
- To reproduce results, simply rerun the notebook.

To ensure consistent results, record package versions with:
```
pip freeze > requirements.txt
```
📖 Acknowledgments

Data collected from Reddit (public subreddits: electricvehicles, EVcharging, Tesla, cars)
Open source Python ecosystem used for NLP and analysis

📜 License
This project is shared for educational purposes as part of a data science portfolio.
