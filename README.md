# Opinion Lab Group 2.6 - Social Topic Distributions


**Description:**

In this project we derive vector representations of: 

  **a)** news and social media articles   
  **b)** individual social media users
    
These vector representations are again cluster or topic distributions which can be compared amongst each other using Jensen Shannon divergence. Consequently, we can analyze if news articles attract answers from individuals with similar topics of interest.


**Tasks:**

* Perform GMM clustering of words and sentences using pre-trained textual embeddings of words and sentences.
    * Pre-trained textual embeddings: GloVe and Universal Sentence Encoder version4
    * Optimize k, e.g., by using criteria such as GMM distance, Bayesian information criterion, and manual heuristics (i.e. "what looks good")
    * The clusters are called topics hereafter
* Derive the cluster or topic distributions(label the topics using word lists) for each news article and for each social media user.
    * Use cosine similarity for labeling static word embeddings and clarity score for sentence embeddings. 

* Represent each newspaper article and all comments of one newspaper article as the normalized distribution/histogram of (cluster, sentiment) tuples over its samples (i.e. words or sentences). This gives us a fixed-dimensional representation of our texts of interest.
    * Use summation and normalization for computing document probability distributions from sentence probability distributions.
    * Use CF-IDF for computing document probability distributions from word probability distributions. Then apply summation and normalization over the word distributions. 

* Calculate mean and standard deviation of Jensen Shannon divergences between 
    * 1- different random user sets and articles
    * 2- answering users of an article and the respective article
* Analyze the differences between both. See if users who are answering on an article have more similar topic distributions than random users.
* Analyze the users topic distributions and articles topic distributions.
* These experiments are done for multiple social media sources analogously.


#### Team members:

*  Mürüvvet Hasanbasoglu
*  Hakan Akyürek
    

#### Presentations Timetable:


|        | 1st      | 2nd      | 3rd      | 4th      | 5th      | 6th      | Final    |
|--------|----------|----------|----------|----------|----------|----------|----------|
| Slot 2 | 04\.05\. | 18\.05\. | 02\.06\. | 15\.06\. | 29\.06\. | 13\.07\. | 20\.07\. |



## Directory:
Following is the folder structure of our repository.

Remarks:
* Check /notebooks/SocialTopicDistributions.ipynb for our main code.
* All the relevant saved python objects can be found under social-topic-distributions.
```
├── Final-Report
│   ├── SocialTopicDistributions.pdf
│   └── SocialTopicDistributions.zip
├── notebooks
│   └── SocialTopicDistributions.ipynb
├── Presentations
│   ├── Final Presentation.pdf
│   ├── Presentation_1.pdf
│   ├── Presentation_2.pdf
│   ├── Presentation_3.pdf
│   ├── Presentation_4.pdf
│   ├── Presentation_5.pdf
│   ├── Presentation_6.pdf
├── README.md
└── social-topic-distributions
    ├── article_clusters
    │   ├── glove_15_article_clusters
    │   ├── glove_30_article_clusters
    │   ├── sentence_15_article_clusters
    │   └── sentence_30_article_clusters
    ├── glove_embeddings
    │   ├── fine_tuned_embeddings.txt
    │   └── vocab_embeddings.txt
    ├── idfs
    │   ├── crisp_idf_15
    │   └── crisp_idf_30
    ├── lower_sw_punc_rw_processed_data
    │   ├── cafemom.json
    │   ├── chicagotribune.json
    │   ├── disqus.json
    │   ├── fb.json
    │   ├── foodbabe.json
    │   ├── foodrevolution.json
    │   ├── huffingtonpost.json
    │   ├── latimes.json
    │   ├── nypost.json
    │   ├── nytimes.json
    │   ├── organicauthority.json
    │   ├── organicconsumers.json
    │   ├── quora.json
    │   ├── reddit.json
    │   ├── usatoday.json
    │   ├── usmessageboard.json
    │   └── washingtonpost.json
    ├── models
    │   ├── model_diag_15_glove
    │   ├── model_diag_15_sentence
    │   ├── model_diag_30_glove
    │   └── model_diag_30_sentence
    ├── static_data
    │   ├── articles_per_dataset
    │   ├── biased_rand_users
    │   ├── forum_rand_users
    │   ├── general_rand_users
    │   ├── news_rand_users
    │   ├── unbiased_rand_users
    │   └── users_per_dataset
    └── user_clusters
        ├── glove_15_user_clusters
        ├── glove_15_user_clusters_cfidf
        ├── glove_30_user_clusters
        ├── glove_30_user_clusters_cfidf
        ├── sentence_15_user_clusters
        └── sentence_30_user_clusters
```
