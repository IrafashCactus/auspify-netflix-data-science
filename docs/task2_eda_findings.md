# Task 2: Exploratory Data Analysis

Input: data/processed/netflix_clean.csv (8,786 titles, 17 columns).
Notebook: notebooks/02_eda.ipynb. Evidence: evidence/task_2/.

| Question | Method | Result |
|----------|--------|--------|
| Dataset structure | describe() | Release years 1925 to 2021 (median 2017); added 2008 to 2021 |
| Content by type | value_counts, countplot | 6,123 movies (69.7%), 2,663 TV shows (30.3%) |
| Top countries | Unknown excluded (287); 8,499 titles remain | US 3,240 (38.1%), India 1,056 (12.4%), UK 638 (7.5%) |
| Top genres | listed_in split into every genre (19,284 mentions) | International Movies 2,751, Dramas 2,423, Comedies 1,673 |
| Ratings | value_counts | TV-MA 3,204 (36.5%), TV-14 2,155 (24.5%) |
| Growth | titles per year_added, by type | 2019 peak (2,013); 98.4% added from 2016; 2021 partial |

## Decisions carried over from Task 1
- "Unknown" is excluded from country and director rankings.
- 2021 is a partial year (data ends 25 September 2021).
- Genre shares can exceed 100% because a title carries up to 3 genres.

## Limitations
- The file lists the catalogue only: no viewing numbers, no removed titles.
- Ratings mix US TV and film systems; NC-17 (3) and TV-Y7-FV (6) are too small to interpret.
- International Movies / TV Shows describe origin or language, not story genre.
