# PyPinion
PyPinion is a model designed to identify opinions in text.

This initial version is based on self-labeled sentences from 7,000 random CNN articles using a library called Simple Transformers to classify if a sentence is an opinion or not. Simple Transformers is based on the Transformers library by HuggingFace.

The current model is based on pre-trained RoBERTa architecture from Facebook and performs reasonably against standard news sentences.  

**Model eval metrics:**
* Accuracy: 91.08%
* F1 Score: 91.79%
* ROC AUC: 90.93%
* Precision: 90.69%
* Recall: 92.91%
