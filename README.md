# Udacity Sparkify

For the Udacity Data Scientist course a big dataset of events from the virtual music streaming service "Sparkify" 
has to be analyzed to find out, which users are likely to churn (either downgrade from paid service to free 
or cancel the service completely). 

Using Spark a model should be trained to predict churning before it happens.
This gives the ability to take actions to avoid a user from churning, e.g. make a special offer.


# Data

The full data set (12GB) is provided in a S3 Bucket `s3a://udacity-dsnd/sparkify/sparkify_event_data.json`  
Also a mini dataset (120MB) is provided: `s3a://udacity-dsnd/sparkify/mini_sparkify_event_data.json`


# Environment and Packages

I used a Jupyter Notebook running in the same cluster as Apache Spark 3.3.2.

Because the server uses Python 3.8, the Kernel used in the Jupyter Notebook also has to be Python 3.8.  
Otherwise it is not possible to use User-Defined-Functions (udf).

In the Jupyter Notebook the following Python packages were installed:

|  Package      |  Version  |
|---------------|----------:|
|  pyspark      |    3.3.2  |
|  scikit-learn |    1.2.1  |
|  pandas       |    1.5.3  |
|  numpy        |   1.23.5  |
|  matplotlib   |    3.7.0  |
|  cryptography |   39.0.1  |

Additionally two jar files had to be downloaded and added to the spark session to allow accessing S3 buckets:

* [hadoop-aws-3.3.2.jar](https://repo1.maven.org/maven2/org/apache/hadoop/hadoop-aws/3.3.2/hadoop-aws-3.3.2.jar)
* [aws-java-sdk-bundle-1.11.1026.jar](https://repo1.maven.org/maven2/com/amazonaws/aws-java-sdk-bundle/1.11.1026/aws-java-sdk-bundle-1.11.1026.jar)


# Files

The repository contains the following files: 

* **01-setup-spark-session.ipynb** - a detailed explanation, of the spark session setup in my environment.
* **02-data-introspection.ipynp** - introspection and cleanup of the data
* **03-visualize-user-events.ipynb** - visualization of the user events
* **04-aggregate-data** - aggregate date for usage in training
* **install-s3-jars.sh** - shell script to download jar files necessary for accessing S3 buckets





# Licenses

Sources are under GPL v3 License.
Credits to [Udacity](https://www.udacity.com/) for providing the data. 


