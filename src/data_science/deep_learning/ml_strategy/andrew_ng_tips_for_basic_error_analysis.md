# Tips for basic error analysis

Error analysis refers to the process of examining dev set examples that your algorithm misclassified, so that you can understand the underlying causes of the errors. It can often help you figure out how promising different directions are, since manually examining a small subset (e.g., 100 examples) does not take that long and can save a huge amount of wasted time later. Notice that error analysis is also an iterative process.

Note: dev and train sets are **not** the same thing.

***

**Main tips:**

- Build your first system quickly, then iterate;
- Look at dev set examples to evaluate ideas and misclassified examples;
- The Eyeball dev set should be large enough to give you a sense of your algorithm’s major error categories (the same applies to a regular subset of misclassified examples).
  
***

<br> When performing error analysis in a large dev set, explicitly splitting your dev set into Eyeball (the examples you manually examine) and Blackbox (examples you don’t look at) dev sets allows you to tell when your manual error analysis is causing you to overfit the Eyeball portion of your data. In other words, if you see the performance on the Eyeball dev set improving much more rapidly than the performance on the Blackbox dev set, you have overfitted the Eyeball dev set.

<br> Error analysis might not be that useful on a task where humans don’t perform that well.
