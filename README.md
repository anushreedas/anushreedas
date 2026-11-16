# Hi, I'm Anushree 👋

**Machine Learning Engineer / Data Scientist** · I work on tabular, time-to-event, and sequence modelling for financial data, with a focus on evaluation that holds up outside the notebook (no leakage, out-of-time validation, models that are calibrated and tuned for a decision).

🇪🇺 &nbsp;**Open to ML / Data Science roles in the Netherlands, Belgium and Luxembourg.**

- 🏦 &nbsp;**Now:** ML proofs of concept at **Arkatechture** for financial-services clients: arrival forecasting and next-best-product recommendation
- 🎓 &nbsp;MS Data Analytics, **McDaniel College** (2026) · MS Computer Science, **RIT** (2021)
- ☁️ &nbsp;Previously at **Amazon Web Services** (Computer Vision Data Platform) and **Quantil / CDNetworks**
- 🔬 &nbsp;Research: [**DTProfiler**](https://github.com/anushreedas/DTProfiler), ML-based SQL column type inference for automated data pipelines

---

## 🔬 Research: DTProfiler, SQL data type inference with ML

Infers the SQL type of CSV columns (VARCHAR, NUMBER, BOOLEAN, TIME) from column statistics plus FastText embeddings of the column name. It catches cases where regex and pandas typing go wrong, such as IDs and ZIP codes whose leading zeros would be lost if cast to numbers.

| | |
|---|---|
| **Models** | Decision tree, random forest, a modular neural network, and an RF + NN ensemble, compared with pandas dtype inference as the baseline |
| **Evaluation** | Table-grouped and source-grouped splits so no test column shares a CSV (or a whole data source) with training · 5 splits × 3 seeds · variance decomposition, ablations, PCA sensitivity |
| **Result** | RF + NN ensemble: **97.2% accuracy on unseen tables and 95.6% on unseen data sources**, vs. 88.7% and 90.3% for pandas, which never detects temporal types |

📂 [Code, data splits and notebooks](https://github.com/anushreedas/DTProfiler)

---

## ⭐ Featured work: next-best-product prediction in retail banking

Predicts which product a new bank customer will adopt next (loan, card, both, or neither) from only their **first 90 days** of transactions. Built on the Berka PKDD'99 dataset (1M+ transactions, 4,303 accounts).

| | |
|---|---|
| **Problem framing** | Survival landmarking with competing risks and right-censoring, which removes the target leakage that full-history features introduce |
| **Models compared** | ElasticNet, LightGBM, cause-specific Cox PH, Random Survival Forest, an RMTPP-style GRU temporal point process (PyTorch), and an ensemble |
| **Validation** | Expanding-window temporal CV, held-out 1997 cohort, 1,000-sample bootstrap CIs |
| **Result** | Random Survival Forest: **macro ROC-AUC 0.821**. A cost-sensitive decision rule raised **macro-F1 from 0.217 to 0.432** on a target that is 87% one class |

📓 [Research notebook + 11-page paper](https://github.com/anushreedas/berka-next-best-product) &nbsp;·&nbsp; 🧱 [Modular, reproducible pipeline](https://github.com/anushreedas/banking-landmark-survival-rmtpp) &nbsp;·&nbsp; ✍️ [Write-up on Medium](https://anushree-das.medium.com/continuous-time-next-best-product-recommendation-tabular-baselines-survival-analysis-and-rmtpp-353b55c76b14)

---

## Other selected projects

| Project | What it does | Stack |
|---|---|---|
| [BERT Confusion Detection](https://github.com/anushreedas/BERT_LLM_Detect_Confusion_Emotion) | Fine-tuned BERT / TOD-BERT on transcribed speech to detect multi-level confusion; 12 configurations compared with sign-test significance checks | PyTorch, Hugging Face |
| [Credit Card Data Warehouse](https://github.com/anushreedas/credit-card-transactions-datapipeline) | ETL pipeline and star-schema warehouse for 24M credit card transactions, built for fraud and customer-behaviour analysis | R, SQL, dimensional modelling |
| [Dishwasher-Safe Image Classifier](https://github.com/anushreedas/dishwasher-safe-image-classifier) | Five CNN architectures on a custom imbalanced dataset of 1,237 images; best (VGG16-BN) reached 80% test accuracy, MCC 0.579 | PyTorch, torchvision |
| [Handwritten Math Recognition](https://github.com/anushreedas/Handwritten_Math_Expression_Recognition) | Stroke segmentation, symbol classification and layout-tree parsing to LaTeX / MathML | scikit-learn |
| [Content-Based Image Retrieval](https://github.com/anushreedas/Content_Based_Retrieval_System_Dog_Images) | Colour histogram, Gabor, HOG and ResNet50 features compared for similarity search across 133 dog breeds | PyTorch, OpenCV |
| [Parking Availability Prediction](https://github.com/anushreedas/Car_Detection) | Faster R-CNN car counts combined with time, weather and lot capacity to estimate free spots | TensorFlow |

<details>
<summary>Classical computer vision</summary>

- [Foreground Mosaic with MOG2](https://github.com/anushreedas/Foreground_Mosaic_OpenCV): composites moving objects from video into one frame
- [Bird's-Eye View & Vehicle Counting](https://github.com/anushreedas/Birds_Eye_Transformation_And_Motion_Estimation): Hough-line lane detection, perspective warp, vehicle counting

</details>

---

## Toolbox

```
Modelling     scikit-learn · LightGBM · PyTorch · Hugging Face Transformers · TensorFlow
              survival analysis (lifelines, scikit-survival) · time-series forecasting
              temporal point processes (Hawkes, Neural Hawkes, RMTPP) · FastText embeddings
              imbalanced classification · calibration & threshold optimisation
Data          Python · SQL · PySpark · pandas · R · Snowflake · ETL/ELT · data quality
Production    Docker · CI/CD · AWS (S3, Lambda, Glue) · experiment tracking · monitoring
```

**AWS Certified Cloud Practitioner** (valid to Dec 2027)

---

## Writing

I write on [Medium](https://anushree-das.medium.com/) about the modelling I do and the fundamentals that come before it.

- 🆕 [Forecasting Data-Pipeline Arrivals with Poisson, Hawkes, Neural Hawkes and LogNormMix](https://anushree-das.medium.com/forecasting-data-pipeline-arrivals-with-poisson-hawkes-neural-hawkes-and-lognormmix-409561eb2f4f)
- 🆕 [Continuous-Time Next-Best-Product Recommendation: Tabular Baselines, Survival Analysis, and RMTPP on the Berka Banking Dataset](https://anushree-das.medium.com/continuous-time-next-best-product-recommendation-tabular-baselines-survival-analysis-and-rmtpp-353b55c76b14)
- [How to Build a Data Warehouse from 24 Million Credit Card Transactions](https://anushree-das.medium.com/how-to-build-a-data-warehouse-from-24-million-credit-card-transactions-3cb6e48a829a)
- [Your Image Dataset Is Ready. Now Which Model Do You Train?](https://anushree-das.medium.com/your-image-dataset-is-ready-now-which-model-do-you-train-b72d63367708)
- [Finding Structure in Unstructured Data: VGG16 + KMeans on Unlabelled Images](https://anushree-das.medium.com/finding-structure-in-unstructured-image-dataset-an-initial-analysis-of-unlabelled-data-0cf2f6231735)
- [Before You Train Anything, Analyze This: EDA for Image Datasets](https://anushree-das.medium.com/image-dataset-analysis-using-python-libraries-pandas-and-matplotlib-a640e5f59805)

---

## Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-anushree--s--das-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/anushree-s-das)
[![Medium](https://img.shields.io/badge/Medium-anushree--das-000000?style=flat&logo=medium&logoColor=white)](https://anushree-das.medium.com/)
[![Email](https://img.shields.io/badge/Email-anushreedas.2710@gmail.com-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:anushreedas.2710@gmail.com)
