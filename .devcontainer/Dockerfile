FROM mcr.microsoft.com/devcontainers/python:3.10

# Installation de Java (indispensable pour Spark)
RUN apt-get update && apt-get install -y openjdk-11-jdk-headless \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

# Définition du JAVA_HOME
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64

# Installation de PySpark et des outils de notebook
RUN pip install --no-cache-dir pyspark findspark pandas matplotlib
