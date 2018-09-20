# Coreference Resolution 

## Data preparation for CoNLL 2012 transformation

### First choice
The first choice to transform OntoNote data into CoNLL 2012 format is directly use a bash script in AllenNLP package: allennlp/scripts/compile_coref_data.sh.

### Second choice
If you do not use AllenNLP, you can also prepare data from scratch.
* Download *.tar.gz from <conll.cemantix.org/2012/data.html>.
* Unzip all *.tar.gz, you will find that all folders are merged to a top-level directory conll-2012.
* If you use Python 3, you must modify the file conll-2012/v3/scripts/skeleton2conll.py to adapt Python 3 syntax (exception ... as e, print()).
* Execute 

  ```bash your-path/conll-2012/v3/scripts/skeleton2conll.sh -D your-path/ontonotes-v5.0-release/data/files/data conll-data```
  
At last, transformed \*_conll data will be embedded directly in conll-2012.


## Comlementary implementations in AllenNLP
Coreference Resolution is a practical and challenging NLP topic . It aims to find out all words or phrases which are associated to the same real-world entities. One of the current state-of-the-art result is provided by End-to-End Coreference Resolution (Lee et al, 2017). This model has been already well implemented by a Python library AllenNLP. However, some features like speaker and ELMo embeddings are not considered in the library. This repository will provide complementary implementations of the coreference model in AllenNLP.
