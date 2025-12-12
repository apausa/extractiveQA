# Fine-tuning RoBERTa for Extractive QA using the Stanford Question Answering Dataset (SQuAD)

## Extractive QA

This notebook demonstrates the fine-tuning of RoBERTa for extractive question-answering using the Stanford Question Answering Dataset (SQuAD) and preprocessing with sliding windows, **achieving 85.71% Exact Match and 92.18% F1 score**. Unlike generative approaches that generate text, extractive QA identifies the answer from the context. 

Extractive QA is impacting the field of Web Science by changing how users interact with web content. Browser engines are starting to incorporate QA capabilities that allow direct extraction of relevant answers from web pages, eliminating the need to manually read long documents. Which reduces cognitive load while searching for information. 

## RoBERTa

RoBERTa has been selected for its performance on question-answering tasks. It improves upon BERT through optimized pretraining with more data, larger batches, and dynamic masking **(Liu et al., 2019)**. These enhancements result in better performance, making it an excellent choice for extractive QA tasks. 

Encoder-only architectures like BERT and RoBERTa excel at answering direct questions, but present limitations with open-ended questions (for these situations that require elaboration, encoder-decoder architectures are more appropriate since they can generate more elaborate responses).

## Fine-tuning

Fine-tuning consists of adapting a pretrained model to a specific task to improve its performance. In this case, pre-training provides the model with a general understanding of language, while fine-tuning specializes it to identify the start and end positions of answers within a given context. 

QA systems enable users to ask specific questions about any webpage and receive precise answers extracted from their content. This is especially useful for documents where information must be found quickly. This task also benefits web accessibility by helping users with disabilities navigate complex content. 

## Index

The notebook is structured in the following phases:
- **3. Data Preparation**: SQuAD, preprocessing with sliding windows, maintaining character-to-token alignment and generating token-level labels.
- **4. Training**: Fine-tuning RoBERTa to predict answer fragments on the training dataset.
- **5. Evaluation**: Post-processing predictions, feature aggregation, calculating SQuAD metrics.
- **6. Performance Analysis**: Demonstration of improvement over the base model on specific questions covering different topics.
