# Tips for dev and test sets

Concepts: train set, dev set, test set.

***

**Main tips:**

- Choose dev and test sets to reflect data you expect to get in the future;
- Your dev and test sets should come from the same distribution;
- Whenever possible, a dev set should be large enough to detect improvements and meaningful changes in an algorithm’s performance;
- When starting out a new project, coming up with an initial dev/test set should usually take no longer than 1 week (<u>guideline</u>);
- If it is detected that the dev/test set is missing the mark then by all means change them quickly.
  
***

<br> Having mismatched dev and test sets introduces additional uncertainty about whether improving on the dev set distribution also improves test set performance. It also makes it harder to figure out what is and isn’t working, and thus makes it harder to prioritize what to work on.

<br> Regarding the size of the dev set, consider the dev set A with 100 samples and the dev set B with 10k samples. There’s a good chance of detecting an improvement of 0.1% with the dev set B, contrary to the dev set A.

<br> Notice that the process of repeatedly evaluating ideas on the dev set can cause your algorithm to gradually “overfit” to the dev set. If you find that your dev set performance is much better than your test set performance, it is a sign that you have overfitted to the dev set.

<br> Finally, if you had overfit the dev set, get more dev set data.
