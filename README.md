# Road Accident Analysis Dashboard - Excel (Power Query + Pivot Tables)

An interactive Excel dashboard built to analyze road accident patterns and surface actionable insights.  
I used Power Query to clean and transform the raw dataset and Pivot Tables / Pivot Charts to build the interactive visuals — all inside a single `Dashboard.xlsx`.

This project helps spot trends by vehicle type, road type, time trends, severity, and weather conditions so teams can prioritize interventions.

---

## 📊 Features
- **Vehicle-wise analysis** — casualties and counts by vehicle type  
- **Road type breakdown** — which road types see more incidents  
- **Monthly & year-over-year trends** — compare current vs previous year patterns  
- **Severity slices** — fatal, serious, minor injuries analysis  
- **Filters / Slicers** — weather, wind, year, month, and other dimensions for fast exploration  
- **Interactive pivot visuals** — charts built from Pivot Tables for fast rendering on large snapshots

---

## 🔑 Key metrics
- **Total casualties (snapshot):** 
- **Severity breakdown:**  
  - **Slight injuries:**
  - **Serious injuries:**
  - **Fatalities:** 
- **Casualties by vehicle**
- **Top road-type (by casualties):**  
- **Area distribution:** 
- **Light conditions:**
- **Dominant surface condition:** 
- **Monthly CY vs PY trend**
---

## 🛠️ Built With
- Microsoft Excel (desktop)  
- Power Query (data cleaning & transformation)  
- Pivot Tables & Pivot Charts (interactive visuals)  
- Slicers & Excel Data Model

---


## ▶️ Demo
Watch the screen recording demo of the dashboard here:  
👉 [Add demo / video link here]

---

## 📁 Repo structure
/icons/ # icons used in the dashboard (PNG / SVG)
Dashboard.xlsx # main Excel file (contains Power Query transformations, pivot cache & dashboard)
Final_Dashboard.png # screenshot of the final result (screen capture)
README.md # this file

## 📊 Using the Dashboard (important)
- You can open `Dashboard.xlsx` immediately and explore the interactive dashboard — the file already contains the cleaned data snapshot via Pivot Tables, so you **do not** need the original 90MB raw file just to view the visuals.
- **If you want to refresh or reproduce the full cleaning steps**, follow the steps below.

### Dataset (hosted on Google Drive)
The full raw dataset is hosted on Google Drive:

**Direct download URL:**  
`https://drive.google.com/uc?export=download&id=1xi4kcJlYAKGCQqvKBVFUcGgL1G5okKSU`

---
### To refresh with the full raw dataset (recommended workflows)

**Option A — Local (recommended for reproducibility)**
1. Download the dataset from the Drive link above and save it at: `/data/road_accidents.csv` .
2. Open `Dashboard.xlsx` → Power Query Editor → update the `DataPath` parameter (or the query `Source`) to `data/road_accidents.csv`.
3. In Excel: **Data → Refresh All** (or right-click a Pivot Table → Refresh).

**Option B — Direct web fetch**
1. Create/update a Power Query parameter named `DataPath` and paste the direct-download URL:
   `https://drive.google.com/uc?export=download&id=1xi4kcJlYAKGCQqvKBVFUcGgL1G5okKSU`
2. In Power Query use `Web.Contents(DataPath)` as the Source (examples below), then **Data → Refresh All**.

---
⚠️ Notes & troubleshooting

Google Drive sometimes shows a confirmation/virus-check page for very large files; if the Web.Contents() approach returns an error, download the file manually and use Option A (place in /data/).

Pivot Tables store a pivot cache: the dashboard displays the last saved snapshot even if the raw file is missing. Users will only see refresh errors if they try to refresh without the raw data available or without updating DataPath.

If your current Power Query source is a hard-coded local path (e.g., C:\Users\You\...), consider switching to the DataPath parameter or relative path for easier sharing.

---
🙋‍♂️ About Me

I enjoy turning messy data into clear, actionable dashboards using tools available to most analysts — like Excel. This project is part of my work to build practical analytics that help teams make decisions faster.

📫 Let's connect
LinkedIn: [ Ashutosh Kumar Jalan](https://www.linkedin.com/in/ashutoshjalan-/)
