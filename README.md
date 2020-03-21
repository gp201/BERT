# BERT
There are 2 models in this repository     

## 1) [Bert_trial](https://github.com/gp201/BERT/tree/master/Bert_trial)
This is a basic model made using BertForTokenClassification([Developed by huggingface](https://huggingface.co/transformers/model_doc/bert.html)) from pytorch.   
Further details are given in the Readme file in the folder Bert_trial

## 2) [Bert_Custom](https://github.com/gp201/BERT/tree/master/BERT_Custom) 
This is a custom model. The details are given in the Readme file in the folder Bert_Custom

### Tasks
- [x] Convert a given corpus into [word,tag] format [create_dataset.ipynb](create_dataset.ipynb).
- [x] Basic BertForTokenClassification
- [x] Will try with the latest version of *pytorch_pretrained_bert* (ver==6.2.0)
- [ ] Look into implememnting the *[CLS]* token in the beginning.  
- [ ] Bugfix with regard to numbers and symbols ex:(AF) not recognized as T047 numbers are taken as a new sentence.
> BERT prepends a [CLS] token (short for "classification") to the start of each sentence (this is essentially like a start-of-sentence token). 
