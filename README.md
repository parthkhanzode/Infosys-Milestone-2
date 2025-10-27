# Infosys-Milestone-2

# Milestone 2 — Clustering and Pattern Detection

## 1️. Objective
The objective of this milestone is to perform **behavior clustering and pattern detection** on student study habits and performance data.  
This helps to identify groups of students with similar study behaviors and academic outcomes, enabling targeted recommendations for improving study habits and performance.

---

## 2. Dataset Source
**Dataset Name:** `student_habits_performance.csv`  
**Location:** Google Drive — `/MyDrive/Study_Based_Recommendation/student_habits_performance.csv`  
**Description:**  
- Contains student demographic and behavioral information such as study hours, sleep hours, social media usage, diet quality, internet quality, parental education, part-time job, extracurricular participation, and exam scores.  
- The dataset has numeric, categorical, and textual data.

---

## 3️. Steps Followed

### Step 1: Data Loading
- Loaded the dataset using `pandas.read_csv`.
- Examined the first few rows and column types to understand the data.

### Step 2: Feature Selection
- Selected relevant **numerical features** for clustering:  
  `study_hours_per_day`, `sleep_hours`, `social_media_hours`, `exam_score`, etc.
- Converted categorical text columns into numeric codes where needed (e.g., diet quality, internet quality).

### Step 3: Data Preprocessing
- Scaled numerical features using `StandardScaler` from `sklearn` to standardize values.
- Checked for missing values and ensured all features are numeric for clustering.

### Step 4: Dimensionality Reduction
- Applied **PCA (Principal Component Analysis)** to reduce feature space to 2 dimensions for visualization.

### Step 5: Clustering
#### K-Means Clustering:
- Determined optimal cluster count using **Elbow Method** and **Silhouette Score**.
- Fit the K-Means model and predicted cluster labels.
- Added `kmeans_cluster` column to the DataFrame.

#### DBSCAN Clustering:
- Experimented with different `eps` and `min_samples` values.
- Identified noise points and cluster distribution.
- Added `dbscan_cluster` column to the DataFrame.

### Step 6: Cluster Summary
- Calculated **mean values of key metrics** per cluster.
- Interpreted clusters (e.g., high study hours & high exam scores → Focused & Consistent students).

### Step 7: Visualization
- **Scatter Plot (2D PCA):** Visualized clusters with different colors.
- **Bar Plot:** Mean values of features per cluster.
- **Box Plot:** Exam score distribution across clusters.
- **Count Plot:** Number of students per cluster.
- Saved visualizations in `/visualizations/` folder.

### Step 8: Insights
- Identified behavioral patterns in clusters:
  - Cluster 0: High study hours, high exam scores → Focused & Consistent
  - Cluster 1: Moderate study, average performance → Balanced Learners
  - Cluster 2: Low study, low scores → Distracted / Struggling
  - Cluster 3: High social media usage → Irregular / High Digital Usage

### Step 9: Save Results
- Saved the clustered dataset as `student_clustered.csv`.

---

## 4. Tools Used
- **Python Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`, `sklearn`
- **Google Colaboratory:** Notebook execution and visualization
- **Version Control:** GitHub repository for Milestone submission
- **Google Drive:** Dataset storage and retrieval

---

## 5️. Key Graphs & Observations
- **PCA Scatter Plot:** Shows distinct clustering of student groups.
- **Bar Plot:** Highlights feature differences (study hours, exam scores) among clusters.
- **Box Plot:** Exam score variation across clusters, identifying high and low performers.
- **Count Plot:** Distribution of students in each cluster, showing cluster sizes.

---

## 6️⃣ Folder Structure
