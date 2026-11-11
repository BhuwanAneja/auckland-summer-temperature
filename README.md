# Auckland Summer Temperature and Land Cover

How do land cover and urban development affect summer air temperature across Auckland?

## Data
104,181 grid locations across Auckland, with mean and maximum summer temperature, altitude, tree/grass/water/building/paved fractions and population density.

## Methods
- Mapped mean summer temperature across the region (ggplot2, viridis)
- **Regression trees** (rpart) to find the main drivers of mean and maximum temperature
- **Random forests** (ranger) with permutation variable importance and an 80/20 train/test split
- Linear regression to estimate the urban heat island effect and the effect of tree cover, controlling for altitude, water and buildings

## Findings
- Mean temperature ranged from 16.1°C to 19.8°C. **Altitude** was the strongest predictor of mean temperature, and **grass cover** of maximum temperature.
- Random forests predicted much better than single trees (test MSE about 0.052 for mean temperature).
- In urban areas, **more tree cover was linked to lower maximum temperatures**, after controlling for other land-cover factors.

## Tools
R, tidyverse, rpart, ranger, viridis

## Files
- `analysis.Rmd` – code
- `report.html` – full report
