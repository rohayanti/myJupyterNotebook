### Cost Function in Multi-Class Classification

The cost function, also known as the loss function or objective function, is a crucial component in training machine learning models. It measures how well the model's predictions match the actual target values. In multi-class classification tasks, where the output can belong to one of several classes (e.g., red, green, blue), the cost function quantifies the difference between the predicted probabilities and the true labels.

#### Example:

Let's consider a multi-class classification problem where we have a dataset of fruits and their corresponding colors: "red," "green," and "blue." We want to use a neural network with the softmax activation function in the output layer to classify the fruits into these three color categories based on their features.

Suppose we have a single sample (fruit) and its corresponding true color label:

```python
# True label for the fruit (one-hot encoded)
true_label = [0, 1, 0]  # [red, green, blue]
```

After passing this sample through the neural network and applying the softmax function, we obtain the predicted probabilities for each class:

```python
# Predicted probabilities (output of the softmax function)
predicted_probabilities = [0.3, 0.6, 0.1]  # [red, green, blue]
```

The cost function quantifies the difference between the predicted probabilities and the true label. One common cost function for multi-class classification is the cross-entropy loss (also known as the log loss). The formula for the cross-entropy loss for a single sample is as follows:

```
CE = -Σ(true_label_i * log(predicted_probabilities_i))
```

where `CE` is the cross-entropy loss, `true_label_i` is the true probability (1 or 0) for class i, and `predicted_probabilities_i` is the predicted probability for class i.

Using the formula, let's calculate the cross-entropy loss for our example:

```python
import numpy as np

def cross_entropy_loss(true_label, predicted_probabilities):
    return -np.sum(true_label * np.log(predicted_probabilities))

# Calculating cross-entropy loss for the example
ce_loss = cross_entropy_loss(np.array(true_label), np.array(predicted_probabilities))
print("Cross-Entropy Loss:", ce_loss)
```

The output will be:

```
Cross-Entropy Loss: 0.5108256237659907
```

**Interpreting the results:**

The cross-entropy loss for this example is approximately 0.5108. The lower the cross-entropy loss, the better the model's predictions align with the true labels. In this case, the loss indicates how much the predicted probabilities differ from the true probabilities.

In Markdown format:

### Cost Function in Multi-Class Classification

The cost function, also known as the loss function or objective function, is a crucial component in training machine learning models. It measures how well the model's predictions match the actual target values. In multi-class classification tasks, where the output can belong to one of several classes (e.g., red, green, blue), the cost function quantifies the difference between the predicted probabilities and the true labels.

#### Example:

Consider a multi-class classification problem where we have a dataset of fruits and their corresponding colors: "red," "green," and "blue." We want to use a neural network with the softmax activation function in the output layer to classify the fruits into these three color categories based on their features.

Suppose we have a single sample (fruit) and its corresponding true color label:

```python
# True label for the fruit (one-hot encoded)
true_label = [0, 1, 0]  # [red, green, blue]
```

After passing this sample through the neural network and applying the softmax function, we obtain the predicted probabilities for each class:

```python
# Predicted probabilities (output of the softmax function)
predicted_probabilities = [0.3, 0.6, 0.1]  # [red, green, blue]
```

The cost function quantifies the difference between the predicted probabilities and the true label. One common cost function for multi-class classification is the cross-entropy loss (also known as the log loss). The formula for the cross-entropy loss for a single sample is as follows:

```
CE = -Σ(true_label_i * log(predicted_probabilities_i))
```

where `CE` is the cross-entropy loss, `true_label_i` is the true probability (1 or 0) for class i, and `predicted_probabilities_i` is the predicted probability for class i.

Using the formula, let's calculate the cross-entropy loss for our example:

```python
import numpy as np

def cross_entropy_loss(true_label, predicted_probabilities):
    return -np.sum(true_label * np.log(predicted_probabilities))

# Calculating cross-entropy loss for the example
ce_loss = cross_entropy_loss(np.array(true_label), np.array(predicted_probabilities))
print("Cross-Entropy Loss:", ce_loss)
```

The output will be:

```
Cross-Entropy Loss: 0.5108256237659907
```

**Interpreting the results:**

The cross-entropy loss for this example is approximately 0.5108. The lower the cross-entropy loss, the better the model's predictions align with the true labels. In this case, the loss indicates how much the predicted probabilities differ from the true probabilities.
