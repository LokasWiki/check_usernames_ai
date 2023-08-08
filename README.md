## Username Classification Model 👤🔍

This is a machine learning model that can classify usernames into two categories: spam and non-spam. The model is based on a deep learning architecture that uses a combination of embedding layers, LSTM layers, and fully connected layers. The input to the model is a string representing a username, and the output is a probability distribution over the two categories.

## Dataset 📊

The model was trained on a dataset of usernames that were manually labeled as spam or non-spam. The dataset contains approximately 50,000 usernames, with a roughly equal number of examples in each category.

## Performance 🏆

The model achieved an accuracy of 82% on the test set, and has been shown to generalize well to new data. However, as with any machine learning model, its performance may vary depending on the specific characteristics of the data.



## Usage 🚀
To use this model, you will need to install the Hugging Face library. You can do this by running the following command in your terminal:

```bash
pip install transformers
```

Once you have the library installed, you can use the model by following these steps:

1. Import the necessary libraries:

```python
from transformers import AutoTokenizer, AutoModelForSequenceClassification
import torch
```

2. Load the model and the tokenizer:

```python
tokenizer = AutoTokenizer.from_pretrained("lokas/spam-usernames-classifier")
model = AutoModelForSequenceClassification.from_pretrained("lokas/spam-usernames-classifier")
```

3. Tokenize your input:

```python
inputs = tokenizer("YourUsernameHere", return_tensors="pt")
```

4. Run the model:

```python
outputs = model(**inputs)
```

5. Interpret the output:

```python
probs = torch.nn.functional.softmax(outputs.logits, dim=-1)
print(probs)
```

This will print a probability distribution over the two categories (spam and non-spam). The first value corresponds to the probability that the username is non-spam, and the second value corresponds to the probability that the username is spam.

## License 📝

This project is licensed under the MIT License. See the LICENSE file for more details.

