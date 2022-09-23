# Real-World Applications of Synthetic Data

***
Challenges where synthetic data can help solving:

- Considering that predictive models trained on biased datasets can result in poor performance for organizations and their customers, one can generate samples of an under-represented category to unbias the dataset and improve the model's performance;
- Data shortage can be overcomed by expanding the dataset with synthetic data, which improves a model's stability and performance;
- Models can be break in production if nor properly validated due to population shifts, therefore unseen scenarios can be generated with synthetic data and used to test the model's performance and ensure its stability.

***

A predictive model trained on an imbalanced dataset vcan overfit on the majority class, especially when trained to maximize the total number of correctly predicted labels. *Synthetic data provides a simple and easy way to manipulate distributions and generate a rebalanced dataset, while preserving data privacy.*

One of the major benefits of data synthetic is to fulfill data privacy requirements, as well as to have a faster product development and testing.

<br>

Other notes:

- Data augmentation is a form of regularization, as it reduces dataset variance.
- For small datasets, small variations and outliers affect performance strongly, making the results unstable and highly variable on each train-test split.
