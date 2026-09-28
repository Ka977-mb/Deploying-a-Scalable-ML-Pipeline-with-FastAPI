# Model Card

For additional information see the Model Card paper: https://arxiv.org/pdf/1810.03993.pdf

## Model Details

This project uses a Random Forest classification model to predict whether a person's salary is greater than $50K or less than or equal to $50K. The model was trained using scikit-learn. Categorical features were processed with one-hot encoding before training.

## Intended Use

The model is intended for this educational machine learning project to demonstrate data preprocessing, model training, inference, model evaluation, and deployment through a REST API. It is not intended to make real-world employment, financial, or other high-impact decisions about individuals.

## Training Data

The model was trained using the Census dataset provided with the project. The dataset contains demographic and employment-related features such as age, workclass, education, marital status, occupation, relationship, race, sex, hours worked per week, and native country. The target variable is salary, which contains the classes >50K and <=50K.

The dataset was split into training and testing datasets. Eighty percent of the data was used for training and 20 percent was used for testing. Categorical features were transformed using one-hot encoding.

## Evaluation Data

The evaluation data consists of the 20 percent test portion of the Census dataset that was not used to train the model. The model was also evaluated on slices of categorical features to examine its performance for different values within those features.

## Metrics

The model was evaluated using precision, recall, and F1 score.

The model achieved a precision of 0.7353, recall of 0.6378, and F1 score of 0.6831 on the test dataset.

Precision measures how many of the samples predicted as the positive salary class were correct. Recall measures how many of the actual positive samples were correctly identified. The F1 score provides a balance between precision and recall.

## Ethical Considerations

The Census dataset contains demographic characteristics such as race and sex. Model performance may differ across demographic groups because of patterns and biases present in the data. Predictions from this model should therefore not be used to make decisions that could negatively affect individuals. The model is being used only for educational purposes in this project.

## Caveats and Recommendations

The model was trained on the Census dataset and may not represent current populations or economic conditions. Its predictions should not be generalized to other datasets or populations without additional testing. Performance should continue to be evaluated across different data slices, and additional approaches could be explored to improve recall and overall model performance.