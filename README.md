# Big Data Computing HW 2

The assignment is based on finding the best clustering technique that provides the most accurate results comparing them with `labels.txt` (our Ground Truth). Since the initial dataset `corpus.txt` contains **314808** phrases and **87094** dimensions (after the text pre-processing) I performed some random projection, Mini-Batch clustering, and dimensionality reduction with Truncated-SVD.

## File contained in the folder

* README.pdf
* HW2.ipynb 
* clean_corpus.txt

## Data Pre-processing

In section **1.1 Create Dataset** the only thing to change in order to use it on your personal computer is the path where the input data `corpus.txt` and `labels.txt` in stored.

Since the preprocessing would take a while to run, section **1.2 Preprocessing** can be skipped by using a cleaned version of the corpus, the file is called `clean_corpus.txt`  

## Usage

```python
import foobar

foobar.pluralize('word') # returns 'words'
foobar.pluralize('goose') # returns 'geese'
foobar.singularize('phenomena') # returns 'phenomenon'
```
