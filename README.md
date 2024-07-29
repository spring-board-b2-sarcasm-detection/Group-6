
# Sarcasm Detection in IMDb Movie Reviews

##**Business Problem**
- The movie industry heavily relies on audience reviews for a film's success in theaters.
- Understanding and analyzing these reviews is crucial for providing accurate ratings and overall opinions on movies
- However, some reviewers express their thoughts sarcastically, which can mislead traditional sentiment analysis models.

##**Solution Proposed**

- To address the challenge of sarcasm detection, we need to develop and implement deep learning models specifically designed to recognize and interpret sarcastic reviews.
- By incorporating sarcasm detection into sentiment analysis, we can significantly enhance the accuracy of review analysis.


![Sarcasm](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQh2oNie2NZjxi-5yhoj__Og7FtVcuTz2pS4A&s)

![workflow_1.jpg]![workflow_1](https://github.com/user-attachments/assets/1d0b52e0-0f79-4e1f-88ca-6b13c10bff5f)



## Dataset

 - [IMDb Dataset](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews)
 
## Scope of the Solution
In-scope:
- Developing a sarcasm detection model specifically for English-language IMDb reviews.
- Evaluating model performance using a curated dataset of IMDb reviews.
- Focusing on text-based reviews, excluding multimedia content.

Out-of-scope:
- Detecting sarcasm in non-English reviews.
- Handling non-textual sarcasm (e.g., in images or videos or memes)
- Real-time detection of sarcasm during review submission. 

Steps followed to achive the solution

## **1. DATA PREPARATION**

The input Dataset reviews are analysed and following opeartions on the dataset:

1.  Removing duplicate reviews.

2.  Removing Null valued labels.

3.  Handling the label column for uniformity.

4.  Analysing the length of reviews and no.of unique labels in the dataset.

5.  Spliting the dataset into Train , Test , Validation data for further model trainings


**Length of reviews**

![length of reviews.jpg]![image](https://github.com/user-attachments/assets/8f024d62-b0db-4add-a3fa-91aa861063dc)


**no.of unique labels**

![labels count.jpg]![image](https://github.com/user-attachments/assets/46366fee-72ea-4ca6-ad97-831f2f5bee11)



**Split of data into Train , Test , Validation data**

![datset split.jpg]![image](https://github.com/user-attachments/assets/d0629260-5035-495b-b6d8-bc53f50481b6)


## **2. DATA CLEANING**

Cleaning the input Dataset reviews by performing the following steps:

1.  Removing HTML tags from reviews.

2.  Removing URLs from reviews.

3.  Removing specified punctuation marks from reviews.

4.  Removing extra white spaces from reviews.


# **3. DATA PREPROCESSING**

We will follow the following methods in order for preprocessing the data :


1.   Stop words removal
2.   Lemmatization
3.   Tokenization
4.   Input data Embeddings
5.   Checking for dataset imbalance

# **4. Model Training**
![model architecture]![image](https://github.com/user-attachments/assets/b0dd27d4-e624-4769-bf51-d69171b07823)

- Among the various ML models like  logistic regression, Naive Bayes, decision tree, Random Forest and few deep learning model like  Neural Networks (NN), Convolutional Neural Networks (CNN), Long Short-Term Memory (LSTM), Gated Recurrent Unit (GRU), and BERT models , GRU model stood out best for our dataset

- A Gated Recurrent Unit (GRU) is a type of recurrent neural network (RNN) architecture designed to handle sequential data and address the vanishing gradient problem found in traditional RNNs.

The Gated Recurrent Unit (GRU) model offers several advantages in deep learning, especially for handling sequential data:

- **Simpler Architecture**: GRUs have a straightforward design with fewer gates, which makes them easier to implement and understand.

- **Efficient Training**: The simplicity of GRUs leads to faster training times, allowing for quicker model development and experimentation.

- **Long-Term Dependencies**: GRUs are effective at capturing long-term dependencies in sequential data, helping to maintain important information over longer sequences.

- **Memory Efficiency**: The reduced number of parameters in GRUs results in lower memory usage, making them suitable for deployment in environments with limited resources.

- **Good Performance**: GRUs generally achieve strong performance across a wide range of sequence modeling tasks, including natural language processing, time series analysis, and speech recognition.

##**Conclusion**
- The GRU-based model demonstrates strong performance, achieving an overall accuracy of 82% on the dataset, with balanced precision and recall across both classes.

