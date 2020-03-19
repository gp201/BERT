# BERT
Bert-trial is using: 
1) pytorch_pretrained_bert == 0.4.0 ```!pip3 install pytorch_pretrained_bert==0.4.0```
2) seqeval ```!pip install seqeval```

In the latest update for pytorch_pretrained_bert by [huggingface](https://huggingface.co/transformers/model_doc/bert.html) (ver>0.5.0)
you need to pad sequence not with **'O'** but with **'[PAD]'** token.

Tasks
- [x] Basic BertForTokenClassification
- [ ] Will try for the latest version of *pytorch_pretrained_bert*
- [ ] Look into implememnting the *[CLS]* token in the beginning.   

> BERT prepends a [CLS] token (short for "classification") to the start of each sentence (this is essentially like a start-of-sentence token). 
