# Custom BERT

[bert_sequence_tagger](https://github.com/gp201/BERT/tree/master/BERT_Custom/bert_sequence_tagger) is a package that contains a custom version of BERT.
It uses the basic *BertForTokenClassification* from pytorch (Hugging face).
> We can use the latest version of BERT with this package.

The dataset are text files which have Tab implementation type (.csv -> .txt)

If you have a doubt as how ColumnCorpus in flair works take a look at this [thread](https://github.com/flairNLP/flair/blob/master/resources/docs/TUTORIAL_6_CORPUS.md)

## Each file desc
[Bert_custom_run.ipynb](Bert_custom_run.ipynb)   
This file trains the model.
    
[Convert_txt.ipynb](Convert_txt.ipynb)   
This file is used to convert csv file to txt file and count the number of sentences in a file.

[create__labelled.ipynb](create__labelled.ipynb)    
This file is used to create to create a txt file with the following format:
```
dctn4	as	a	modifier	of	chronic	pseudomonas	aeruginosa	infection	in	cystic	fibrosis
T116,T123	O	O	O	O	T047	T047	T047	T047	O	T047	T047
pseudomonas	aeruginosa	pa	infection	in	cystic	fibrosis	cf	patients	is	associated	with	worse	long	term	pulmonary	disease	and	shorter	survival	and	chronic	pa	infection	cpa	is	associated	with	reduced	lung	function	faster	rate	of	lung	decline	increased	rates	of	exacerbations	and	shorter	survival
T047	T047	T047	T047	O	T047	T047	T047	T101	O	O	O	O	T079	T079	T047	T047	O	T169	T169	O	T047	T047	T047	T047	O	O	O	T033	T033	T033	T033	T033	T033	T033	T033	O	T081	T033	T033	O	T169	T169
```

[create_dataset.ipynb](create_dataset.ipynb)    
 This create one file called dataset.csv which we can split in [convert to txt](Convert_txt.ipynb) file

[create_dataset_2.ipynb](create_dataset_2.ipynb)     
This creates a train and test datafile   
- [ ] make sure the number of sentences in train and test is 70:30
> currently iys placing all the unique/first occurences of a word with tags other than 'O' in train.

## Steps to run
1) Run create_dataset_2.ipynb to get train and test files
2) Run creste_labelled.ipynb to get the labelled.txt file
3) Run Bert_custom_run.ipynbto train the model.
4) Restore_bert_model.ipynb to restore th model
 
