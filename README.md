# Healthcare-Data-Visualization
This project explores the key physiological, behavioral, and demographic factors associated with health risk levels (high vs. low) using a structured healthcare dataset. Through systematic data visualization techniques, the analysis identifies and interprets the determinants that distinguish individuals at elevated health risk from those at lower risk.

### Healthcare Data Visualization Project – Health Risk Factor Analysis

~ Overview :
The project follows a three-phase exploratory approach:
- **Univariate visualizations** to understand the distribution of each variable.
- **Bivariate visualizations** to identify relationships between pairs of variables.
- **Multivariate visualizations** to capture complex interactions among multiple factors simultaneously.
Three sampling methods were tested (simple random, systematic, and stratified sampling). Stratified sampling was selected as the optimal method because it preserves the original proportions of the `health_risk` target variable, ensuring representative and robust statistical comparisons.

## Objectives
- Identify major physiological risk factors (BMI, weight, age).
- Analyze the impact of behavioral risk factors (smoking, alcohol consumption, physical exercise, sleep duration).
- Examine sociodemographic variables (profession, marital status) in relation to health risk.
- Compare sampling methods and justify the choice of stratified sampling.
- Produce clear, interpretable visualizations to communicate findings effectively.

~ Key Findings :
#### Physiological Factors
- **BMI**: High-risk individuals show a BMI distribution shifted toward 30–35 (overweight/obese), while low-risk individuals cluster around 20–25.
- **Weight**: Median difference of ~20 kg between high-risk (~85 kg) and low-risk (~65 kg) groups.
- **Age**: High-risk group averages 53.8 years (~15 years older than the low-risk group).

#### Behavioral Factors (Paradoxical results suggesting confounding variables)
- **Smoking**: 96% of non-smokers are classified as high-risk vs. 64% of smokers.
- **Alcohol consumption**: 88% of non-drinkers are high-risk vs. 60% of drinkers.
- **Physical exercise**: Clear dose-response effect — 84.6% high-risk among those with no exercise, decreasing to 59.1% among those with high exercise levels.
- **Sleep**: Weak bivariate correlation, but multivariate analysis reveals interactions with exercise and sugar consumption.

#### Occupational & Social Factors
- Highest-risk professions: drivers (78.7%), students (73.8%), teachers (70.4%).
- Married individuals show a marginally higher risk (68% vs. 60% for non-married), likely confounded by age.

#### Multivariate Interactions
- Moderate exercise level optimizes the relationship between sleep and BMI.
- Low sugar intake improves separation between risk groups and reveals a positive sleep-BMI correlation in the low-risk group.

~ Limitations :
- Categorical variable definitions (e.g., exercise levels, sugar intake) are not explicitly detailed.
- The dataset is cross-sectional, preventing causal inference.
- Only sleep duration is measured, not sleep quality or disorders (e.g., apnea, insomnia).
- The apparent imbalance between risk groups in some visualizations may affect interpretation.

## Repository Structure
- `README.md` : Project overview, objectives, key findings, and limitations
- `data/` : Contains the dataset `Lifestyle_and_Health_Risk_Prediction.csv`
- `notebooks/` : Contains the Jupyter Notebook with all code (data import, sampling, visualizations)
- `images/` : Contains all generated visualizations (PNG files): BMI distribution, age comparison, alcohol/smoking/exercise charts, correlation matrix, faceted plots, etc..
- `requirements.txt` : List of Python dependencies required to run the notebook
- `.gitignore` : Specifies intentionally untracked files to ignore 
