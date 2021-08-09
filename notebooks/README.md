# Opinion Lab Group 2.6 - Social Topic Distributions
* Articles_preprocessing.ipynb was dublicated from Comments_preprocessing.iypnb in order to apply the curations to the articles as well.
* Our main code is included in /notebooks/SocialTopicDistributions.ipynb with the following content:
```
└── Opinion Lab Group 2.6 - Social Topic Distributions
    ├── Configure Notebook
    ├── Preprocessing
    ├── Dataset
    ├── Fine-tuning GloVe Embeddings
    ├── Experiments
    │   ├── With GloVe Embeddings - Static word embeddings
    │   │   ├── Find Optimal Model
    │   │   ├── Find Optimal n_component
    │   │   ├── Train 15 and 30 n_component GMM models
    │   │   └── Topic Labeling with word embeddings
    │   ├── With Universal Sentence Encoder - Sentence embeddings
    │   │   ├── Find Optimal n_component
    │   │   ├── Retrieve sentences vocabulary
    │   │   ├── Compute sentence embeddings
    │   │   ├── Train 15 and 30 n_component GMM models
    │   │   └── Topic Labeling with sentence embeddings
    └── Results
        ├── Clustering
        │   ├── Article Clustering
        │   └── User Clustering
        └──  User based Experiments
```
