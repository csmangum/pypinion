# PyPinion
PyPinion is a model designed to identify opinions in text.

## Overview
This initial version is based on self-labeled sentences from 7,000 random CNN articles using a library called [Simple Transformers](https://github.com/ThilinaRajapakse/simpletransformers) to classify if a sentence is an opinion or not. Simple Transformers is based on the [Transformers](https://github.com/huggingface/transformers) library by HuggingFace.

The current model is based on pre-trained [RoBERTa](https://huggingface.co/transformers/model_doc/roberta.html) architecture from Facebook and performs reasonably against standard news sentences. The model is currently more of a proof-of-concept and there are plans for a more robust and scientific approach to its development.  

### Model eval metrics:
* Accuracy: 91.08%
* F1 Score: 91.79%
* ROC AUC: 90.93%
* Precision: 90.69%
* Recall: 92.91%

### Important Notes
* Slow to score large amounts of sentences
* Not intended to be a fact identifier
* Not built for colloquial or informal text like twitter
