# STA304 Study on Study Habits and Academic Performance

This repository contains code and data files for a study conducted in the STA304 course. The research aims to examine the relationship between study habits and academic performance among students, specifically analyzing how study hours, study preferences, preview frequency, and demographic factors (gender, major, student status, and employment status) relate to GPA.

## Project Overview

The main objective of this study was to explore which factors in students' study habits contribute to better academic outcomes. The key research questions included:
1. Is there a significant association between study hours and GPA?
2. Does study preference (group vs. individual) affect GPA?
3. Is preview frequency associated with GPA?
4. Are demographic factors such as gender, major, student status, and employment status associated with GPA?

## Files in this Repository

- `STA304H5 Group 4 Dataset.xlsx`: The dataset containing responses from students, including variables such as GPA, study hours, preview frequency, and demographic information.
- `codebook.pdf`: Documentation of each variable in the dataset, including labels and codes used.
- `report_draft.pdf`: Draft of the final report with detailed analysis, results, and conclusions.
- `analysis_script.R`: R script containing the analysis code used to answer the research questions and generate key statistics.

## Methodology

1. **Population and Sampling**: The population for this study consisted of 240 students. Data was collected from 97 participants, with 4 responses removed as invalid. A simple random sample (SRS) of 50 responses was selected for analysis.
   
2. **Sample Size Calculation**: The sample size was calculated using the following formula, focusing on a bound error of 0.13:

   $$
   \frac{{Npq}}{{(N - 1)D + pq}} = \frac{{(240)(0.5)(0.5)}}{{(239)(0.13^2) + (0.5)(0.5)}} \approx 50
   $$

3. **Statistical Analysis**:
   - **RQ1**: Pearson correlation was used to test the association between study hours and GPA.
   - **RQ2**: An independent t-test examined the effect of study preference (group vs. individual) on GPA.
   - **RQ3**: An ordinal logistic regression tested the association between preview frequency and GPA.
   - **RQ4**: ANOVA tested the effect of demographic factors on GPA.

## Key Findings

- **Study Hours and GPA**: No significant correlation was found between study hours and GPA (p = 0.3426).
- **Study Preference and GPA**: No significant difference in GPA was observed based on study preference (p = 0.6778).
- **Preview Frequency and GPA**: A significant negative association was found for students who reported previewing "never to rarely" (p = 0.0328), suggesting a minimal level of previewing benefits GPA.
- **Demographic Factors and GPA**: No significant associations were found between GPA and demographic factors, with p-values as follows:
  - Gender: p = 0.309
  - Student Status: p = 0.335
  - Major: p = 0.214
  - Employment Status: p = 0.494

## Requirements

The analysis scripts require the following R packages:
- `tidyverse`
- `car`
- `readxl`
- `ggplot2`
- `MASS`
- `knitr`

## How to Run the Analysis

1. **Load the Dataset**: Ensure `STA304H5 Group 4 Dataset.xlsx` is in the working directory.
2. **Run `analysis_script.R`**: Execute the R script to reproduce the analysis, generate tables, and create visualizations.
3. **Check Output**: The script will output key descriptive statistics and statistical test results.

## Limitations

- **Sample Size**: With a sample size of 50, the findings may not generalize to the entire student population.
- **Assumption Violations in Statistical Tests**: Some statistical tests in our analysis assume normality and homogeneity of variances, con-ditions which were not fully met, particularly regarding the normality of GPA distributionsacross groups.
- **Omitted Confounding Variables**: Our survey focused on study habits and academic performance, but it did not account forpotential confounding factors such as extracurricular activities, study environments, or accessto academic resources. These factors could influence both study habits and GPA, introducingpotential bias in our findings.

## Conclusion

This study underscores the potential benefits of previewing course materials on academic performance, while study hours, preference, and demographic factors showed limited impact on GPA. Future research should explore larger and more diverse samples to confirm these findings.
