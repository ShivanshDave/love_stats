# Answering a Question about Question 5

**A student asked**:

> In Q5 Lambda = -0.29, which is closer to -0.5 than to zero. Shouldn't we go with inverse square root instead of log for Q6? 

**Here's my response**:

1. You probably want to get away from the notion that there is ever going to be one "correct" transformation, just in the way that there is never one "correct" model. All models are wrong, some are useful. 

2. Box-Cox is meant to identify useful transformations that may lead to useful models - the point estimate provides a false precision here.
    - The fact that the point estimate of lambda is closer to -0.5 than to zero is essentially irrelevant to the question of whether there is a meaningful difference in the quality of adherence to the complete set of regression assumptions between the inverse square root and the logarithm. The tool simply isn't anywhere near that precise (so that, for example, if the value was -0.2 instead of -0.3, that wouldn't imply anything substantial at all.) 
    - I say this knowing that the likelihood ratio test comparing a value of -0.29 is likely to suggest that using that value (-0.29) is statistically significantly better than using 0, in part because the large sample size means that the test will find even small differences to be significant, and in part because that doesn't address the question of using -0.5 rather than 0, for which it's probably important to note that -0.29 also looks statistically significantly better than -0.5 if you try that out using the `powerTransform` and `testTransform` functions in the `MASS` package (the 95% Wald test bounds turn out to be -0.41 and -0.16.)

3. The inverse square root is meaningfully harder to interpret than is the logarithm.

As the Hint suggests, the choice of transformation (among the five power transformations we actually understand easily - the square, the raw data, the square root, the log and the inverse) is straightforward. And so, we'll use a logarithm.

Thanks for asking, TEL
