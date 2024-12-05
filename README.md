### Code Execution
Due to the private nature of the data set, I cannot publically share the dataset, but the jupyter notebooks have been left with the code executed and output shown for the real data. Additionally, included in this repository is a 'synthestic_comments.csv' which contain fake comments made by me. The models here produce nearly perfect results on this fake data set since there are few comments and most of them are duplicated, but it will demonstrate that the code does run on a data set. 

To run the code:
clone the repository and run the scripts in the following order:
1) Exploration.ipynb (it will make a train and test split of the data)
2) ml-modes/naiveBayes.ipynb
3) deep-models/a_sequenceModels.ipynb
4) deep-models/b_GRUModels.ipynb
5) deep-models/c_GRU-commentLength.ipynb
6) deep-models/d_GRU-Finetuned.ipynb
7) deep-models/e_GRU-Evaluation.ipynb

Each deep model script will need about 20-30 seconds to load the word2vec pretrained embeddings, otherwise the scripts should run pretty fast on the synthetic data set. 

### Dependencies and Specifically Installed Packages

* cudatoolkit               11.2.2 conda-forge
* cudnn                     8.1.0.77 conda-forge
* gensim                    4.3.3 conda-forge
* imbalanced-learn          0.12.4 conda-forge
* keras                     2.10.0 pypi
* keras-preprocessing       1.1.2 pypi
* keras-tuner               1.4.7 pypi
* matplotlib                3.8.4 conda-forge
* numpy                     1.22.4 conda-forge
* pandas                    1.4.3  conda-forge
* python                    3.9.20 
* scikit-learn              1.5.2 conda-forge
* scipy                     1.13.1 conda-forge
* seaborn                   0.13.2 conda-forge
* tensorflow                2.10.1 pypi