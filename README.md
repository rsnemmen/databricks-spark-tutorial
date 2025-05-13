Getting started with databricks and Apache Spark
=================================================

Jupyter notebooks meant to be run in [Databricks](https://www.databricks.com). Create a free account there and run these notebooks to get familiarized with the platform and its capabilities.

Notebooks based on the [Getting started with Apache Spark on Databricks tutorial](https://www.databricks.com/spark/getting-started-with-apache-spark).

Docker image

docker pull quay.io/jupyter/all-spark-notebook

Start docker with

docker run -p 8888:8888 -p 4040:4040 \
  -v "/Users/nemmen/Dropbox/industry/study/DS/spark-getting-started:/home/jovyan/work" \
  --name all-spark \
  quay.io/jupyter/all-spark-notebook


## Notebooks

[Notebook 1](1-basics,%20ARIMA.ipynb): EDA, naive, ACF, PACF, (S)AR(I)MA.

[Notebook 2](2-ML,%20linear%20model.ipynb): prepare data for pytorch, linear model.

[Notebook 3](3_RNN_and_more—need_NVIDIA_GPU.ipynb): RNN, deep RNN, multivariate/multitarget, seq2vec, uncertainty band.

[Notebook 4](4_LSTM—need_NVIDIA_GPU.ipynb): LSTM, GRU, CNN, wavenet.

[Notebook 5](5-XGBoost.ipynb): XGBoost.


