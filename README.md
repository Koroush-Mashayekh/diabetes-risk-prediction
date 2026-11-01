# Diabetes Risk Prediction

Machine learning project to predict the onset of diabetes from clinical measurements,
using the Pima Indians Diabetes dataset.

> 🚧 **Status:** work in progress. Exploratory data analysis is complete; modeling is under development.

## Project structure

```text
diabetes-risk-prediction/
├── data/
│   ├── diabetes.csv        # dataset (768 patients, 8 features)
│   └── README.md           # data source and description
├── notebooks/
│   └── 01_eda.ipynb        # exploratory data analysis
├── LICENSE
└── README.md
```

## Exploratory data analysis: key findings

1. **Hidden missing values.** No null values are reported, but zeros in Glucose, BloodPressure,
   SkinThickness, Insulin and BMI are physiologically impossible and represent missing data
   (Insulin: 48.7%, SkinThickness: 29.6%).
2. **Class imbalance.** 65% non-diabetic vs. 35% diabetic. A naive model would reach 65% accuracy,
   so models are evaluated with ROC-AUC and Recall.
3. **Most informative feature.** Glucose shows the strongest relationship with diabetes,
   followed by BMI, Insulin and Age.

👉 Full analysis: [`notebooks/01_eda.ipynb`](notebooks/01_eda.ipynb)


## How to run

Open the notebooks in Google Colab (an "Open in Colab" badge is at the top of each notebook).
The data is loaded directly from this repository, so no setup is needed.

## Data source

Pima Indians Diabetes Database, originally from the National Institute of Diabetes and Digestive
and Kidney Diseases (NIDDK). See [`data/README.md`](data/README.md).

## License

MIT
