# Summary Report: Logistic Regression vs. XGBoost for CTR Prediction

## Overview

This report provides a comparison between the performance of a Logistic Regression model and an XGBoost model used for predicting click-through rates (CTR) in online advertising. Each model's metrics, strengths, and areas for improvement are discussed based on their respective classification reports and confusion matrices.

## Model Performance Comparison

### Logistic Regression Model

**Metrics:**

- Accuracy: 0.72
- Precision: 0.73
- Recall: 0.68
- F1-Score: 0.70

**Confusion Matrix:**

```
[[1169  374]
 [ 462  995]]
```

**Observations:**

- The model achieved an accuracy of 72%, indicating that it correctly predicted 72% of the total instances.
- Precision of 0.73 suggests that when the model predicts a positive class (e.g., a user will click on an ad), it is correct 73% of the time.
- Recall of 0.68 indicates that the model identifies 68% of actual positive cases, showing that there is room for improvement in capturing all positive instances.
- The F1-score of 0.70 shows a moderate balance between precision and recall, but there is potential for enhancement.
- The confusion matrix highlights 462 false negatives and 374 false positives, implying that the model has difficulty in correctly predicting some positive and negative cases.

**Strengths:**

- Decent precision for initial predictions.
- A simple and interpretable model that can be fine-tuned further.

**Areas for Improvement:**

- Improve recall by reducing false negatives.
- Address false positives to increase precision.
- Use feature engineering, regularization tuning, or data balancing techniques for better results.

### XGBoost Model

**Metrics:**

- Accuracy: 0.882
- Precision (Class 0): 0.881
- Recall (Class 0): 0.887
- Precision (Class 1): 0.883
- Recall (Class 1): 0.877
- F1-Score (Overall): 0.882

**Confusion Matrix:**

```
[[ 899  115]
 [ 121  865]]
```

**Observations:**

- The XGBoost model achieved a high accuracy of 88.2%, indicating better performance compared to the logistic regression model.
- Precision and recall for both classes are balanced, with both scoring around 88%, showing strong predictive capability.
- The F1-score of 0.882 confirms that the model maintains a good balance between precision and recall.
- The confusion matrix shows 121 false negatives and 115 false positives, indicating fewer misclassifications compared to the logistic regression model.

**Strengths:**

- High accuracy and balanced precision and recall.
- Robust to various data distributions and effective at capturing complex relationships in the data.

**Areas for Improvement:**

- Although performance is high, further hyperparameter tuning and feature engineering could push the model closer to optimal performance.
- Ensure that the model's complexity does not lead to overfitting, especially when deployed in real-world applications.

## Conclusion

The XGBoost model outperforms the Logistic Regression model in terms of accuracy, precision, recall, and F1-score. It shows strong performance across both classes with fewer misclassifications.

The Logistic Regression model, while less accurate, provides a simpler and more interpretable solution that could be enhanced with additional feature engineering and hyperparameter tuning.

## Recommendations

- For high-stakes applications where accuracy and recall are critical, the XGBoost model is preferable due to its higher performance.
- For simpler, more interpretable models, Logistic Regression can still be considered but may require further adjustments to improve recall and overall F1-score.

## Future Work

Future work could involve combining both models in an ensemble or leveraging techniques such as feature selection and data augmentation to enhance predictive power.
