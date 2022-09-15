# Tips to address the data mismatch problem

***

**Main tips:**

- Try to understand what properties of the data differ between the training and the dev set distributions;
- Try to find more training data that better matches the dev set examples that your algorithm has trouble with (i.e., make the training data more similar to the dev/test data);
- Artificial data synthesis.

***

<br> When an algorithm generalizes well to new data drawn from the same distribution as the training set, but not to data drawn from the dev/test distribution, it means the training set data is a poor match for the dev/test set data - <u>data mismatch problem</u>.

<br> There is also some research on “domain adaptation” - how to train an algorithm on one distribution and have it generalize to a different distribution. These methods are typically applied only on special types of problems and are much less widely used than the previous tips.
