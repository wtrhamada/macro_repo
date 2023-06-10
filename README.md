# macro_repo

## About this repository
This repository contains programs to calculate business cycles and programs to calculate growth accounting.

This repository has three files,

  README.md

  macro_report_business_cycle.m

  macro_report_growth_accounting.ipynb

### 1. README.md
This file.

### 2. macro_report_business_cycle
This file is coded by Matlab.

We obtain GDP data for Germany and Japan for 1994-2022 from FRED (https://fred.stlouisfed.org), apply the HP filter, and plot **the cyclical variation components on a time-series graph**.

We also calculate **the standard deviation of the cyclical components** for each of Germany and Japan, and **the correlation coefficient between the cyclical components** for Germany and Japan.


### 3. macro_report_growth_accounting.ipynb
This file is coded by Python.

We get data from Penn World Table (https://www.rug.nl/ggdc/productivity/pwt/?lang=en), and decompose labor productivity growth into TFP and Capital deepening. The countries targeted are Canada, France, Germany, Italy, Japan, the United Kingdom, and the United States.

Finally, we output **the growth rate of labor productivity, the rate of change in TFP and Capital deepening**, and **the contribution of TFP and Capital deepening** for each country in table format.


## Change Log

### 2023/06/10
in ipynb file, column "L" of data frame "data" was calculated by emp * avh, but only the value of emp is used instead.

### 2023/06/08
in ipynb file, added a new row of output for the average values per column.

### 2023/06/06
created "README.md".

in ipynb file, added the column "alpha_x_ln_k" to the data frame "data" to put the alpha in diff().

### 2023/06/05
apploaded "macro_report_business_cycle.m"

apploaded "macro_report_growth_accounting.ipynb"
