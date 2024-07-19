
# Sarcasm Detection in IMDb Movie Reviews

Online reviews hold immense power in the film industry, shaping audience perception and box office success. However, sarcasm a common weapon in the reviewer's arsenal, can wreak havoc on sentiment analysis systems. These automated tools struggle to decipher sarcastic intent, leading to misinterpretations that can skew audience ratings, mislead studios, and ultimately, disappoint moviegoers.

![Sarcasm](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQh2oNie2NZjxi-5yhoj__Og7FtVcuTz2pS4A&s)

## Dataset

 - [IMDb Dataset](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews)

![data.png]()

 
## Scope of the Solution


In-scope:
- Developing a sarcasm detection model specifically for English-language IMDb reviews.
- Evaluating model performance using a curated dataset of IMDb reviews.
- Focusing on text-based reviews, excluding multimedia content.

Out-of-scope:
- Detecting sarcasm in non-English reviews.
- Handling non-textual sarcasm (e.g., in images or videos or memes)
- Real-time detection of sarcasm during review submission. 

## Model Selection 

Why Use RoBERTa for Sarcasm Detection?

RoBERTa (Robustly optimized BERT approach) is an extension of BERT (Bidirectional Encoder Representations from Transformers) designed to achieve better performance on a variety of NLP tasks, including sarcasm detection. Here are some reasons why RoBERTa might be particularly effective for your sarcasm detection in movie reviews

**Higher Capacity** :
- RoBERTa has more parameters compared to many other models, which allows it to capture complex patterns in the data, including the subtle cues associated with sarcasm.

**Pre-trained on Large Datasets** :
- RoBERTa is pre-trained on larger and more diverse datasets compared to other models like BERT. This extensive pre-training allows RoBERTa to capture a richer understanding of language nuances, including sarcasm.

**Dynamic Masking** :
- Unlike BERT, which uses static masking during pre-training, RoBERTa employs dynamic masking. This means the model sees different masked tokens during each epoch of training, leading to better generalization and robustness.



## Model Evaluation

**Accuracy and Overall Performance**:
- The RoBERTa model achieved an overall accuracy of 85.69%, which is a strong result for sarcasm detection in movie reviews.
- The model shows balanced performance across both classes (Sarcastic and Not Sarcastic), indicating that it does not heavily favor one class over the other.

**Class-wise Performance**:
- **Not Sarcastic**
  1. **Precision** : 0.83, which means that 83% of the reviews predicted as "Not Sarcastic" are actually "Not Sarcastic."
  2. **Recall** : 0.90, indicating that the model correctly identifies 90% of the actual "Not Sarcastic" reviews.
  3. **F1-Score** : 0.86, reflecting a good balance between precision and recall for this class.

- **Sarcastic**
  1. **Precision** : 0.89, meaning 89% of the reviews predicted as "Sarcastic" are indeed sarcastic.
  2. **Recall** : 0.82, showing that the model successfully detects 82% of the actual "Sarcastic" reviews.
  3. **F1-Score** : 0.85, demonstrating a high level of accuracy in both identifying and correctly classifying sarcastic reviews.

**Macro and Weighted Averages**:
The macro average (0.86) and weighted average (0.86) for precision, recall, and F1-score are the same, underscoring the model's balanced performance across both classes.




**Interpretation**:
- The RoBERTa model's high precision and recall values for both classes suggest that it is very effective at distinguishing between sarcastic and non-sarcastic reviews.
- The balanced F1-scores indicate that the model is equally proficient at minimizing false positives and false negatives, which is crucial for a nuanced task like sarcasm detection.
- With an accuracy close to 85%, the RoBERTa model is a reliable choice for your sarcasm detection task, surpassing the performance of simpler models like neural networks, CNNs, and LSTMs.

## Conclusion:
The RoBERTa model's performance highlights its robustness and effectiveness in handling the complexities of sarcasm detection in movie reviews. Its ability to achieve high precision, recall, and F1-scores for both sarcastic and non-sarcastic classes makes it a superior model for this task.

