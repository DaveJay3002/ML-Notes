**Precision**: In machine learning and classification, precision is the ratio of correctly predicted positive instances to the total predicted positive instances. It answers the question: "Of all the instances classified as positive, how many were actually positive?"

**Recall**: Recall (also known as sensitivity or true positive rate) is the ratio of correctly predicted positive instances to all actual positive instances. It answers the question: "Of all the actual positive instances, how many were correctly identified?"

![[Pasted image 20241010133011.png]]
![[Pasted image 20241010134220.png]]

# F1 Score
The **F1 Score** is the harmonic mean of precision and recall, providing a single metric that balances both. It is particularly useful when there is an uneven class distribution or when both precision and recall are important. The F1 Score is calculated as:

F1=2×Precision+Recall  / Precision×Recall​

The **F1 score** is used because it provides a balanced measure of a model’s performance by combining both **precision** and **recall** into a single metric. It is especially useful in situations where:

1. **Imbalanced Datasets**: When one class is more frequent than the other, accuracy alone can be misleading. F1 score focuses on the performance of the minority class.
    
2. **Trade-off between Precision and Recall**: In cases where improving precision decreases recall or vice versa, the F1 score helps to find a balance between the two.
    
3. **Avoiding Overly Optimistic Metrics**: Since the F1 score is the harmonic mean, it prevents the overestimation of performance when either precision or recall is significantly low.