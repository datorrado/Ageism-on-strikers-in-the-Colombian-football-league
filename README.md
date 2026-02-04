
> 📌 **Note:**  
> All analysis is contained in a single, fully documented notebook:  
> **`ColombianFootball.ipynb`**

---

## 🧠 Methodology Overview

### 1️⃣ Descriptive Age Trends
- Mean and distributional age of Top-15 scorers by season
- Cross-league comparison (Colombia vs Argentina vs Brazil)
- Structural break exploration around the post-2020 period

### 2️⃣ Statistical Trend Testing
- **Mann–Kendall non-parametric trend test** applied to age time series
- Confirms a statistically significant upward age trend among elite scorers

### 3️⃣ Age–Performance Relationship
- **LOWESS smoothing** of goals per 90 minutes vs age
- Comparison of pre-2020 and post-2020 scoring curves
- Used to test whether aging corresponds to declining efficiency

### 4️⃣ Striker Archetypes (Clustering)
Using K-Means on:
- Age  
- Minutes played  
- Goals per 90  

This identifies **distinct striker profiles**, such as:
- Emerging / rotational scorers  
- High-usage elite veterans  
- Stable, experienced contributors  

The evolution of these profiles over time reveals compositional changes in elite scorers.

### 5️⃣ Probability Modeling (Random Forest)
A Random Forest classifier estimates:
- The probability of finishing in each Top-15 ranking position

Features include:
- Age  
- Minutes played  
- Goals & goals per 90  
- Previous ranking position  
- Career Top-15 appearances  

This allows comparison between:
- **Newcomers**
- **Elite veterans**
- **Theoretical average players**

---

## 📊 Key Visual Results

The notebook includes:

- 📈 Mean age of Top-15 scorers over time  
- 📉 LOWESS age–performance curves (pre vs post-2020)  
- 🔥 Heatmaps of Top-15 access probabilities by age and rank  
- 🧩 Evolution of striker archetypes across seasons  

*(Figures shown in this repository are generated directly in the notebook.)*

---

## 🔍 Main Findings

- **Top scorers in Colombia are significantly older today than a decade ago**, a result confirmed by non-parametric trend tests.
- **Scoring efficiency does not decline sharply with age** among elite forwards; in recent seasons, older players maintain or even improve per-90 output.
- The observed aging trend is **compositional**, not biological:
  - Teams increasingly rely on **experienced, proven strikers**.
  - Younger players are less represented at the very top of rankings.
- **Experience variables** (previous rankings, career persistence) strongly influence ranking probabilities, alongside age.

In short:  
> Modern elite scorers are older not because young players are worse, but because **experience has become more valuable at the top of the scoring distribution**.

---

## 🛠️ Tech Stack

- Python  
- Pandas / NumPy  
- Matplotlib / Seaborn  
- Statsmodels (LOWESS)  
- Scikit-learn (KMeans, Random Forest)  

---

## 🚀 How to Use

1. Clone the repository  
2. Open `ColombianFootball.ipynb`  
3. Run cells sequentially (the notebook is self-contained)

---

## 📌 Final Note

This project is designed as an **exploratory football analytics study**, blending statistical rigor with narrative interpretation — ideal for showcasing applied data science in sports contexts.

If you’re interested in extensions (other leagues, positions, or seasons), the pipeline is easily adaptable.

---

**Author:** David Torrado  

