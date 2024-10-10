The **softmax function** is a mathematical function that converts a vector of raw scores (logits) from a model into a probability distribution over multiple classes. It is commonly used in the output layer of multiclass classification models.

### Key Properties:

1. **Range**: The output probabilities range between 0 and 1.
2. **Sum to One**: The sum of the output probabilities equals 1, making them interpretable as probabilities.
3. **Sensitivity to Scores**: Higher input scores lead to higher probabilities, allowing the model to favor certain classes over others.

The softmax function is particularly useful in multiclass classification tasks, where it helps in determining the likelihood of each class based on the model's predictions.

![[Pasted image 20241009164538.png]]