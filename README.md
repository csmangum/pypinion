# PyPinion
PyPinion is a classification model designed to identify opinions in news articles.

## Overview
This initial version is based on self-labeled sentences from 7,000 random CNN articles using a library called [Simple Transformers](https://github.com/ThilinaRajapakse/simpletransformers) to classify if a sentence is an opinion or not. Simple Transformers is based on the [Transformers](https://github.com/huggingface/transformers) library by HuggingFace.

The current model leverages a pre-trained [RoBERTa](https://huggingface.co/transformers/model_doc/roberta.html) architecture from Facebook and performs reasonably against standard news sentences. The model is currently more of a proof-of-concept and there are plans for a more robust and scientific approach to its development.  

### Model evaluation metrics
* Accuracy: 91.08%
* F1 Score: 91.79%
* ROC AUC: 90.93%
* Precision: 90.69%
* Recall: 92.91%


### Important Notes
* Slow to score large amounts of sentences
* Not intended to be a fact identifier
* Not tested on colloquial or informal text like twitter


## Usage

* Download the trained model zip [here](https://drive.google.com/file/d/1vjdike8Wn6OHB4bXBohs_5DxTojXImHt/view?usp=sharing)
* Install [Simple Transformers](https://github.com/ThilinaRajapakse/simpletransformers)

```python
from simpletransformers.classification import ClassificationModel


sent = 'The president should always speak to the people that got him into office' # Example sentence

trained_model = ClassificationModel("roberta", PATH) # PATH is the location of the extracted trained model
predictions, raw_outputs = trained_model.predict([sent])

print(predictions[0]) # '1' indicates opinion,'0' indicates non-opinion
```
## Examples

| Sentence | Result |
|---|---|
| The show was successful because even though it was about death, it lacked violence. | Opinion |
| The apparent car bomb attack happened outside of St. Finbar's Catholic Church, according to Plateau Gov. Jonah David Jang. | Non-Opinion |
| Perhaps it's good for his job as a comedian, but, personally, there's no sense of schadenfreude. | Opinion |
| Similarly, when fewer people are waiting to cross the road, the traffic is given a longer set of green lights. | Non-Opinion |
| They choose to stop paying, one way or another. | Opinion |
| South Sudan, which became independent in 2011, is facing many challenges. | Opinion |
| FC Shakhtar regretfully informs that on 8 February 2014 the life of a footballer Maicon Pereira de Oliveira tragically ended. | Non-Opinion  |
| The list includes the startups I consider to have the most potential, to be the most viable -- not necessarily the most popular or hyped. | Opinion |
| Europe has more than its fair share of sausages that time forgot. | Opinion |
| The Spanish club, also hit with a $455,000 fine, says the transfer ban is "disproportionate" and "excessive." | Non-Opinion |
