# Education Project: Analyzing the relationship between socioeconomic factors SAT scores, as well as looking into private school 

> The purpose of the Education project is to perform work using the data science methodology to answer the question of whether school performance is predicted by socioeconomic factors. Additionally, we will analyze if a school's Title I elegiblity status has an impact on ACT scores.

---

## Project Overview

We analyzed the impact of six socioeconomic factors on the results of ACT scores across the US. We measured unemployment rate, married family percentage, Percentage of parents with a college education or higher, percentage of schools with free or reduced lunch programs, median income, and a school’s Title I eligibility status.
Using exploratory data analysis methods and statistical regression models, we found that schools with free or reduced lunch programs had the strongest relationship of the six variables in their impact on ACT scores. Additionally, percent married, median income, and Title I were not statistically significant when tested in a multiple linear regression model.


- **Objective:** Answer the question of whether school performance is predicted by socioeconomic factors.
- **Domain:** (Education
- **Key Techniques:** Regrerssion, Exploratory Data Analysis.

---

## Project Structure

```
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
```

---

## Data

- **Source:** https://nces.ed.gov/programs/digest/d23/tables/dt23_205.10.asp, https://www.edgap.org, https://nces.ed.gov/ccd/elsi/tableGenerator.aspx
- **Description:** The data was imported into our notebook, and then merged, cleaned, and imputated the data of the EdGap and NCES data to serve our purposes of analyzing socioeconomic factors against SAT scores. Data Prep document: https://github.com/CameronMangione/education/blob/refs/heads/main/code/Education.ipynb.
Clean Data File (WIP): https://github.com/CameronMangione/education/blob/refs/heads/main/code/education_clean.csv.
- **License:** MIT License

Copyright (c) 2025 CameronMangione

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

## Analysis

Using a comprehensive pair plot that included all our variables helped us understand the key relationships between our variables. It answered the question of whether this data was worth analyzing in greater detail. 
Quality control involved ensuring that our data fell within the correct parameters, which included analyzing the details of our categorical variables, such as state data. Lastly, we imputed any missing data in our data frames and exported a clean dataset for our initial exploratory analysis.
For our exploratory data analysis, we used a heatmap and a comprehensive pair plot to visualize our key numerical predictor variables in the initial correlation data. 
Our modeling consisted of running a single-input model first, then pivoting to our multiple linear regression model, followed by a reduced model based on statistically significant socioeconomic factors, and finally a scaled reduced model to gain a better understanding of our coefficients.


---

## Results

Initially, our heatmap revealed the strongest correlation between our percentage of free/reduced lunch programs and ACT scores, with a correlation coefficient of -0.78. Our other four variables showed moderate correlations across the board. For our multiple linear regression model, we found that Title I, percent married, and median income did not show statistically significant results. 
The reduced model posted an R-squared value of 0.6185 and a mean absolute error of 1.1615, which was not a significant difference compared to the multiple linear regression results (0.6279 and 1.1455). The scaled model produced intriguing results, as we found that in a scaled model where the mean of the factors is 0 and the standard deviation is equal to 1, a change in the factor of free/reduced lunch correlated with a 1.177-point reduction in ACT scores. This relationship was the strongest of the three coefficients measured.


---

## Authors

- Cameron Mangione - [@CameronMangione](https://github.com/CameronMangione)

---

## License

MIT License

Copyright (c) 2025 CameronMangione

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


---

## Acknowledgements

- numpy, scikit, pandas (especially pandas), plotly, matplotlib, seaborn, wget, statsmodels
- Tutorials or papers referenced
- Inspiration or collaborators
