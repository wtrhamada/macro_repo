# macro_repo

## About this repository
This repository contains programs to calculate business cycles and programs to calculate growth accounting.

This repository has two program files,

  - macro_report_business_cycle.m

  - macro_report_growth_accounting.ipynb

### 1. macro_report_business_cycle
This file is coded by Matlab.

We obtain GDP data for Germany and Japan for 1994-2022 from [FRED](https://fred.stlouisfed.org), apply the HP filter, and plot *the cyclical variation components on a time-series graph*.

We also calculate *the standard deviation of the cyclical components** for each of Germany and Japan, and **the correlation coefficient between the cyclical components* for Germany and Japan.


### 2. macro_report_growth_accounting.ipynb
This file is coded by Python.

We get data from [Penn World Table](https://www.rug.nl/ggdc/productivity/pwt/?lang=en), and decompose labor productivity growth into TFP and Capital deepening. The countries targeted are Canada, France, Germany, Italy, Japan, the United Kingdom, and the United States.

Finally, we output *the growth rate of labor productivity, the rate of change in TFP and Capital deepening*, and *the contribution of TFP and Capital deepening* for each country in table format.

However, there are two definitions of "L," one is using "emp" only, and the other is using the value of "emp*avh". In addition, alpha should be included in the differential equation because it is time series data, but the results are quite strange, so I calculated the case where alpha is not included in the equation.
In this file, only emp is used for L, and alpha is included in the differential equation.

For reference, here are the results of the output with different definitions of L and different treatment of alpha.

![Output results for different definitions of L and different treatment of alpha](https://github.com/wtrhamada/macro_repo/blob/610854ceb2dfa12058406b74eb0c16fc2534615a/Comparison.png)

## Change Log

### 2023/06/11
- in ipynb file, changed the calculation method of Average of TFP Share and Capital Share in the output table. The average of Growth Rate, TFP Growth, and Capital Deepening is now used in the calculation.

- in ipynb file, deleted the extra cells and code.

- apploaded "Comparison.png"

### 2023/06/10
- in ipynb file, column "L" of data frame "data" was calculated by emp * avh, but only the value of emp is used instead.

### 2023/06/08
- in ipynb file, added a new row of output for the average values per column.

### 2023/06/06
- created "README.md".

- in ipynb file, added the column "alpha_x_ln_k" to the data frame "data" to put the alpha in diff().

### 2023/06/05
- apploaded "macro_report_business_cycle.m"

- apploaded "macro_report_growth_accounting.ipynb"
