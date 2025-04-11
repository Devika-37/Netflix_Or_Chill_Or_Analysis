# Netflix_Or_Chill_Or_Analysis

This project performs data cleaning and preprocessing on the Netflix Titles dataset to prepare it for visualization in **Tableau**. The processed data is exported as a CSV file, which can be directly used for creating insightful dashboards.

## 📌 Steps Performed in Python

1. **Drop Duplicate Entries**  
   Removes any repeated rows in the dataset to ensure uniqueness.

2. **Drop Rows with Null Values**  
   Eliminates rows that contain any missing (null) values for cleaner analysis.

3. **Clean 'country' Column**  
   - Extracts only the first country name if multiple are listed (i.e., the name before the comma).
   - Replaces the existing `country` column with the cleaned one.

4. **Split 'listed_in' (Genres) into Separate Columns**  
   - The `listed_in` column contains comma-separated genres.
   - Each genre is split into a separate column (e.g., `genre_1`, `genre_2`, ...).
   - Null columns formed due to missing genres are dropped.

5. **Save the Cleaned Dataset**  
   The final cleaned dataset is saved as `cleaned_netflix_titles.csv`.

## 📊 Usage in Tableau

The cleaned data is used to build a dynamic and interactive dashboard in Tableau with the following visualizations:

### 🔍 Visualizations

1. **Release Year vs Genre**  
   - Shows the distribution of different genres over the years.
   - Helps identify trends in content production.

2. **Country-Based Interactivity**  
   - Click on a country to filter the dashboard.
   - Displays genre counts and their variations over time for the selected country.

### ✅ Benefits

- Improved data consistency and clarity.
- Easier comparison across countries and genres.
- Interactive and visually appealing analytics through Tableau.

## 📁 Output File

- `cleaned_netflix_titles.csv` — cleaned and transformed dataset for Tableau analysis.

---

### Run the Python Script

Make sure you have the original `netflix_titles.csv` in the same directory and run:

```bash
python clean_netflix_data.py
