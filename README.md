Key Components:

    Data Preparation:
        Dataset: The script reads a CSV file (text.csv) containing text samples and their corresponding emotion labels. Each text is assigned an emotion category represented as a numeric label.
        Text Vectorization: The TfidfVectorizer converts text data into numerical features suitable for machine learning models.

    Model Definition:
        Naive Bayes (MultinomialNB): A probabilistic model well-suited for text classification tasks.
        Support Vector Machine (SVC): A powerful model for classification in high-dimensional spaces, using a linear kernel and probability estimates.
        Logistic Regression: A straightforward model for binary and multi-class classification problems.

    Ensemble Learning:
        Voting Classifier: Combines the predictions of multiple models (Naive Bayes, SVM, and Logistic Regression) using soft voting. Soft voting averages the probabilities predicted by each model and selects the class with the highest average probability.

    Model Training and Evaluation:
        Training: The ensemble model is trained on a subset of the data, and predictions are made on a held-out test set.
        Evaluation: The script calculates and prints the accuracy and classification report, providing insights into the model's performance across different emotion categories.

    Interactive Prediction:
        User Input: The script provides an interactive command-line interface allowing users to input text sentences for emotion prediction. It outputs the predicted emotion based on the ensemble model’s collective decision.

Usage Instructions:

    Save the Script: Save the provided code as emotion_analysis_ensemble.py.
    Prepare Data: Ensure your dataset (data.csv) is formatted with columns text and label and is located in the same directory as the script.
    Install Dependencies: Install the required Python libraries using:
    scikit learn 
    Enter Sentences: Use the interactive input to enter text and receive emotion predictions. Type 'exit' to terminate the interactive session.

Benefits:

    Enhanced Accuracy: By combining multiple models, the ensemble approach leverages diverse strengths, potentially improving overall classification accuracy.
    Flexibility: The interactive component allows for real-time predictions on user-provided text data.

This ensemble-based approach helps to address the limitations of individual models by aggregating their predictions, thereby offering a more accurate and reliable emotion classification system.
