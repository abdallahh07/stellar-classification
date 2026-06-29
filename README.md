# Predicting Stellar Class | Kaggle Competition

Multi-class classification predicting stellar object type (Galaxy, Star, QSO) from astronomical measurements.

## Competition Result

- **Competition:** Kaggle Playground Series Season 6 Episode 6
- **Public Score:** 0.96517 (Balanced Accuracy)
- **Leaderboard Rank:** 1203 / 2,666 teams (Top 45%)
- **Submissions:** 1

## Approach

- Feature engineering: color indices (u-g, g-r, r-i, i-z, u-z) from photometric filters
- Model: LightGBM with class_weight='balanced'
- Metric: Balanced Accuracy (handles class imbalance across 3 classes)

## Dataset

- 577,347 training rows, 247,435 test rows
- 3 classes: GALAXY (65.4%), QSO (20.3%), STAR (14.3%)
- Key feature: redshift — almost perfectly separates QSOs from stars and galaxies

## Key Features

| Feature                 | Description                                                       |
| ----------------------- | ----------------------------------------------------------------- |
| redshift                | Most powerful feature — separates QSO from GALAXY and STAR        |
| u_g, g_r, r_i, i_z, u_z | Color indices — brightness differences between wavelength filters |
| spectral_type           | Star spectrum classification                                      |
| galaxy_population       | Galaxy population type                                            |

## Project Structure

stellarclass_model/

├── config/

├── processing/

├── trained_models/

├── pipeline.py

train_pipeline.py

predict.py

research.ipynb
