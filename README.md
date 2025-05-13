Getting started with databricks and Apache Spark
=================================================

Notebooks that can be run locally or on [Databricks](https://www.databricks.com) illustrating: 

- Running an Apache Spark job
- Using the Dataframe and MLlib APIs
- Fitting a simple regression model
- Handling streaming datasets

Based on the [Getting started with Apache Spark on Databricks tutorial](https://www.databricks.com/spark/getting-started-with-apache-spark). 

## Running Spark locally

When running a "serverless compute" databricks instance on the free tier, many of the commands will not run. For example, you will not be able to use scala commands, perform fits or continuously generate a time series (notebooks 3-4). In that case, you should run the notebooks locally as follows.

(1) Pull a good Docker image.

I suggest the `all-spark-notebook` one which comes with a full installation of spark and jupyter lab:

    docker pull quay.io/jupyter/all-spark-notebook

(2) Start a Docker container with

```shell
docker run -p 8888:8888 -p 4040:4040 \
  -v "/path/to/these/notebooks:/home/jovyan/work" \
  --name all-spark quay.io/jupyter/all-spark-notebook
```

This will map port 8888 from the container to your host machine for accessing Jupyter Lab. Port  4040 maps to the Spark Application UI. Take note of an address like http://localhost:8888/lab?token=605809399c43cf30f3df2c04d936597cccb06db22444f028 that will show up.

(3) Open Jupyter Lab in your browser.





## Notebooks

[Notebook 1](1-My%20first%20Apache%20Spark%20job.ipynb): Running your first Apache Spark job.

[Notebook 2](2-Dataframe,%20SQL%20queries.ipynb): Creating a dataframe, running a SQL query.

[Notebook 3](3-Create%20sample%20data,%20process%20and%20visualize.ipynb): Create sample data, process and visualize with Scala.

[Notebook 4](4-Spark%20ML%20library.ipynb): Fitting a linear model with the machine learning library.

[Notebook 5](5-Streaming.ipynb): Structured streaming—handling streaming datasets.


