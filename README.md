# Exploring Extractive Question Answering in Web Science by Fine-tuning RoBERTa

This notebook demonstrates the fine-tuning of RoBERTa for extractive question-answering using the Stanford Question Answering Dataset (SQuAD) and preprocessing with sliding windows. Unlike generative approaches that generate text, extractive QA identifies the answer from the context.

Extractive QA is impacting the field of Web Science by changing how users interact with web content. Browser engines are starting to incorporate QA capabilities that allow direct extraction of relevant answers from web pages, eliminating the need to manually read long documents. Which reduces cognitive load while searching for information.

### 1.2. RoBERTa

RoBERTa (Robustly Optimized BERT Pretraining Approach) has been selected for its superior performance on question-answering tasks. It improves upon BERT through optimized pretraining with more data, longer training, larger batches, and dynamic masking **(Liu et al., 2019)**. These enhancements result in 2-3% better performance on SQuAD compared to BERT, making it an excellent choice for extractive QA tasks where accuracy is paramount.

Encoder-only architectures like BERT and RoBERTa excel at answering direct questions, but present limitations with open-ended questions (for these situations that require elaboration, encoder-decoder architectures are more appropriate since they can generate more elaborate responses).

### 1.3. Fine-tuning

Fine-tuning consists of adapting a pretrained model to a specific task to improve its performance. In this case, while pretraining provides the model with a general understanding of language, fine-tuning specializes it to identify the start and end positions of answers within a given context, **achieving high accuracy in EM and F1 metrics**.

QA systems enable users to ask specific questions about any webpage and receive precise answers extracted from their content. This is especially useful for documents where information must be found quickly. This task also benefits web accessibility by helping users with disabilities navigate complex content.

### 1.4. Index

The notebook is structured in the following phases:

- **3. Data Preparation**: SQuAD, preprocessing with sliding windows, maintaining character-to-token alignment and generating token-level labels.
- **4. Training**: Fine-tuning RoBERTa to predict answer fragments on the training dataset.
- **5. Evaluation**: Post-processing predictions, feature aggregation, calculating SQuAD metrics.
- **6. Performance Analysis**: Demonstration of improvement over the base model on specific questions about class slides.
