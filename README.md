# BERT
There are 2 models in this repository
1) Bert-trial 
> This is the first model that was made Details given below
2) Bert_custom
> This is the next custom model. The details are given in the Readme file in the folder Bert_custom

## Bert-trial
It is using: 
1) pytorch_pretrained_bert == 0.4.0 ```!pip3 install pytorch_pretrained_bert==0.4.0```
2) seqeval ```!pip install seqeval```

In the latest update for pytorch_pretrained_bert by [huggingface](https://huggingface.co/transformers/model_doc/bert.html) (ver>0.5.0) the Bert-trial code will yield a very low validation score.   
So you need to pad sequence not with **'O'** but with **'[PAD]'** token.

Tasks
- [x] Basic BertForTokenClassification
- [ ] Will try with the latest version of *pytorch_pretrained_bert* (ver==6.2.0)
- [ ] Look into implememnting the *[CLS]* token in the beginning.   

> BERT prepends a [CLS] token (short for "classification") to the start of each sentence (this is essentially like a start-of-sentence token). 

### Data
The data folder contains the corpus.    
[The dataset.csv](data/dataset.csv) file contains a model O/P for a single abstract.   
If multiple tags or no tags are present it will be present in the given format.

| Word            | Tag       |
| --------------- |:---------:|
| associated	    | 0         |
| with	          | 0         |  
| coronary	      | T019,T047 |  
| sinus	          | T019,T047 |

> The individual tags can be obtained by simply splitting the tag field ```tag.split(,)```     

Tasks
- [x] Convert a given corpus into [word,tag] format [create_dataset.ipynb](create_dataset.ipynb).
- [ ] Bugfix with regard to numbers and symbols ex:(AF) not recognized as T047 numbers are taken as a new sentence.
