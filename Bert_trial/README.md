# Bert-trial
It is using: 
1) pytorch_pretrained_bert == 0.4.0 ```!pip3 install pytorch_pretrained_bert==0.4.0```
2) seqeval ```!pip install seqeval```

In the latest update for pytorch_pretrained_bert by [huggingface](https://huggingface.co/transformers/model_doc/bert.html) (ver>0.5.0) the Bert-trial code will yield a very low validation score.   
So you need to pad sequence not with **'O'** but with **'[PAD]'** token. 

## Data
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
