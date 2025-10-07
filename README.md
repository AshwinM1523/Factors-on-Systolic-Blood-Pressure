# Systolic Blood Pressure Analysis

A statistical case study examining the influence of lifestyle and demographic factors on Systolic Blood Pressure (SBP) using data from 500 patients.

## Overview

This research employs statistical modeling and inference to identify significant predictors of SBP, a critical cardiovascular health marker. The analysis explores relationships between SBP and various factors including age, weight, height, BMI, race, lifestyle choices (smoking, exercise, alcohol consumption), and treatment history.

## Authors

- Adam Badar
- Ashwin Mallik
- Alex Zeng
- Francis Ayyad

## Project Structure

- `FinalProject.Rmd` - R Markdown source file containing the complete analysis
- `FinalProject.pdf` - Compiled report with findings and visualizations
- `BloodPressure.xlsx` - Dataset containing patient measurements and lifestyle factors (not included in repository)

## Key Findings

### Significant Predictors
- **Weight, Height, and BMI**: Strong linear relationships with SBP
- **Race**: Significant genetic influence on SBP variation
- **Treatment for Hypertension**: High predictive power
- **Age**: No significant linear relationship when analyzed independently

### Model Performance
The study compared two statistical models:
1. **Main Effect Model**: Baseline model with no interaction terms
2. **Interaction Model**: Superior performance across all metrics (adjusted R², AIC, BIC, PRESS)

The interaction model demonstrated that accounting for interactions between continuous variables (weight, height, age) and categorical variables (race, smoking, exercise, etc.) significantly improves predictive accuracy.

## Methodology

1. **Exploratory Data Analysis**
   - Distribution analysis of continuous variables (age, weight, height, BMI)
   - Categorical variable impact assessment
   - Correlation analysis and multicollinearity detection

2. **Model Building**
   - Main effect model construction
   - Interaction model with cross-terms
   - Backward elimination using AIC criterion
   - Model selection based on multiple criteria

3. **Model Diagnostics**
   - Outlier detection using Cook's Distance
   - Normality assessment via Q-Q plots
   - Homoscedasticity verification

4. **Validation**
   - 70/30 training-testing split
   - Cross-validation performance assessment

## Technologies Used

- **R** - Statistical computing and graphics
- **RMarkdown** - Reproducible research document generation
- **Key R Libraries**:
  - `ggplot2` - Data visualization
  - `gridExtra` - Plot arrangement
  - `corrplot` - Correlation visualization
  - `car` - Regression diagnostics
  - `readxl` - Data import

## Requirements

```r
install.packages(c("ggplot2", "gridExtra", "corrplot", "car", "readxl"))
```

## Usage

To reproduce the analysis:

1. Ensure you have R and RStudio installed
2. Install required packages
3. Place the `BloodPressure.xlsx` dataset in the project directory
4. Open `FinalProject.Rmd` in RStudio
5. Click "Knit" to generate the PDF report

## Limitations

- Model validation showed prediction error (SE ~35 on test set vs ~20 on training)
- Limited generalizability to other populations
- Relatively low R² values indicate additional unmeasured factors may influence SBP
- Sample restricted to 500 patients

## Future Research Directions

- Incorporation of genetic markers and environmental exposures
- Longitudinal studies to track SBP changes over time
- Exploration of psychosocial stressors and their interactions
- Multi-center studies with diverse demographic groups
- Investigation of medication-specific effects on SBP

## Clinical Implications

This study provides a framework for:
- Personalized cardiovascular risk assessment
- Targeted intervention strategies based on race and lifestyle factors
- Evidence-based weight management and lifestyle modification programs
- Enhanced screening protocols for high-risk populations

## References

Theodore, R. F., et al. (2015). Childhood to Early-Midlife Systolic Blood Pressure Trajectories. *Hypertension*, 66(6), 1108–1115.

Cené, C. W., et al. (2009). The Effect of Patient Race and Blood Pressure Control on Patient-Physician Communication. *Journal of General Internal Medicine*, 24(9), 1057–1064.

## License

This project was completed as part of academic coursework (April 2024).