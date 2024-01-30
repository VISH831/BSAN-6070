# CA02 - Spam Email Classifier using Naive Bayes

## Project Description
This project implements a Spam Email Classifier using the Naive Bayes supervised machine learning algorithm. The classifier is trained and tested on a dataset of emails, which are labeled as either 'Spam' or 'Not Spam'.

**IMPORTANT NOTE:**
The paths to the 'train-mails' and 'test-mails' data folders must be set as './train-mails' and './test-mails'. This setup ensures that the notebook and these folders are in the same directory, allowing for consistent execution across different environments.


## Library Imports
The project uses the following Python libraries <br>
- os <br>
- numpy <br>
- collections.Counter <br>
- sklearn (for the Naive Bayes algorithm and accuracy metrics). <br>

To install the sikit-learn library, run the following command: <br>
pip install scikit-learn

## Methodology and Code Descriptions
**Function: make_Dictionary**
- This function processes a collection of emails to create a list of the 3000 most common words, excluding non-alphabetical words and single characters, which serves as the feature set for spam email classification.

**Function: extract_features**
- This function reads emails from the specified directory and extracts features for use in a spam classifier. It creates a feature matrix based on the frequency of the most common words (as per the provided dictionary) in each email. It also assigns labels to the emails, marking them as spam or not spam based on their filenames. The feature matrix and the labels are used for training and evaluating the machine learning model.

**Training and Testing the Classifier**
- The Naive Bayes classifier is trained using the extracted features and labels from the training dataset. It is then tested on a separate test dataset to evaluate its accuracy in classifying emails as spam or not spam.
