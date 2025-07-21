# NYC TLC Big Data Analysis

This project analyzes over a decade of NYC Taxi and Limousine Commission (TLC) trip data, focusing on spatial-temporal trends, data quality, external data integration, and machine learning-based demand forecasting. The work includes a big data processing pipeline implemented using Dask on the Arnes HPC cluster, and includes streaming analysis using Kafka, ML modeling, and detailed analysis and visualizations.

---

## 📂 Folder Structure

* `T1/`: Dataset loading and partitioning (Parquet → yearly partitions)
* `T2/`: Data cleaning and analysis of invalid entries
* `T3/`: Export and benchmarking across file formats (CSV, CSV.GZ, HDF5, DuckDB)
* `T4/`: Exploratory data analysis (EDA) – temporal, spatial, and fare-based
* `T5/`: External data integration (weather, hotels, schools, events, holidays)
* `T6/`: Stream processing with Apache Kafka and Faust
* `T7/`: Machine learning pipeline for ride demand forecasting
* `T8/`: Analysis of FHVHV (e.g., Uber, Lyft) growth and impact
* `T9/`: Map visualizations (pickup/dropoff zones, fare heatmaps)

---

## 💡 Key Features

* Handling of >60GB TLC trip data using distributed computing
* Data cleaning for invalid data instances like negative distances, corrupt timestamps
* External data fusion: weather, events, schools, colleges, holidays, attractions, hotels...
* Streaming data processing via Kafka with real-time statistics and clustering
* Forecasting models (BVR, Dask-XGBoost, LGBM) for demand forecasting with original and augmented dataset
* Interactive maps showing zone-based analysis of rides and fares
* Business insight: FHVHV dominance vs. traditional taxis

---

## 📈 Results Summary

* FHVHV services (Uber, Lyft) now dominate the NYC market
* Augmenting data with weather/events improved forecasting MAE by up to **15,000**
* **BlockwiseVotingRegressor** outperformed other models with MAPE ≈ **7%** on the test set

---

## 🧠 Authors

* **Jovana Videnović**
* **Haris Kupinić**
