# Task 4: Trend Prediction Analysis

Input: data/processed/netflix_clean.csv. Notebook: notebooks/04_trend_prediction.ipynb.
Evidence: evidence/task_4/.

| Step | Method | Result |
|------|--------|--------|
| Prepare release-year data | Counts per release_year | 74 years present (1925 to 2021), 23 empty years; 525 titles up to 1999, 8,261 from 2000 |
| Analyze trends | Titles per year and type, year-over-year change | Peak 1,144 in 2018; jumps of +58.1% (2015) and +62.3% (2016) |
| Build models | Naive, linear, exponential; trained 2000 to 2015, tested 2016 to 2018 | Average error 470, 617, 439 titles |
| Visualize | Refit on 2000 to 2018, scenarios for 2019 to 2023 | Linear +52 titles/year; exponential about +21%/year |
| Interpret | Compared with observed 2019 to 2021 | Observed 1,029, 953, 592; neither model tracks consistently |

## Decisions
- Modelling window 2000 to 2018: earlier years are sparse with gaps; 2019 to 2021 may be incomplete.
- Time-based split (no random split), because forecasting predicts later years from earlier ones.
- Results presented as scenarios, not predictions.

## Limitations
- Only 3 test years, so the model ranking is uncertain.
- Catalogue of titles, not worldwide production.
- Data ends 25 September 2021; the fall from 2019 may be a data artefact.
