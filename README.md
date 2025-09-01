# 🎬 Netflix EDA & Probability Analysis

This project explores the Netflix dataset using **Exploratory Data Analysis (EDA)** and **Probability Distributions**.  
It covers data cleaning, visualization, and applying statistical probability concepts like **Bernoulli, Binomial, Multinomial, and Poisson distributions**.

---

## 📊 Project Workflow

1. **Data Cleaning**
   - Handled missing values (`director`, `cast`, `country`)
   - Converted `date_added` into year & month
   - Extracted movie durations & TV show seasons
   - Split `listed_in` into genres
   - Removed duplicates

2. **Exploratory Data Analysis**
   - Movies vs TV Shows (overall + trends)
   - Monthly & yearly additions
   - Content growth by country
   - Distribution of durations & seasons
   - Top directors & actors
   - Genre & rating analysis
   - Heatmaps (Country vs Genre, Monthly trends)

3. **Probability Analysis**
   - Bernoulli: Probability of Movie vs TV Show
   - Binomial: Probability of k Movies in n picks
   - Multinomial: Country-wise probabilities
   - Poisson: Content release modeling

4. **Visualization**
   - Histograms, Bar plots, Line plots, Heatmaps
   - Probability Mass Functions (PMF), CDFs
   - Pie charts for ratings

---

## 🛠️ Tech Stack

- Python 🐍
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy

---

## 📂 Repository Structure

├── data/ # Raw & cleaned data<br>
├── notebooks/ # Jupyter notebooks<br>
├── images/ # Visualization screenshots<br>
├── README.md # Documentation<br>
├── requirements.txt # Dependencies<br>



---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/Netflix-EDA-Probability-Analysis.git
   cd Netflix-EDA-Probability-Analysis

2. Install dependencies:
    ```bash
    pip install -r requirements.txt

3. Run Jupyter Notebook:
    ```bash
   jupyter notebook notebooks/Netflix_data.ipynb

---

📌 Future Work

Add WordCloud for title/description analysis

Perform hypothesis testing on movie durations

Build interactive dashboards (Plotly/Streamlit)


---

📜 Credits

Dataset: Netflix Titles Dataset - Kaggle


---

## 📦 requirements.txt

  ```txt
  pandas
  numpy
  matplotlib
  seaborn
  scipy
