# Data Cleaning Report

## Project Overview
This report documents the data cleaning process for a comprehensive movie dataset containing both static and dynamic data sources. The cleaning pipeline processes multiple CSV files related to movies, actors, studios, awards, and reviews to ensure data quality and consistency for downstream analysis.

## Project objectives
To understand which genres are most produced and most appreciated, and in which countries they are made.

## Dataset

### Static Data
- **Studios**: Production companies 
- **Actors**: Actor names and roles
- **Countries**: Geographic data
- **Crew**: Production crew members and their roles
- **Genres**: Genre
- **Languages**: Type and languages
- **Movies**: Core movie metadata including titles, dates, ratings
- **Posters**: Movie poster links and references
- **Releases**: Release information by country and type
- **Themes**: Movie themes and categories

### Dynamic Data
- **Oscar Awards**: Academy Awards data including winners and nominees
- **Rotten Tomatoes Reviews**: Movie reviews and ratings from critics

### Duplicate Records
Duplicate records were identified and removed from:
- Studios dataset
- Actors dataset
- Crew dataset
- Oscar Awards dataset
- Rotten Tomatoes Reviews dataset

## Data Standardization

### Country Code Normalization with method to_iso3
- Implemented ISO-3 country code standardization using the `pycountry` library
- Special handling for "UK" → "United Kingdom" conversion
- Rows with unrecognizable country names were removed

### Data Type Conversions in method clean_movie()
- Movie dates converted to numeric format with error handling
- Movie ratings converted to numeric format with error handling

## Cleaning Methodology

### Missing Value Strategy
1. **Critical Fields**: Rows with missing essential identifiers (names, links) were removed
2. **Optional Fields**: Missing values filled with "Unknown" placeholder
3. **Numeric Fields**: Converted to numeric with coercion for invalid values



### Data Validation
- Duplicate and removal across all datasets
- Empty string validation 
- Data type consistency checks

## Output Structure
All cleaned datasets are saved to `../data/cleaned/` directory with `_clean.csv` suffix:
- `studios_clean.csv`
- `actors_clean.csv`
- `countries_clean.csv`
- `genres_clean.csv`
- `languages_clean.csv`
- `crew_clean.csv`
- `movie_clean.csv`
- `posters_clean.csv`
- `releases_clean.csv`
- `themes_clean.csv`
- `the_oscar_awards_clean.csv`
- `rotten_tomatoes_reviews_clean.csv`

## Data Validation in method clean_posters
Implement additional validation for URL structures in poster links


## Data analysis

- Calculation of productions by decade and by genre.

- Identification of the 5 most produced genres.

- Calculation of the average grade assigned by the public for each gender.

- Identification of the 5 most popular genres.

- Visualization of geographic distribution via interactive choropleth maps.

## Technical Implementation
The cleaning pipeline is implemented in Joopiter Notebook using:
- **pandas**: Data manipulation and CSV processing
- **pycountry**: Country code standardization
- **matplotlib and seaborn** for static graphs
- **plotly** for interactive maps
- Modular function design for maintainability and reusability
