# **Problem Description**

## **About the Project**

This project focuses on building a machine learning pipeline to estimate the *Unified Index of Tension and Interruptions* (UITI), a composite technical indicator used to evaluate the quality of electrical service in distribution networks. The work is developed as part of an academic module on interpretable machine learning applied to power systems.

The goal is not only to train a predictive model—based on the TabNet architecture—but also to generate interpretable analyses using Retrieval-Augmented Generation (RAG) and Agentic RAG to understand the underlying causes of poor service quality in specific circuits and municipalities.

---

## **Problem to Solve**

Ensuring high-quality electrical service requires monitoring both **power quality** and **continuity of service**. Traditional reliability indicators such as SAIFI, SAIDI, and CAIDI measure different aspects of service interruptions, but they fail to capture voltage stability and multi-factor interactions occurring at specific points of the network.

To address this, utilities use **UITI**, a unified metric that integrates:

* Voltage stability
* Frequency of interruptions
* Duration of interruptions

However, predicting UITI is challenging because it depends on a combination of technical conditions, operational behavior, spatial context, and even meteorological factors. Understanding which variables contribute most to high UITI values is critical for:

* Identifying assets or circuits with poor service quality
* Supporting maintenance planning
* Prioritizing investments
* Detecting emerging risks before failures occur

This project aims to **predict UITI at each network asset** and **explain the factors driving that prediction**, enabling a data-driven interpretation of grid quality issues.

---

## **Objective of the Model**

The primary objective is to develop a supervised learning model capable of predicting UITI using a combination of:

* Technical attributes of equipment
* Network topology information
* Historical interruption data
* Meteorological variables (including 24-hour weather history)
* Spatial coordinates of assets

We use **TabNet**, a deep learning architecture optimized for tabular data, due to its ability to provide interpretability through feature masks and sequential attention.

---

## **Reliability and Quality Indices**

To contextualize the UITI metric, we consider the standard reliability indices in power systems:

### **SAIFI — System Average Interruption Frequency Index**

Represents the average number of interruptions per customer.

### **SAIDI — System Average Interruption Duration Index**

Represents the average outage duration per customer.

### **CAIDI — Customer Average Interruption Duration Index**

Represents the average duration of each interruption (CAIDI = SAIDI / SAIFI).

### **UITI — Unified Index of Tension and Interruptions**

A composite index that incorporates:

* Voltage level deviations
* Interruption frequency (SAIFI)
* Interruption duration (SAIDI)

UITI provides a more comprehensive view of service quality than the traditional indicators alone.

---

## **Interpretability and RAG / Agentic RAG**

In addition to training a predictive model, the project includes an explainability layer:

### **RAG Examples**

RAG is used to retrieve and reference technical documentation, operational guidelines, and reliability standards to explain the causes of high UITI for:

* The most problematic circuit
* The municipality with the highest UITI values

### **Agentic RAG Examples**

Agentic RAG goes beyond retrieval by generating multi-step, reasoning-based explanations and actionable recommendations, linking:

* Model predictions
* Technical evidence
* Regulatory compliance

This ensures transparent, traceable, and auditable decision-making.

---

- To know more abouts this implementation you can visit the following investigation paper: 

https://github.com/amalvarezme/AprendizajeMaquina/blob/main/8˙NLP˙Basics/NLP6˙LLM˙Agentes.ipynb

- to download the database you can do it from this dataset in Kaggle: 

https://www.kaggle.com/datasets/cristiancamiloo/powergrid-assets-ml-dataset/data/data/data
