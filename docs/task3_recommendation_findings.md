# Task 3: Recommendation System

Input: data/processed/netflix_clean.csv. Notebook: notebooks/03_recommendation_system.ipynb.
Evidence: evidence/task_3/.

| Step | Method | Result |
|------|--------|--------|
| Extract features | type, rating, genres, director, country joined as tokens; Unknown left out | 4 to 18 tokens per title (mean about 6) |
| Preprocess text | punctuation removed, lowercase, multi-word labels kept as one token | 5,127 distinct tokens |
| Similarity | TF-IDF + cosine similarity, one title at a time | matrix (8,786, 5,127) |
| Recommend | top 5, same-title matches excluded | e.g. Motu Patlu titles 1.0 to 0.92 |
| Evaluate | 300 random titles vs 5 random picks | same type 0.933 (random 0.595); shares genre 0.899 (random 0.241) |

## Limitations
- No description column, so only metadata is matched.
- Evaluation is circular: the features include type and genres.
- Many ties in scores; director names can outweigh type.