# Keyword Extraction 

## Description
This repository hosts a Python-based Keyword Extraction Tool built using IPython widgets and Spark NLP. The tool leverages the YAKE (Yet Another Keyword Extractor) algorithm, providing users with an intuitive interface to input text and extract relevant keywords. The extracted keywords are displayed alongside the input text, with highlighting for easy identification. This tool is useful for tasks such as information retrieval, document summarization, and content categorization in natural language processing (NLP) applications.

## Tools Used
- IPython widgets: Used for building the user interface for inputting text and displaying keyword extraction results.
- Spark NLP: Utilized for natural language processing tasks, including tokenization and keyword extraction.
- YAKE (Yet Another Keyword Extractor): The algorithm employed for unsupervised keyword extraction from the input text.

## Libraries
The following Python libraries are used in this project:
- pyspark==3.4.1: Apache Spark library for distributed data processing.
- spark-nlp==5.1.2: Natural language processing library built on top of Apache Spark.
- ipywidgets: Interactive widgets for Jupyter notebooks and IPython.
- pandas: Data manipulation and analysis library.

## Installation
To use the Keyword Extraction Tool, ensure you have the required dependencies installed. You can install them using the following command:
```bash
! pip install -q pyspark==3.4.1 spark-nlp==5.1.2 ipywidgets pandas

