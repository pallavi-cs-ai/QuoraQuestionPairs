# Semantic Duplicate Question Detection
An end-to-end Natural Language Processing (NLP) application that identifies semantically similar questions using classical machine learning techniques. The system combines advanced text preprocessing, feature engineering, and supervised learning models, and is deployed through a Django web application.

## Project Overview

Large Q&A platforms frequently contain duplicate questions expressed using different wording.

This project builds an end-to-end semantic duplicate-question detection pipeline using the Quora Question Pairs dataset. The solution performs NLP preprocessing, engineers interpretable textual similarity features, evaluates multiple machine learning models, and serves predictions through a Django-based web application.

## Tech Stack

- Python
- Django
- Scikit-learn
- XGBoost
- NLTK
- Pandas
- NumPy

## System Architecture

The application follows a complete machine learning workflow from user input through preprocessing, feature engineering, model inference, and real-time prediction delivery.

<img width="1536" height="1024" alt="ChatGPT Image Jun 26, 2026, 07_01_46 PM" src="https://github.com/user-attachments/assets/9d7de622-6bfe-4e05-b926-1217fe0065c7" />

## NLP Pipeline

### Text Preprocessing

- Acronym expansion
- Token normalization
- Stopword handling
- Semantic stopword retention
- Stemming
- Unit normalization

### Feature Engineering

- TF-IDF
- Bag-of-Words
- Cosine Similarity
- Digit Matching
- Mathematical Expression Similarity

### Model Evaluation

Compared

- Random Forest
- Naive Bayes
- SVM
- XGBoost

Evaluation Metrics

- Accuracy
- Log Loss
- F1 Score


###  Dataset: https://www.kaggle.com/c/quora-question-pairs/data
  The dataset used for this analysis was provided by  Quora , released as their first public dataset as described above. 
  It consists of  404352  question pairs in a tab-separated format:
•    id :   unique identifier for  the question pair
•    qid1 :   unique  identifier for the  first  question
•    qid2 :   unique  identifier for the  second  question
•    question1 : full  unicode  text  of  the first  question
•    question2 : full  unicode  text  of the  second question
•    is_duplicate : label 1 if questions are duplicates,  0  otherwise

### Project Structure :
   -  **Cleaning.py**
      Performs NLP preprocessing including spelling correction, stemming, stopword handling, acronym expansion, and token normalization.
     
   -  **Features.py**
      Extracts textual similarity features including TF-IDF, Bag-of-Words, cosine similarity, and engineered semantic features used for model
      training.
      
   -  **ConnectionFront.py**
      Handles incoming user requests from the Django application, performs inference using the trained model, and renders duplicate-question
      predictions.

 ### Results

  The trained models were evaluated using:
  
  - Accuracy
  - Log Loss
  - F1 Score
  
  XGBoost achieved the strongest overall predictive performance among the evaluated classical machine learning models.

 ### Application Demo :
 **Similar Question** 
   
   <img src="./similarquestion.png" data-canonical-src="./similarquestion.png" width="400" height="400" ALIGN=”left” 
   style="border: #00008B 4px solid;" />  
    
 **No duplicate Questions found** 
      
   
   <img src="./Nopresent.png" data-canonical-src="./Nopresent.png" width="400" height="400" ALIGN=”left”           style="border: #00008B 4px solid;" />
     
     
  **Console Results**
    
   <img src="./consoleResults.png" data-canonical-src="./consoleResults.png" width="800" height="400" ALIGN=”left” 
  style="border: #00008B 4px solid;" />

   
