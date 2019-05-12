# Visualizing high dimentional data
The 'Apply function to Series and DataFrame' python file is based on Ritchie Ng's work where map() and applymap() has been explained.
t-SNE : t-distributed stochastic neighbor embedding
What is t-SNE?
(i) a technique of non linear dimentionality reduction and visualization of multi-dimentional data,
(ii) normal distribution is replaced with t-distribution,
(iii) some improvements have been made in finding of local minima.

Where to use t-SNE?
-to visualise any high dimentional data

MATH behind it
(i) each data is a vector with high dimentionality,
(ii) at the end we need new dataset in 2D or 3D space,
(iii) BUT each data point needs to maintain the structure and patterns that existed in the ioriginal dataset.

1. Transformation of multi-dimentional Euclidean distance between data points into conditional pronbabilities, that reflects a relationship between points.

2. σ-must be chosen for each data point. It is chosen using perplexity.
NOTE : What is perplexity?
In information theory, perplexity is a measurement of how well a probability distribution or probability model predicts a sample. It may be used to compare probability models. A low perplexity indicates the probability distribution is good at predicting the sample.The perplexity of a discrete probability distribution p is defined as
{\displaystyle 2^{H(p)}=2^{-\sum _{x}p(x)\log _{2}p(x)}} 2^{{H(p)}}=2^{{-\sum _{x}p(x)\log _{2}p(x)}}
where H(p) is the entropy (in bits) of the distribution and x ranges over events. (The base need not be 2: The perplexity is independent of the base, provided that the entropy and the exponentiation use the same base.) Source: wikipedia

3. Perplexity can be interpolated as a smoothed estimation of a numbe of neighbors. These neighbors can affect on point xi and are defined as hyperparameter of the method. (5 - 50 values are recommended)

4. Similarity between points of data points are determined.

5. It is then minimised using gradient descent.
