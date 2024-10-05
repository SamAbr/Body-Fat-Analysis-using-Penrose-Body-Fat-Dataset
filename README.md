# Body Fat Analysis using Penrose Body Fat Dataset

## Overview

This project analyzes the Penrose body fat dataset, which includes physiological measurements related to 252 men. The primary objective is to investigate the correlation between body fat percentage and various physical attributes such as age, weight, and body circumferences. The dataset contains **252 observations** and **14 variables**.

### Dataset Variables

- **Bodyfat**: Percentage of body fat obtained through underwater weighing.
- **age**: Age in years/100.
- **weight**: Weight in lbs/100.
- **height**: Height in inches/100.
- **neck**: Neck circumference in cm/100.
- **chest**: Chest circumference in cm/100.
- **abdomen**: Abdomen circumference in cm/100.
- **hip**: Hip circumference in cm/100.
- **thigh**: Thigh circumference in cm/100.
- **knee**: Knee circumference in cm/100.
- **ankle**: Ankle circumference in cm/100.
- **biceps**: Biceps circumference in cm/100.
- **forearm**: Forearm circumference in cm/100.
- **wrist**: Wrist circumference in cm/100.

## Installation

To run this analysis, ensure you have R and the following libraries installed:

- `tidyverse`
- `psych`
- `bbreg`
- `plotly`

You can install the required packages using the following command in R:

```r
install.packages(c("tidyverse", "psych", "bbreg", "plotly"))
```

## Usage

1. Load the necessary libraries:
   ```r
   library(tidyverse)
   library(psych)
   library(bbreg)
   library(plotly)
   ```

2. Load the Penrose body fat dataset:
   ```r
   data(BF)
   ```

3. Perform correlation analysis between body fat percentage and other variables.

4. Generate scatter plots to visualize relationships and trends.

5. Conduct regression analysis using the most significant predictor variable, which is `abdomen` in this case.

### Examples

Calculate the correlation between body fat and various measurements:
```r
# Correlation between age and body fat
cor.test(BF$age, BF$bodyfat)
```

Create a scatter plot for weight and body fat:
```r
# Scatter plot for weight and body fat
plot_ly(x = ~BF$weight, y = ~BF$bodyfat) %>%
  add_markers()
```

## Results

- The analysis shows varying degrees of correlation between body fat percentage and physiological measurements. The variable with the strongest correlation to body fat is **abdomen circumference**.
- All significant correlations have been identified and visualized using scatter plots.
- A linear regression model is also fitted to predict body fat percentage using abdomen circumference.

## Files included

1. Body_Fat_Analysis_using_Penrose_Body_Fat_Dataset.Rmd: RMarkdown file containing the code and analysis for the body fat percentage project.
2. Body_Fat_Analysis_using_Penrose_Body_Fat_Dataset.html: HTML output of the analysis, generated from the RMarkdown file.

## Conclusion

This project provides insights into how body measurements correlate with body fat percentage. It emphasizes the importance of abdomen circumference as a predictor of body fat and illustrates the use of correlation and regression analysis in physiological data interpretation.

## Author

**Samuel Abrha Gebremariam**

Date: June 4, 2024
