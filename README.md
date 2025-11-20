# **Vietnam National High School Exam Analysis 2025**

## **1. Introduction**

This project performs Exploratory Data Analysis (EDA) on the 2025 Vietnam National High School Graduation Exam scores, comparing trends with the 2022–2024 period. The goal is to uncover score distributions, evaluate exam difficulty, analyze regional disparities, and predict admission thresholds for top universities.

This project demonstrates skills in **Large-scale Data Processing**, **Web Crawling**, **Geospatial Visualization**, and **Statistical Analysis**.

---

## **2. Data Source**

The data used in this project was independently crawled and consolidated into comprehensive datasets.

- **Origin**: Self-crawled from official exam result pages.
- **Scale**: Large-scale datasets containing over 1 million candidate records per year.
- **Coverage**: Full score data for 4 consecutive years (2022, 2023, 2024, 2025).
- **Completeness**: Includes scores for all compulsory and elective subjects (Math, Literature, Foreign Languages, Natural Sciences, Social Sciences).

---

## **3. Tech Stack**

- **Development Environment**: Jupyter Notebook / Google Colab
- **Language**: Python
- **Key Libraries**:
  - **Pandas & Numpy**: Data Cleaning & Manipulation for large datasets.
  - **Matplotlib & Seaborn**: Advanced Data Visualization.
  - **Geopandas**: Geospatial analysis and Choropleth Maps.
  - **Scipy**: Statistical calculations and confidence intervals.

---

## **4. Analysis Workflow**

1. **Data Acquisition**: Built a crawler to fetch >1M records annually and consolidated them into CSV format.
2. **Data Cleaning**:
   - Handled null values and standardized column names.
   - Mapped Student IDs (SBD) to administrative geographical names (Provinces).
   - Calculated composite scores for university admission blocks (A00, A01, B00, C00, D01...).
3. **Exploratory Data Analysis (EDA)**:
   - Analyzed mean score trends and distributions over the years.
   - Evaluated subject correlations.
   - Compared regional performance (North - Central - South).
4. **Visualization**: Presented findings via Heatmaps, Histograms, KDE Plots, and Geographic Maps.

---

## **5. Key Insights**

Here is a summary of the key findings (refer to the notebook for detailed code):

### 1. General Trends

- **Candidate Volume**: Significant increase in 2025 (~8.6% growth compared to previous years).
- **Mathematics**: The exam was notably harder; the average score dropped significantly from ~6.4 (2022) to 4.8 (2025). The distribution is normalized with high differentiation.
- **Literature**: Highest average score (nearly 7.2), normalized distribution, eliminating the "rain of 10s" phenomenon.
- **Foreign Languages**: Low average scores, with strong differentiation in the advanced section of the exam.

### 2. Admission Combination Analysis

<details>
<summary> Click to view details for each Block (A00, A01, B00, C00, D01)</summary>

#### a. Block A00 (Math - Physics - Chemistry)
- **Trend**: Average score decreased by ~1.5 points compared to 2024. Standard deviation increased (4.44).
- **Top 5% (P95)**: Threshold is approximately 26.50.
- **Prediction**: Admission scores for top majors will fluctuate between 25.5 – 27.0.

#### b. Block A01 (Math - Physics - English)
- **Trend**: Flat distribution, no specific peak concentration.
- **Top 5% (P95)**: Decreased to 24.75.
- **Prediction**: Estimated admission scores: 24.5 – 26.5.

#### c. Block B00 (Math - Chemistry - Biology)
- **Trend**: Average score dropped sharply (~2.2 points). Reduced grade inflation.
- **Top 5% (P95)**: Increased to 26.50 due to exceptional performance by the top tier.
- **Prediction**: Top Medical majors will range from 25.0 – 26.5.

#### d. Block C00 (Literature - History - Geography)
- **Trend**: More dispersed distribution, high differentiation.
- **Top 5% (P95)**: Maintained at 26.25.
- **Prediction**: Hot majors will range from 25.0 – 26.5.

#### e. Block D01 (Math - Literature - English)
- **Trend**: Slight decrease in average score, lower spectrum than previous years.
- **Top 5% (P95)**: Dropped to 25.25.
- **Prediction**: Admission scores likely to decrease slightly, ranging 24.5 – 26.5.

</details>

### 3. Geospatial Analysis

- **High Performance Zones**: The Red River Delta and major cities (Hanoi, Ho Chi Minh City, Nam Dinh, Nghe An) dominate in the number of Top 5% candidates, especially in Math and Foreign Languages.
- **Regional Disparity**: The North exhibits a wider and higher score spectrum compared to the South in most Natural Science combinations. The South shows a lower standard deviation (scores are more uniform but average).

---

## **6. Project Structure**

```
├── images/                         # Generated charts (Histogram, Map, Heatmap)
├── datasets/                       # Raw CSV files (2022-2025)
├── PhanTichDiemThiTHPTQG2025.ipynb # Main Analysis Notebook
└── README.md                       # Project Documentation
```

---

## **7. Installation & Usage**

### Clone repository:
```bash
git clone https://github.com/ldgk2712/VietNam-HighSchool-Exam-Analysis-2025.git
cd VietNam-HighSchool-Exam-Analysis-2025
```

### Install Dependencies:
```bash
pip install pandas numpy matplotlib seaborn geopandas scipy
```

### Data Configuration:
- Place the crawled CSV files (2022-2025) and `vnprovince.geojson` into the `datasets/` folder.
- Update file paths in the Notebook if necessary.

### Run Analysis:
- **Option 1 (Local)**: Launch `jupyter notebook` and open the `.ipynb` file.
- **Option 2 (Google Colab)**: Upload the `.ipynb` file and datasets folder to Google Drive, then run via Colab (Recommended for handling >1M rows).

---

## **8. Author**

**Le Dang Gia Khanh**  
Student @ Data Science  

[LinkedIn](https://linkedin.com/in/ledanggkhanh) | [Email](mailto:ldgk2712@gmail.com)

---

*This project is for educational purposes and educational trend research.*