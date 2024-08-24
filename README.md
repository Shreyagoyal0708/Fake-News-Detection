# Fake-News-Detector

## Overview
This project focuses on predicting whether a new is fake or real using IFND dataset combined with a chatbot which further suggests the related news. The dataset covers news pretraining to India. It was created by Indian fact checking websites.

## Dataset
The dataset used in this project is the IFND dataset. It contains both a training and a test set with multiple information about the news, labled fake or real.
A RelatedNews file is used as input for the chatbot to give the related news.

## Features
The dataset contains multiple features, including:

- `Date`: Date at which news was released.
- `Web`: The website from which the news is taken.
- `Category`: Different types of news (eg.Election, COVID-19)
  
Additionally, the dataset has a label column indicating whether a news is fake or real.

## Preprocessing
To prepare the data for machine learning models, the following steps were taken:
- **Label Encoding**: Categorical features like `Category`,'Date' and `Web` were converted into numeric form using label encoders.
- **TF-IDF Vectorization**: It converts the text data into numerical features that can be used by machine learning algorithms.

To prepare the data for chatbots,the following steps were taken:
- **Text Preprocessing**: It involves reading a text file, normalizing the text, and tokenizing it into sentences and words.
- **Tokenization**: It converts the text data into numerical features that can be used by machine learning algorithms.
- **Normalization**: It focuses on lemmatization(precess of converting the words to their root form) and punctuation removal.


## Model Training and Evaluation
Various models were trained to classify different attack categories. LinearSVC were used extensively due to their interpretability and effectiveness in dealing with complex features. Models were evaluated using the following metrics:

- **Confusion Matrix**: To understand misclassifications.
- **Cross_Val_Score**: To measure model performance on unseen data.

Trained TfidfVectorizer for the chatbot to find the related news from the text file.The following functions were made:

- **Response**: To take the input from the user and give the related news as the output.
- **Greet**: If the user greets the bot will greet back randomly from the list.

## Results and Findings
The project results include the following key outcomes:

- **Performance Metrics**: Accuracy and confusion matrices for each model.
- **Output**: Predicted if the news was fake with and accuracy of 94.8%.


## Contributing
Contributions are welcome. If you find a bug or want to add new features, feel free to open an issue or submit a pull request.
