# NLP-based-Article-Analysis

Article recommandation system has been an interesting topic in NLP. Every user want to have most relavent results for their query. Delighting user is the objective of every search engine. 

In this project we will build an NLP system to do two task:
1. Domain-Specific Keyword/Topic/Tag Extraction System
2. Article Ranking System

## 1. Domain-Specific Keyword/Topic/Tag Extraction System:
Objective: **Given an Article if user ask a query we should return most relavent Tags/Keyword/Topic present in the Article based on Query**

I divided this task in to two parts:
1. Keyword Extraction
2. Query-Keyword Similarity check

For Keyword Extraction i used unsupervised machine learning based yake tool.

For Query-Keyword Similarity check, I used Zero-shot-Learning Pipeline. It can uses any transformer based model architecture trained on NLI/MNLI task. The objective of zero-shot-learning is to use state-of-the-art transformer based model without explicitly training it on domain/downstream task. NLI task makes generates understanding in model. It is popular for cross domain uses. 

My above two choices were to keep my approach domain independent. 

More details are available in the [notebook](Keyword_Extraction_and_Ranking.ipynb)

## 2. Article Ranking System:
Objective: **Given a Query and List of Articles return Top 5 relavent articles according to Query**

For this task i have used [bert-base-mdoc-hdct](https://huggingface.co/Luyu/bert-base-mdoc-hdct) model and MS-MARCO v1.1 dataset from Huggingface datasets. The model was giving **58.7853%** ranking precision on 1000 test samples.

More details are available in the [notebook](Query_Based_Article_Ranking.ipynb)


