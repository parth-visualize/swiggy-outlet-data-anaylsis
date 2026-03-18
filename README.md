# 🍽️ Swiggy Bangalore Outlet Data Analysis

An end-to-end Exploratory Data Analysis (EDA) project on Swiggy food outlet data from **Bangalore**. The project uncovers insights about restaurant ratings, pricing, cuisine distribution, and area-wise trends across key Bangalore localities — using Python, Pandas, Seaborn, and Plotly.

---

## 📁 Project Structure

```
swiggy-outlet-data-analysis/
│
├── Swiggy_Bangalore_Outlet_Details.csv          # Raw dataset (118 outlets)
├── full_project.ipynb                           # Jupyter Notebook — full EDA
├── SWIGGY_BANGALORE_OUTLET_DATA_ANALYSIS.pptx  # Project presentation deck
└── README.md                                    # Project documentation
```

---

## 🗃️ Dataset Overview

**File:** `Swiggy_Bangalore_Outlet_Details.csv`  
**Records:** 118 restaurant outlets across Bangalore

| Column         | Description                                          |
|----------------|------------------------------------------------------|
| Shop_Name      | Name of the restaurant/outlet                        |
| Cuisine        | Cuisine type(s) served (comma-separated)             |
| Location       | Area and sub-locality in Bangalore                   |
| Rating         | Customer rating (out of 5); `--` treated as 0        |
| Cost_for_Two   | Approximate cost for two people (₹)                  |

### 📍 Areas Covered
- **Koramangala**
- **HSR Layout**
- **BTM Layout**
- **Jayanagar**

### 🍴 Cuisine Variety
48 unique cuisine types including Indian, Chinese, Biryani, Fast Food, Cafe, Italian, Healthy Food, Andhra, Lebanese, Oriental, and more.

### 💰 Price Range
- Minimum: ₹100 &nbsp;|&nbsp; Maximum: ₹800  
- Average Rating: **4.1 / 5**

---

## 🔍 Analysis Performed

### 🟢 Data Preprocessing
- Loaded and explored the dataset using `pandas`
- Checked for null/missing values
- Cleaned `Rating` column — replaced `"--"` entries with `0`
- Cleaned `Cost_for_Two` column — stripped `₹` symbol and converted to `int`

### 📊 Exploratory Data Analysis

#### 1. Rating Distribution
- Plotted overall rating distribution using `sns.distplot`
- Filtered valid ratings (> 0) for accurate analysis

#### 2. Area-Wise Analysis (BTM, HSR, Koramangala)

| Area         | Rating Insight                   | Cost Insight                    |
|--------------|----------------------------------|---------------------------------|
| BTM          | Peak ratings between 4.1 – 4.2   | Most outlets priced ₹250 – ₹350 |
| HSR          | Most outlets rated 4.0 and above | Avg cost ₹350 – ₹400            |
| Koramangala  | Ratings cluster around 4.1 – 4.3 | Most outlets priced ₹250 – ₹275 |

#### 3. Cost vs Rating Analysis
- Scatter plot (Plotly) of `Cost_for_Two` vs `Rating` for outlets rated ≥ 4.0
- Bubble size represents cost; color indicates rating tier

#### 4. Affordable & Highest Rated Restaurants
- Filtered outlets with `Rating ≥ 4.0` and `Cost_for_Two ≤ ₹500`
- Bar chart of top affordable outlets sorted by rating
- Top 15 cheapest + highest rated restaurants visualized using `px.bar`

#### 5. Cuisine Analysis
- Parsed multi-value `Cuisine` column to build a frequency dictionary
- **Overall Bangalore** cuisine distribution — bar chart + pie chart (top 10)
- **Area-wise cuisine breakdown** for BTM, HSR, and Koramangala — individual bar & pie charts

---

## 📈 Visualizations Used

| Library          | Charts Used                                          |
|------------------|------------------------------------------------------|
| `Seaborn`        | Distribution plots, histograms, bar plots            |
| `Matplotlib`     | Figure sizing, axis labels, titles                   |
| `Plotly Express` | Interactive scatter plots, bar charts, pie charts    |

---

## 🛠️ Tech Stack

| Tool              | Purpose                           |
|-------------------|-----------------------------------|
| Python 3.x        | Core programming language         |
| Pandas            | Data loading, cleaning, wrangling |
| NumPy             | Numerical operations              |
| Matplotlib        | Static visualizations             |
| Seaborn           | Statistical plots                 |
| Plotly Express    | Interactive visualizations        |
| Jupyter Notebook  | Development environment           |

---

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn plotly jupyter
```

### Run the Notebook
```bash
git clone https://github.com/parth-visualize/swiggy-outlet-data-anaylsis.git
cd swiggy-outlet-data-anaylsis
jupyter notebook full_project.ipynb
```

---

## 💡 Key Findings

- **Koramangala** has the highest concentration of outlets and the widest cuisine variety.
- **HSR Layout** outlets tend to have higher average pricing compared to BTM and Koramangala.
- Most highly-rated outlets fall in the **₹250–₹400** price range — the sweet spot for quality + affordability.
- **North Indian, Chinese, and Fast Food** are the most frequently listed cuisines across all areas.
- Several outlets with ratings of **4.5+** are priced under ₹300, making them the best value picks.

---

## 📊 Presentation

A PowerPoint summary of the full analysis is available in:  
📄 `SWIGGY_BANGALORE_OUTLET_DATA_ANALYSIS.pptx`

---

## 🙋‍♂️ Author

**Parth**  
🔗 [GitHub](https://github.com/parth-visualize)

---
