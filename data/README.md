# Course data

This directory contains the datasets needed by the released GB656 problem-set
templates and preparatory labs. Each notebook first looks for a local file in this
directory and otherwise loads the same course copy from the public GitHub repository.

## Dataset catalog

| File | Released materials | Upstream terms |
|---|---|---|
| `car_price_prediction.csv` | Problem Set 1 and its lab | MIT declaration in the upstream dataset card |
| `SeoulBikeData.csv` | Problem Set 2 and its lab | Creative Commons Attribution 4.0 International |

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
- Released course use: `problem-sets/03-02-template.ipynb` and
  `problem-sets/lab-lectures/03-02-lab.ipynb`

UCI distributes this dataset under the
[Creative Commons Attribution 4.0 International license](https://creativecommons.org/licenses/by/4.0/).
That license permits sharing and adaptation with appropriate attribution. This
course copy remains subject to the dataset's upstream license.
