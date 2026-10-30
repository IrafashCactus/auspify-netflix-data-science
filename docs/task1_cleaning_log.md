# Task 1: Data Cleaning Log

Raw: 8,790 rows x 10 columns. Clean: 8,786 rows x 17 columns.

| # | Issue | Evidence | Decision | Result |
|---|-------|----------|----------|--------|
| 1 | Hidden missing values | "Not Given": 2,588 director, 287 country | Replaced with "Unknown" | 0 placeholders left |
| 2 | Exact duplicates | 3 pairs identical except show_id | Kept first copy | 8,787 rows |
| 3 | Date-like titles | 5 matches (9-Feb, 15-Aug, 22-Jul, SPF-18, 1-Oct) | Kept, documented as limitation | Unchanged |
| 4 | Wrong data types | date_added and duration stored as text | Converted date (%m/%d/%Y); split duration into value and unit | datetime64, int64 |
| 5 | Added before release | 14 titles (12 TV shows) | Flagged, not removed | added_before_release |
| 6 | Text inconsistencies | 2 director spellings, UR and NR, 1 padded title | Standardised | 13 ratings |
| 7 | Exact duplicate after trimming | Consequences (s6530) | Removed | 8,786 rows |
| 8 | Near-duplicate titles | 3 pairs differ in date_added | Kept all six rows | Unchanged |
| 9 | Multi-value genres | listed_in holds 1 to 3 genres | Added main_genre, n_genres | New columns |

Removed rows are stored in data/processed/removed_duplicates.csv.