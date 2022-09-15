# Tips for metrics choice and optimization

***

**Main tips:**

- Establish a single-number evaluation metric for your team to optimize;
- In the case of existing 2 or more metrics that are important, use a single metric that combines those metrics so your team ends up with a single number;
- If needed, distinguish between a satisficing metric and an optimizing metric;
- When starting out a new project, choosing an initial metric should take no longer than 1 week (<u>guideline</u>);
- If it is detected that the chosen metric is missing the mark then by all means change it quickly;
- The team should trust the metric so the best model is automatically chosen instead of curating them manually.  
  
***

<br> One of the examples regarding combining metrics into a single number metric is precision and recall - you can calculate f1-score instead. Averages and weighted averages of metrics are also an option to combine multiple metrics into one (e.g., an average accuracy of a classifier on n classes).

<br> Satisficing metrics are required to meet a certain value (e.g., running time equal to or smaller than 100 ms; the binary file size of the model must not surpass 25 KB). The optimizing metric is the number we want to maximize or minimize.

<br> Regarding picking a new metric to replace another one that was failing at choosing the best algorithm for the product: pick a new metric and use it to explicitly define a new goal for the team, rather than proceeding for too long without a trusted metric and reverting to manually choosing among models.

<br> It’s pretty common to change dev/test sets or evaluation metrics during a project - it’s not a big deal. Just change them if needed and make sure your team knows about the new direction.
