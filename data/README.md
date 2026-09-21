# Course data

This directory contains the datasets vendored for the released GB656 problem-set
templates and preparatory labs. Most notebooks first look for a local file in this
directory and otherwise load the same course copy from the public GitHub repository.
Two releases instead use pinned external sources: the Problem Set 3 lab loads
customer-churn data from IBM, and the Module 7 notebooks load synthetic patient-year
data from the Dissecting Bias project. Neither external dataset is vendored here.

## Dataset catalog

| File | Released materials | Upstream terms |
|---|---|---|
| `car_price_prediction.csv` | Problem Set 1 and its lab | MIT declaration in the upstream dataset card |
| `SeoulBikeData.csv` | Problem Set 2, its lab, and the Problem Set 5 lab | Creative Commons Attribution 4.0 International |
| `UCI_Credit_Card.csv` | Problem Set 3 | Creative Commons Attribution 4.0 International |
| `WA_Fn-UseC_-Telco-Customer-Churn.csv` (external only) | Problem Set 3 lab | Not vendored; loaded from a pinned IBM source |
| `insurance.csv` | Problem Set 4 | Public-domain declaration in the upstream repository |
| `auto-mpg.csv` | Problem Set 4 lab | Creative Commons Attribution 4.0 International |
| `residential_building.csv` | Problem Set 5 | Creative Commons Attribution 4.0 International |
| `data_new.csv` (external only) | Module 7 application notebooks and solutions | No explicit upstream license identified; not vendored |

## `car_price_prediction.csv`

This is a **synthetic teaching dataset**, not a collection of observed used-car
listings. It contains 1,000 simulated cars and eight variables.

| Column | Description |
|---|---|
| `Make` | Randomly assigned vehicle manufacturer label |
| `Model` | Randomly assigned generic model label |
| `Year` | Model year, from 2000 through 2021 |
| `Engine Size` | Simulated engine-size value |
| `Mileage` | Simulated odometer mileage; interpreted as miles in the course |
| `Fuel Type` | Randomly assigned fuel-type label |
| `Transmission` | Randomly assigned transmission label |
| `Price` | Simulated price; interpreted as dollars in the course |

### Source and course copy

- Upstream repository: [`Vishaltiwari2019/Car-Price-Prediction`](https://huggingface.co/datasets/Vishaltiwari2019/Car-Price-Prediction)
- Upstream filename: `Car_Price_Prediction.csv`
- Earliest verified public upload: [commit `ff4fc9620f5003fb981627dec1804c59f6e268b7`](https://huggingface.co/datasets/Vishaltiwari2019/Car-Price-Prediction/commit/ff4fc9620f5003fb981627dec1804c59f6e268b7), September 28, 2024
- Course transformation: filename changed to `car_price_prediction.csv`; the file
  contents are otherwise byte-for-byte identical to the upstream CSV
- SHA-256: `4f033c25944a3455572c9a7dde8ff3c6e3135c8bf9ca360aae9b2eb311b0e45c`

The upstream dataset-card metadata declares the dataset license as MIT. The upstream
repository does not provide a separate license file or copyright notice, so this
page records the upstream declaration and does not claim ownership of the dataset.
This course copy remains subject to the dataset's upstream terms.

### Synthetic-data notes

An exact reconstruction of the file is consistent with:

```text
Price = 30,000 - 500*(2022 - Year) + 2,000*(Engine Size)
        - 0.05*Mileage + epsilon,
epsilon ~ Normal(0, 2,000^2).
```

The assignments therefore use 2022 as the valuation/reference year and define
`car_age = 2022 - Year`. The resulting ages range from 1 through 22 years. The
upstream uploader does not document the measurement units, generating code, or an
earlier source; dollar and mile interpretations are course conventions.

## `SeoulBikeData.csv`

This observed dataset contains 8,760 hourly records and 14 columns describing
rented-bike counts, time, weather, season, holiday status, and whether the Seoul
bike-sharing system was functioning.

### Source and course copy

- Publisher and repository: [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/560/seoul+bike+sharing+demand)
- UCI dataset DOI: [`10.24432/C5F62R`](https://doi.org/10.24432/C5F62R)
- UCI citation: *Seoul Bike Sharing Demand* [Dataset] (2020), UCI Machine
  Learning Repository
- Upstream filename: `SeoulBikeData.csv`, distributed in the official
  [dataset archive](https://archive.ics.uci.edu/static/public/560/seoul+bike+sharing+demand.zip)
- Course transformation: none; this course copy is byte-for-byte identical to the
  CSV extracted from the upstream archive
- Text encoding: Latin-1
- SHA-256: `373339b71a8935d69e9af0abf26a70744632119862eeb3919efb389a7b749c60`
- Released course use: `problem-sets/03-02-template.ipynb`,
  `problem-sets/lab-lectures/03-02-lab.ipynb`, and
  `problem-sets/lab-lectures/06-05-lab.ipynb`

UCI distributes this dataset under the
[Creative Commons Attribution 4.0 International license](https://creativecommons.org/licenses/by/4.0/).
That license permits sharing and adaptation with appropriate attribution. This
course copy remains subject to the dataset's upstream license.

## `UCI_Credit_Card.csv`

This observed dataset contains 30,000 credit-card client records and 25 columns.
It records demographic attributes, credit limits, repayment status, bill amounts,
payment amounts, and whether each client defaulted in the following month.

### Source and course copy

- Creator: I-Cheng Yeh
- Publisher and original source: [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients)
- UCI dataset DOI: [`10.24432/C55S3H`](https://doi.org/10.24432/C55S3H)
- UCI citation: Yeh, I. (2009), *Default of Credit Card Clients* [Dataset],
  UCI Machine Learning Repository
- CSV mirror: [`scikit-learn/credit-card-clients`](https://huggingface.co/datasets/scikit-learn/credit-card-clients/blob/f809522649eaf948ad40a11ed575c4bb4d4460c1/UCI_Credit_Card.csv)
- Course transformation: none; this course copy is byte-for-byte identical to the
  CSV at mirror commit `f809522649eaf948ad40a11ed575c4bb4d4460c1`
- Shape: 30,000 rows and 25 columns
- SHA-256: `a0f0ab49d6326671d6cd83be5c88dcf18007025fe9a53ecd699119c871176ca1`
- Released course use: `problem-sets/04-03-template.ipynb`

UCI distributes the original dataset under the
[Creative Commons Attribution 4.0 International license](https://creativecommons.org/licenses/by/4.0/).
That license permits sharing and adaptation with appropriate attribution. This
course copy remains subject to the dataset's upstream license.

## `WA_Fn-UseC_-Telco-Customer-Churn.csv` (external only)

The Problem Set 3 lab uses a fictional IBM telecommunications sample containing
7,043 customer records and 21 columns. The fields describe demographics, services,
account terms, charges, and whether the customer churned. The raw `TotalCharges`
column contains 11 blank values, which the lab identifies and handles explicitly.

### Pinned source used by the lab

- Publisher and repository: [IBM, `telco-customer-churn-on-icp4d`](https://github.com/IBM/telco-customer-churn-on-icp4d)
- Pinned source file: [`Telco-Customer-Churn.csv`](https://raw.githubusercontent.com/IBM/telco-customer-churn-on-icp4d/d5371f5d83a446ad5673cbcca3b814b926491f8a/data/Telco-Customer-Churn.csv)
- Pinned commit: `d5371f5d83a446ad5673cbcca3b814b926491f8a`
- Shape: 7,043 rows and 21 columns
- SHA-256: `16320c9c1ec72448db59aa0a26a0b95401046bef5d02fd3aeb906448e3055e91`
- Course transformation: none to the downloaded file; the lab performs its cleaning
  and feature preparation in memory
- Released course use: `problem-sets/lab-lectures/04-03-lab.ipynb`

The IBM repository includes an Apache License 2.0 file, but the dataset's provenance
and redistribution status are not stated clearly enough to justify placing another
copy in this repository. The lab therefore reads the exact pinned IBM file directly;
no `WA_Fn-UseC_-Telco-Customer-Churn.csv` file is vendored here.

## `insurance.csv`

This synthetic teaching dataset contains 1,338 insurance records and seven columns:
age, sex, body mass index, number of children, smoking status, region, and annual
medical charges. It was created for Brett Lantz's *Machine Learning with R* using
demographic characteristics based on U.S. Census data.

### Source and course copy

- Upstream repository: [`stedy/Machine-Learning-with-R-datasets`](https://github.com/stedy/Machine-Learning-with-R-datasets)
- Pinned upstream file: [`insurance.csv`](https://raw.githubusercontent.com/stedy/Machine-Learning-with-R-datasets/ff933238d9c30da179b7e3ad4b6ca938d67efc53/insurance.csv)
- Pinned commit: `ff933238d9c30da179b7e3ad4b6ca938d67efc53`
- Course transformation: none; this course copy is byte-for-byte identical to the
  pinned upstream CSV
- Shape: 1,338 rows and 7 columns
- SHA-256: `505c1cbc2e63d0363bac59501563df2530aadf4cdb9cfee226f4ef32f5468281`
- Released course use: `problem-sets/05-04-template.ipynb`

The upstream repository declares its datasets to be in the public domain but does
not provide a separate license file. This page records that upstream declaration
and does not claim ownership of the dataset.

## `auto-mpg.csv`

This observed dataset contains 398 vehicle records and nine columns describing fuel
economy, engine and vehicle characteristics, model year, origin, and car name. Six
records use `?` as the missing-value code for horsepower; the lab handles those rows
explicitly.

### Source and course copy

- Creator: R. Quinlan
- Publisher and original source: [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/9/auto+mpg)
- UCI dataset DOI: [`10.24432/C5859H`](https://doi.org/10.24432/C5859H)
- UCI citation: Quinlan, R. (1993), *Auto MPG* [Dataset], UCI Machine
  Learning Repository
- Upstream data file: `auto-mpg.data`
- Course transformation: parsed the whitespace-delimited UCI data into nine named
  CSV columns and added a header row; all source values and all 398 records were
  preserved
- Shape: 398 rows and 9 columns
- SHA-256: `09a282cf12c7ab4ffb517b496b0dd1a8bac6e95977178cc7832c32044c32c3f6`
- Released course use: `problem-sets/lab-lectures/05-04-lab.ipynb`

UCI distributes this dataset under the
[Creative Commons Attribution 4.0 International license](https://creativecommons.org/licenses/by/4.0/).
That license permits sharing and adaptation with appropriate attribution. This
course copy remains subject to the dataset's upstream license.

## `residential_building.csv`

This observed dataset contains 372 residential-building projects in Tehran, Iran.
The course CSV has 109 columns: four project-date fields, eight project variables,
19 economic variables at each of five lags, and two realized outputs (sales price
and construction cost).

### Source and course copy

- Creator: Mohammad Rafiei
- Publisher and original source: [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/437/residential+building+data+set)
- UCI dataset DOI: [`10.24432/C5S896`](https://doi.org/10.24432/C5S896)
- UCI citation: Rafiei, M. (2015), *Residential Building* [Dataset], UCI Machine
  Learning Repository
- Upstream file: `Residential-Building-Data-Set.xlsx`
- Course transformation: read the workbook's `Data` sheet; combined its two header
  rows; renamed the four project-date columns to `start_year`, `start_quarter`,
  `completion_year`, and `completion_quarter`; normalized project and economic IDs
  (for example, `V-2` to `v_2` and lagged `V-11` fields to `v_11_lag1` through
  `v_11_lag5`); renamed `V-9` to `actual_sales_price` and `V-10` to
  `actual_construction_cost`; retained all 372 rows; and exported the result as CSV
- Shape: 372 rows and 109 columns
- SHA-256: `eeee5cd5ce49524ad3513f756f2b7583ba06d1786993fe41007d986f05a22b0d`
- Released course use: `problem-sets/06-05-template.ipynb`

UCI distributes this dataset under the
[Creative Commons Attribution 4.0 International license](https://creativecommons.org/licenses/by/4.0/).
That license permits sharing and adaptation with appropriate attribution. This
course copy remains subject to the dataset's upstream license.

## `data_new.csv` (external only)

The Module 7 application uses the public synthetic patient-year dataset released by
the Dissecting Bias project for reproducibility of Obermeyer et al. (2019),
*Dissecting racial bias in an algorithm used to manage the health of populations*.
It contains no original patient records and has 48,784 rows and 160 columns.

### Pinned source used by Module 7

- Project: [Dissecting Bias](https://gitlab.com/labsysmed/dissecting-bias)
- Related paper DOI: [`10.1126/science.aax2342`](https://doi.org/10.1126/science.aax2342)
- Pinned source file: [`data_new.csv`](https://gitlab.com/labsysmed/dissecting-bias/-/raw/daceb25bba00e65d7b05882f049e229a8bedb60c/data/data_new.csv)
- Pinned commit: `daceb25bba00e65d7b05882f049e229a8bedb60c`
- Shape: 48,784 rows and 160 columns
- SHA-256: `5341f90f3a1d330557620af1c734e552abe0ad57053055dd13dbccc6d8384d74`
- Course transformation: none to the downloaded file; each notebook validates only
  its required columns in memory
- Released course use: all notebooks under `module_7/`

The pinned upstream revision does not include an explicit license file or license
statement. The notebooks therefore load the file directly from the pinned upstream
URL; this repository does not redistribute it or claim ownership or additional
rights.
