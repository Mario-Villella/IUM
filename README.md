# IUM
# 🎬 Movie Dataset Analysis & Data Cleaning

## 📌 Project Overview
Data analysis project developed to explore trends in the global movie market. The main objective is to identify which movie genres are most produced and most appreciated by the public, while also analyzing their geographic distribution. The project includes a robust data cleaning pipeline and the generation of interactive visualizations.

## 📊 Dataset & Download
The project uses a comprehensive dataset consisting of static data (movie metadata, actors, studios, genres) and dynamic data (Rotten Tomatoes reviews, Oscar nominations and awards).

> ⚠️ **Data Note:** To keep the repository lightweight, the original CSV files are not tracked on GitHub. 
> **[Download the full dataset here](https://drive.google.com/drive/folders/1LZokTM5jA-Ut71Deg_7fPAIig5tlvbEl?usp=drive_link)**.
> Once downloaded, place the raw files in the `data/raw/` folder before running the notebook. Executing the pipeline will generate the processed files (e.g., `movie_clean.csv`) directly in the `data/cleaned/` directory.

## 🛠 Technologies Used
*   **Environment:** Jupyter Notebook
*   **Data Processing:** `pandas`, `pycountry` (for ISO-3 country code normalization)
*   **Data Visualization:** `matplotlib` and `seaborn` (static charts), `plotly` (interactive choropleth maps)

## 🚀 Key Features (Data Analysis)
*   **Temporal Analysis:** Calculation of movie production volume broken down by decade and genre.
*   **Popularity Trends:** Identification of the top 5 most produced genres overall and the top 5 highest-rated genres by the public.
*   **Geographic Distribution:** Global mapping of movie productions using interactive Choropleth maps.

## 📄 Technical Documentation (Report)
For in-depth technical details regarding data cleaning strategies, missing value handling, applied validations (e.g., `to_iso3`, `clean_movie()`, `clean_posters()` methods), and the exact output file structure, please refer to the attached **[Data Cleaning Report](docs/Data_Cleaning_Report.pdf)**.
