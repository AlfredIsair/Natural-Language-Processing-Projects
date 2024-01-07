# Clinical-NER-Named-Entity-Recognition-

**Overview**

Named Entity Recognition (NER) is a foundational element in Natural Language Processing (NLP) within the medical domain. It plays a pivotal role in extracting meaningful chunks from clinical notes and reports, providing valuable input for downstream tasks such as assertion status detection, entity resolution, relation extraction, and de-identification.

This GitHub project focuses on leveraging the ZeroShotNerModel with the RoBERTa Question Answering model to perform NER without the need for annotated datasets. The unique approach involves crafting prompts for entity detection, allowing healthcare providers to analyze clinical notes, extract keywords, and assign them to specific entities like PROBLEM, TEST, or TREATMENT.

**Model Overview**

**ZeroShotNerModel**
Utilizes the RoBERTa Question Answering model for entity detection without relying on annotated datasets.
The model is capable of extracting entities through crafted prompts, eliminating the need for manual labeling during training.

**Pipeline Configuration**
The project creates a pipeline for the Zero-Shot NER model, comprising the following stages:

1.DocumentAssembler: Prepares the clinical notes for further processing.

2.SentenceDetector: Identifies and separates sentences within the clinical notes.

3.Tokenizer: Breaks down sentences into individual tokens.

4.ZeroShotNer: Utilizes the ZeroShotNerModel to perform entity detection without embeddings models.

5.NerConverter: Converts the detected entities into a structured format for easy analysis.

To customize entity detection, a dictionary is created with specific questions for detecting entities and the corresponding labels desired in the results. For instance, the model may focus on detecting entities like PROBLEM, DRUG, PATIENT_AGE, DIAGNOSIS , SYMPTOMS and ADMISSION_DATE.
The setEntityDefinitions parameter is then used to provide this dictionary to the model, allowing for targeted and flexible entity recognition.
