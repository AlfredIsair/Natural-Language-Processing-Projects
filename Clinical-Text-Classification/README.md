# Clinical-Text-Classification

This repository contains a Colab notebook demonstrating the use of Spark NLP to classify oncology reports into specific cancer types, focusing on colon, thyroid, and lung cancer.

## Overview

### Data Processing Pipeline

The project utilizes a Spark NLP pipeline to prepare text data from oncology reports for classification. The pipeline consists of the following stages:

DocumentAssembler: Converts raw text into structured document objects.

Tokenizer: Breaks down the documents into individual words or tokens.

WordEmbeddings: Generates numerical representations (embeddings) for each token, capturing the semantic meaning of words specific to the healthcare domain.

SentenceEmbeddings: Creates sentence-level embeddings by averaging the word embeddings within each sentence, capturing the overall meaning and context.

### Classification Model

The project employs the ClassifierDL annotator from Spark NLP, which is a generic multi-class text classification model. It utilizes the state-of-the-art Universal Sentence Encoder as input and leverages a deep learning model (DNNs) built within TensorFlow. The model supports up to 100 classes, making it suitable for this multi-class classification task.

