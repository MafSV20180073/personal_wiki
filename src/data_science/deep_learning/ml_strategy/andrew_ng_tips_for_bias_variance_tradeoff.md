# Tips for bias-variance tradeoff

An algorithm exhibiting high bias but a low variance is said to be <u>underfitting</u>. Adding more training data to reduce avoidable bias is not helpful.

***

**Tips when (high avoidable) bias is a source of error:**

- Increase the size of your model (neurons, layers, …);
- Modify model architecture - use academic literature as a source of inspiration to find new models and architectures;
- Modify input features based on insights from error analysis;
- Reduce or eliminate regularization;
- Carry out error analysis on the training data;
- When the training set performance is already close to the optimal error rate, there isn’t much room for improvement in terms of bias or in terms of training set performance;
- Your algorithm must perform well on the training set before you can expect it to perform well on the dev/test sets.
  
***

<br><br><br><br>An algorithm exhibiting high variance but low bias is said to be <u>overfitting</u>.

***

**Tips when (high avoidable) variance is a source of error:**

- Add more data to your training set;
- Use regularization techniques;
- Add early stopping;
- Feature selection to decrease the number and/or type of input features;
- Decrease the model size;
- Modify input features based on insights from error analysis;
- Modify model architecture.
  
***

It is common that making our models more complex will reduce the bias but will also increase variance, or adding regularization techniques will reduce variance but increase bias - Bias vs. Variance tradeoff. <b>Our ultimate goal is to get an algorithm with low bias and low variance.</b>

Regarding the feature selection topic, reducing significantly the number of input features is more likely to have a significant effect than reducing the number of features slightly, as long as you are not excluding too many useful features. Sometimes, within the context of deep learning, feature selection has little to no impact. However, when your training set is small, feature selection can be very useful.
