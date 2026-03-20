# 🎬 Netflix Content Analysis — EDA, Statistics & Probability

> An end-to-end data analysis project on Netflix's content library using Python — covering data cleaning, exploratory data analysis, statistical hypothesis testing, probability distributions, and advanced analytical deep dives.

---

## 📌 Project Overview

This project performs a comprehensive analysis of Netflix's content catalog (`netflix_titles.csv`) to uncover patterns in content type, genre distribution, country contributions, release trends, and viewing ratings. The analysis progressively builds from basic data cleaning to advanced statistical reasoning and probabilistic modelling.

**Dataset:** [Netflix Movies and TV Shows — Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)  
**Records:** ~8,800 titles | **Features:** 12 columns  
**Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy, WordCloud

---

## 🗂️ Project Structure

```
netflix-analysis/
│
├── Netflix_data.ipynb        ← Main analysis notebook
├── netflix_titles.csv        ← Dataset (download from Kaggle)
├── README.md
└── requirements.txt
```

---

## 📊 Analysis Sections

### 1. Data Cleaning
- Handled missing values in `director`, `cast`, `country`, `date_added`
- Parsed `date_added` to extract `year_added` and `month_added`
- Engineered features: `duration_num`, `duration_unit`, `genre_list`
- Removed duplicates on `(title, release_year)`
- Standardised text columns (`type`, `rating`)

### 2. Exploratory Data Analysis (EDA)

| Analysis | Key Finding |
|---|---|
| Movies vs TV Shows | ~70% of content is Movies |
| Top countries | USA dominates, followed by India & UK |
| Rating distribution | TV-MA is the most common rating |
| Top genres | International Movies, Dramas, Comedies lead |
| Top directors & actors | Rajiv Chilaka, Anupam Kher among top contributors |
| Movie duration | Right-skewed distribution, mean ~99 min |
| Monthly trends | January & July see peak content additions |

### 3. Probability Measures

Applied real-world probability distributions to Netflix data:

- **Bernoulli** — P(randomly picked title is a Movie) = 0.696
- **Binomial** — P(exactly 7 out of 10 random picks are Movies)
- **Poisson** — Modelling average new content arrivals per year (λ ≈ 119)

### 4. Statistical Hypothesis Testing *(Tier 1)*

| Test | Question | Result |
|---|---|---|
| **Independent t-test** | Is movie duration significantly different from TV show seasons? | Reject H₀ (p < 0.05) |
| **Shapiro-Wilk + QQ-Plot** | Are movie durations normally distributed? | Not normal — right skewed |
| **Chi-Square test** | Is there an association between content type and rating? | Reject H₀ — significant association |
| **WordCloud** | Most frequent words in Netflix descriptions | family, love, life, friend… |

### 5. Advanced Statistical Analysis *(Tier 2)*

- **Conditional Probability** — P(genre | country): Each country's content personality mapped as a probability heatmap
- **Central Limit Theorem Demo** — Showed how sample means of skewed movie durations converge to normal at n ≥ 30
- **Outlier Detection** — IQR, Z-Score, and Modified Z-Score methods compared on movie durations
- **Content Gap Analysis** — Identified underserved genres per country vs. global average
- **YoY Growth Rate + CAGR** — Computed Compound Annual Growth Rate; peak absolute additions in 2019
- **Multi-Variable EDA** — Pair plots, correlation heatmap, hexbin density (duration vs release year), content lag distribution

### 6. Growth Rate Deep Dive

Investigated *why* Netflix's YoY growth rate declined from 423% (2016) to -20% (2021):

- **Base Effect** — % growth naturally falls as cumulative base grows
- **Absolute additions** — Peaked in 2018–2019, genuine slowdown after
- **COVID Impact** — Monthly analysis revealed production halt in Mar–Jun 2020
- **Strategy shift** — Netflix moved from quantity licensing to quality originals post-2020

---

## 📈 Key Insights

1. **Netflix is movie-heavy** — 69.6% of titles are Movies, but TV Show additions grew faster post-2018
2. **USA + India drive the catalog** — Together accounting for over 40% of all content
3. **Content lag is short** — Median gap between a movie's release and its Netflix addition is just 1–2 years
4. **Rating skews mature** — TV-MA and R dominate; Kids/Family content is proportionally underrepresented
5. **Growth % is misleading alone** — 423% in 2016 is a base-effect illusion; absolute additions peaked in 2019

---

## 🛠️ Tech Stack

```
Python 3.x
├── pandas          — data manipulation
├── numpy           — numerical computing
├── matplotlib      — base visualisations
├── seaborn         — statistical plots
├── scipy.stats     — hypothesis testing, distributions
└── wordcloud       — text frequency visualisation
```

---

## ⚙️ Setup & Run

```bash
# 1. Clone the repo
git clone https://github.com/byteephantom/netflix-content-analysis.git
cd netflix-content-analysis

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn scipy wordcloud

# 3. Download dataset
# Place netflix_titles.csv in the project root
# Dataset: https://www.kaggle.com/datasets/shivamb/netflix-shows

# 4. Launch notebook
jupyter notebook Netflix_data.ipynb
```

---

## 🔭 Roadmap — What's Coming Next

- [ ] **K-Means Clustering** — Group Netflix content into natural content profiles
- [ ] **Classification Model** — Predict Movie vs TV Show from features (Logistic Regression + Random Forest)
- [ ] **TF-IDF Content Recommender** — "You watched X → here are similar titles"
- [ ] **Sentiment Analysis** — VADER on descriptions; do thrillers use more negative language?
- [ ] **Streamlit App** — Interactive dashboard with live recommender, deployed on Streamlit Cloud

---

## 📁 Dataset

**Source:** [Kaggle — Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows)  
The dataset is not included in this repository. Download `netflix_titles.csv` from Kaggle and place it in the project root before running the notebook.

---

## 👤 Author

**Quantum Nomad** ([@byteephantom](https://github.com/byteephantom))  
B.Tech Computer Science | Data Analytics & Data Science  

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
