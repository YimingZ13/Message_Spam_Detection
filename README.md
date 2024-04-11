# Message_Spam_Detection

## Table of Contents
1. [Introduction](#Introduction)
2. [File Structure](#FileStructure)
3. [Installing](#Installing)
4. [Feature Documentations](#FeatureDocumentations)
5. [Key Results](#KeyResults)
6. [Authors](#Authors)
7. [License](#License)

<a name="Introduction"></a>
## Introduction

In the digital age, our inboxes are inundated with a mix of essential communications and unsolicited spam messages. Sorting through them manually is not just cumbersome, it's also inefficient. This is where the Spam Detection Project comes into play, combining the power of machine learning and natural language processing to filter out the noise and prioritize meaningful communication.

This project harnesses the strengths of two highly effective machine learning models: the Support Vector Classifier (SVC) and Naive Bayes. These models are trained to distinguish between spam and non-spam emails (often referred to as "ham") by learning from patterns in a large corpus of labeled data.

To enhance the performance of these models, I employed Term Frequency-Inverse Document Frequency (TF-IDF). TF-IDF is a statistical measure used to evaluate the importance of a word in a document relative to a collection of documents, i.e., the corpus. By converting the raw text into a TF-IDF vectorized form, it gives the models a nuanced understanding of text data, emphasizing words that are unique and thus more informative for classification tasks.

The versatility of SVC, with its ability to model non-linear boundaries, and the probabilistic approach of Naive Bayes, particularly its efficiency with high-dimensional data, make for a potent combination in tackling the complexity of spam detection. Whether it's detecting the latest phishing attempt or filtering out irrelevant advertisements, this project is designed to adapt and respond to the ever-evolving landscape of digital threats.

The [original datasets](https://archive.ics.uci.edu/dataset/228/sms+spam+collection).

<a name="FileStructure"></a>
## File Structure
Each of the following project steps is completed in a separate notebook:
- [Data Cleaning and EDA](https://github.com/YimingZ13/Message_Spam_Detection_with_SVC_Naive_Bayes/blob/main/spam_cleaning_eda.ipynb): `spam_cleaning_eda.ipynb`
- [Data Preprocessing and Modelling](https://github.com/YimingZ13/Message_Spam_Detection_with_SVC_Naive_Bayes/blob/main/spam_preprocessing_modelling.ipynb): `spam_preprocessing_modelling.ipynb`

<a name="Installing"></a>
## Installing
There are no special packages needed for this project, most of packages come with the Anaconda distribution of Python 3.

<a name="FeatureDocumentations"></a>
## Feature Documentations
`spam.csv`:
- `v1`：The label (ham or spam).
- `v2`: The raw message texts.
  
<a name="KeyResults"></a>
## Key Results

<img src="https://github.com/YimingZ13/Message_Spam_Detection_with_SVC_Naive_Bayes/blob/main/confusion_matrics/Screenshot%202024-04-11%20at%2012.26.19%20AM.png" width="500" height="350">
<img src="https://github.com/YimingZ13/Message_Spam_Detection_with_SVC_Naive_Bayes/blob/main/confusion_matrics/Screenshot%202024-04-11%20at%2012.26.27%20AM.png" width="500" height="350">

- The best performed model were SVC (F1: 0.92) and Naive Bayes (F1: 0.91) model.
- While both models show high performance, the SVC model has a slightly better balance between precision and recall, resulting in a higher F1 Score.
- If minimizing false negatives is more important, the SVC model is preferable due to its higher recall.
- If precision is more critical (minimizing the risk of marking legitimate emails as spam), the NB model has a slight edge, though the difference is minimal.



<a name="Authors"></a>
## Authors
Yiming Zhao | [LinkedIn](https://www.linkedin.com/in/yiming-zhao13/)

<a name="License"></a>
## License
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
