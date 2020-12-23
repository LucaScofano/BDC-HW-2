# Big Data Computing HW 2

The assignment is based on finding the best clustering technique that provides the most accurate results comparing them with `labels.txt` (our Ground Truth). Since the initial dataset `corpus.txt` contains **314808** phrases and **87094** dimensions (after the text pre-processing) I performed some random projection, Mini-Batch clustering, and dimensionality reduction with Truncated-SVD.

## File contained in the folder

* README.pdf
* HW2.ipynb 
* clean_sample.txt

## Data Pre-processing

In section **1.1 Create Dataset** the only thing to change in order to use it on your personal computer is the path where the input data `corpus.txt` and `labels.txt` is stored. Since I used Google Colab, I mounted my own Google Drive and used that as a directory.

Since the preprocessing would take a while to run, section **1.2 Preprocessing** can be skipped by using a cleaned version of the corpus, the file is called `clean_sampled.txt`  

## Clustering

This section is divided mainly into three subsections.

The **first** one involves *K-means ++ using as samples random projections* of the original data. The first two methods use Grid-Search in order to obtain the best combination.

```python
def grid_k_means_random(components, n_it, data):
```
The parameters that can be set are:
* components: a list of random projected samples size
* n_it: number of iterations of k-means ++
* data: original data vectorized

The **second** one involves *mini-batches K-means ++*. All of the Grid-Search is contained in a single function

```python
def grid_k_means_mini_random(batch, n_it, data): 
```
The parameters that can be set are:
* batch: a list containing different batch sizes
* n_it: number of iterations of k-means ++
* data: original data vectorized

For the **third** sub-section, grid-search wasn't necessary since very good results are obtained with the default values. 
