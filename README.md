# MBTI-Personality-Type-Classification-using-BERT

Project Overview
This project aims to predict one of the 16 MBTI personality types based on a collection of user posts.

Dataset: Each sample contains 50 different posts from a single user, capturing various emotions, situations, and timeframes.

Challenge: Multi-class classification into 16 distinct categories with significant class imbalance.

 Methodology: Fine-Tuning BERT
We employed Fine-Tuning on a pre-trained BERT (Bidirectional Encoder Representations from Transformers) model. BERT is ideal for this task as it captures deep bidirectional context, which is crucial for understanding the subtle psychological nuances in personal posts.

 Current Results & Analysis
Current Accuracy: 64.0%

Analysis: While 64% is significantly higher than a random baseline (6.25%), the model's performance is currently limited by class imbalance. Some personality types are overrepresented in the dataset, leading to biased predictions.

 Future Work & Improvements
To push the accuracy beyond 64%, the following strategies are planned:

Addressing Class Imbalance:

Oversampling/Undersampling: Balancing the dataset to give equal weight to rare personality types.

Weighted Loss: Implementing class weights in the CrossEntropyLoss function.

Focal Loss: To focus the model's learning on "hard" examples and underrepresented classes.


 Tech Stack
Model: BERT (HuggingFace Transformers)

Framework: PyTorch

Optimization: AdamW with linear schedule
