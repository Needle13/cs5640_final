# About this Project
The Utah Wellbeing Project assesses and monitors wellbeing across Utah communities to support informed city planning and decision-making. In 2024, over 15,000 respondents from 49 Utah cities participated in an online survey. The survey included open-ended questions, such as what residents value most about their city and what improvements they would like to see. This effort resulted in 26,414 comments, which were shared with city leaders upon survey completion. However, organizing these comments for analysis and actionable insights is a time-intensive task. To address this challenge, this project applies natural language processing (NLP) techniques and sequence-based neural networks to classify comments into approximately 24 dominant topics, such as transportation, safety, recreation, and healthcare. Results indicate that gated recurrent units (GRUs) combined with pre-trained Word2Vec embeddings achieve modest performance in comment classification, providing a foundation for more efficient and insightful analysis of community feedback. The full report can be viewed in the **finalReport_5640.pdf**, **finalPresentationSlides.pdf**, or video presentation **finalPresentation.mp4**. 

### Code Execution
Due to the private nature of the data set, I cannot publically share the dataset, but the jupyter notebooks have been left with the code executed and output shown for the real data. Additionally, included in this repository is a 'synthestic_comments.csv' which contain fake comments made by me. The models here produce nearly perfect results on this fake data set since there are few comments and most of them are duplicated, but it will demonstrate that the code does run on a data set. 

To run the code:
clone the repository and run the scripts in the following order:
1) Exploration.ipynb - EDA and some basic pre-processing. 
2) ml-modes/naiveBayes.ipynb -  Use a Naive Bayes as a baseline model. 
3) deep-models/a_sequenceModels.ipynb - Explore Different Sequence Models: RNN, LSTM, GRU
4) deep-models/b_GRUModels.ipynb - Explore different GRU architectures
5) deep-models/c_GRU-commentLength.ipynb - Explore the effect of other hyper-parameters
6) deep-models/d_GRU-Finetuned.ipynb - Tune Hyper-parameters
7) deep-models/e_GRU-Evaluation.ipynb - Qualitatively and quantitatively evaluate the model.

Each deep model script will need about 20-30 seconds to load the word2vec pretrained embeddings, otherwise the scripts should run pretty fast on the synthetic data set. 

### Dependencies and Installed Packages

* cudatoolkit               11.2.2 conda-forge
* cudnn                     8.1.0.77 conda-forge
* gensim                    4.3.3 conda-forge
* imbalanced-learn          0.12.4 conda-forge
* keras                     2.10.0 pypi
* keras-tuner               1.4.7 pypi
* matplotlib                3.8.4 conda-forge
* numpy                     1.22.4 conda-forge
* pandas                    1.4.3  conda-forge
* python                    3.9.20 
* scikit-learn              1.5.2 conda-forge
* scipy                     1.13.1 conda-forge
* seaborn                   0.13.2 conda-forge
* tensorflow                2.10.1 pypi