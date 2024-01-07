# Clinical-Entity-Resolution

Clinical entity resolution is a crucial technique for extracting valuable insights from clinical text data. It involves linking recognized entities to corresponding medical terminologies, such as ICD-10 codes or RxNorm codes. This process facilitates various healthcare-related tasks, including medical research, data analysis, and billing.

## **Spark NLP for Healthcare:**

Spark NLP for Healthcare provides a comprehensive pipeline for clinical entity resolution. This pipeline leverages pre-trained models and incorporates the following steps:

**Named Entity Recognition (NER)**: This step extracts relevant clinical entities from the text, such as diseases, symptoms, and drugs.

**Sentence Embeddings:** Sentence embeddings are generated for each entity using a pre-trained model like Sentence BERT (SBERT).

**Entity Resolution:** These embeddings are then compared against a medical terminology database to identify the closest matching code.


##  **Pipeline Overview**

This pipeline utilizes several Spark NLP for Healthcare annotators to achieve accurate entity resolution with ICD-10 mapping:

**DocumentAssembler**: Prepares the input text data for NLP processing.

**SentenceDetectorDL:** Identifies individual sentences within the text.

**Tokenizer:** Breaks down each sentence into individual tokens (words).

**WordEmbeddings:** Generates word embeddings that capture the semantic meaning of each token.

**Clinical NER:** Recognizes and extracts clinical entities (e.g., diagnoses, symptoms) from the text.

**NerConverterInternal:** Filters and transforms extracted entities into chunks.

**Chunk2Doc:** Converts the entity chunks back into document format for further processing.

**BertSentenceEmbeddings**: Generates sentence embeddings for each entity chunk.

**SentenceEntityResolverModel**: Utilizes a pre-trained model to find the closest ICD-10/LOINC/CPT code based on the sentence embeddings.

