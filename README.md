# TravelTide-Customer-Segmentation
Customer segmentation project combining SQL, Python (ML), and Tableau dashboards for TravelTide.

TravelTide-Customer-Segmentation/
├── data/                # CSVs for Tableau (e.g., tableau_final_data.csv, pca_clusters.csv)
├── sql/                 # SQL cohort extraction queries
├── notebooks/           # Jupyter/Colab notebooks (.ipynb) or .py exports
├── reports/             # Executive summary (PDF), detailed report, presentation slides
├── dashboards/          # Tableau workbook (.twb/.twbx) or Tableau Public link
├── README.md            # Project overview
└── requirements.txt     # Python dependencies

---
├── data/ # Exported datasets for Tableau / analysis
│ ├── tableau_final_data.csv
│ ├── pca_clusters_for_tableau.csv
│
├── notebooks/ # Jupyter/Colab notebooks
│ └── traveltide_project.ipynb
│
├── reports/
│ ├── executive_summary.pdf # 1-page summary for stakeholders
│ ├── detailed_report.pdf # 2–3 page full analysis
│ └── presentation_slides.pdf # Slides for business presentation
│
├── src/ # Python scripts (modularized code)
│ ├── feature_engineering.py
│ ├── clustering.py
│ └── utils.py
│
├── dashboards/
│ └── tableau_dashboard.twbx # Tableau packaged workbook
│
└── README.md # Project documentation (this file)

##  Methodology

### 1. **SQL (Data Extraction)**
- Selected active users (`>7 sessions since Jan 4, 2023`)
- Joined `sessions`, `flights`, `hotels`, and `users` tables
- Cleaned and aggregated features:
  - `num_sessions`, `avg_session_duration`, `discount usage`
  - `num_trips`, `avg_bags`, `km_distance`, `exploration_index`
  - `seasonal travel behavior` (summer flights, winter hotels)
- Exported a **clean, user-level dataset** (no missing values)

### 2. **Python (Feature Engineering & Clustering)**
- Engineered additional features:
  - `bargain_index`, `ads_per_km`, `family_traveler_score`
- Applied clustering methods:
  - **KMeans** (main segmentation, K=4)
  - **DBSCAN** (noise detection, flexible clusters)
  - **Hierarchical Clustering** (to compare structure)
- Reduced dimensionality with **PCA (2D visualization)**
- Profiled each segment with revenue, discounts, and demographics

### 3. **Tableau Dashboards**
- Built interactive dashboards:
  - Segment distribution by demographics
  - Revenue contribution by segment
  - Discount sensitivity analysis
  - Travel distance and age patterns
- Designed for **stakeholder storytelling** (Elena’s business questions)

---

##  Key Insights
- **Family Travelers**: Higher baggage, travel mostly in summer, sensitive to perks like *free child tickets*  
- **Bargain Seekers**: High discount usage, responsive to promotions → *special discounts*  
- **Loyal Explorers**: Travel to many destinations, strong engagement → *exclusive rewards*  
- **Infrequent Users**: Book rarely, need activation offers → *30% off first trip*  

---

##  Deliverables
-  SQL query pipeline for cohort & metrics  
-  Clean user-level dataset for modeling  
-  Python clustering workflow (KMeans, DBSCAN, PCA, Hierarchical)  
-  Tableau dashboards (business storytelling)  
-  Final report & executive summary  

---

##  Technologies Used
- **SQL** (PostgreSQL) – data extraction & cleaning  
- **Python** (pandas, scikit-learn, seaborn, matplotlib) – feature engineering & clustering  
- **Tableau** – dashboards & visualization  
- **Google Colab / Jupyter Notebook** – analysis environment  

---

##  Author
**Tigist Hayilemariyam**  
  
  

---


