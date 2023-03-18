## Username Classification Model

This is a machine learning model that can classify usernames into two categories: spam and non-spam. The model is based on a deep learning architecture that uses a combination of embedding layers, LSTM layers, and fully connected layers. The input to the model is a string representing a username, and the output is a probability distribution over the two categories.

## Dataset

The model was trained on a dataset of usernames that were manually labeled as spam or non-spam. The dataset contains approximately 50,000 usernames, with a roughly equal number of examples in each category.

## Performance

The model achieved an accuracy of 82% on the test set, and has been shown to generalize well to new data. However, as with any machine learning model, its performance may vary depending on the specific characteristics of the data.

## Usage

To use the model, you can simply load it into memory using the load_model function from the Keras library. You can then pass individual usernames to the model and obtain a prediction of the category to which they belong. We have also provided a tokenizer that can be used to preprocess the usernames before they are passed to the model.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
