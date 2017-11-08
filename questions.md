# Lecture Questions

## Week 1: Introduction

1. [Video 2][w1v2] at 2'36":

"A computer program is said to learn from experience E with respect to some 
task T and some performance measure P, if its performance on T, as measured 
by P, improves with experience E." - [Mitchell, T. 1997.][mitch97]

Suppose your email program watches which emails you do or do not mark as spam,
and based on that learns how to better filter spam. What is the task T in this
setting?

  a. Classifying emails as spam or not spam.
  b. Watching you label emails as spam or not spam.
  c. The number (or fraction) of emails correctly classified as spam/not spam.
  d. None of the above - this is not a machine learning problem.

2. [Video 3][w1v3] at 10'23":

You're running a company, and you want to develop learning algorithms to
address each of two problems.

Problem 1: You have a large inventory of identical items. You want to predict
how many of these items will sell over the next 3 months.

Problem 2: You'd like software to examine individual customer's accounts, and
for each account decide if it has been hacked/compromised.

Should you treat these as classification or as regression problems?

  a. Treat both as classification problems.
  b. Treat problem 1 as a classification problem, problem 2 as a regression problem.
  c. Treat problem 1 as a regression problem, problem 2 as a classification problem.
  d. Treat both as regression problems.

3. [Video 4][w1v4] at 12'24":

Of the following examples, which would you address using an unsupervised learning
algorithm? (Check all that apply.)

  a. Given email labeled as spam/not spam, learn a spam filter.
  b. Given a set of news articles found on the web, group them into a set of
     articles about the same story.
  c. Given a database of customer data, automatically discover market segments and
     group customers into different market segments.
  d. Given a dataset of patients diagnosed as either having diabetes or not, learn
     to classify new patients as having diabetes or not.
 
4. [Video 5][w1v5] at 4'38":

Consider the training set shown below. `(x^(i), y^(i))` is the i^th training example.

What is y^(3)?

    |  Size in feet^2 (x)  |  Price($) in 1000's (y)  |
    |----------------------|--------------------------|
    |        2104          |           460            |
    |        1416          |           232            |
    |        1534          |           315            |
    |         852          |           178            |
 
  a. 1416
  b. 1534
  c. 315
  d. 0

5. [Video 6][w1v6] at 2'12":

Consider the plot below of `h_theta(x) = theta_0 + theta_1 * x`. What are `theta_0` and
`theta_1`?

  ![Graph question](img/2.2-quiz-1-fig.jpg)

  a. `theta_0` = 0, `theta_1` = 1
  b. `theta_0` = 0.5, `theta_1` = 1
  c. `theta_0` = 1, `theta_1` = 0.5
  d. `theta_0` = 1, `theta_1` = 1

6. [Video 7][w1v7] at 6'52":

Suppose we have a training set with m=3 examples, plotted below. Our hypothesis
representation is `h_theta(x) = theta_1 * x`. The cost function `J(theta_1)` is
`J(theta_1) = ½m * sum(i = 1, m, (h_theta(x^i)−y^i)^2)`. What is `J(0)`?

  ![Graph question](img/2.3-quiz-1-fig.jpg)

  a. 0
  b. 1/6
  c. 1
  d. 14/6

7. [Video 9][w1v9] at 10'48":

Suppose `theta_0 = 1`, `theta_1 = 2`, and we simultaneously update `theta_0` and
`theta_1` using the rule:

    theta_j <= theta_j + sqrt(theta_0 * theta_1) (for j=0 and j=1)
    
What are the resulting values of `theta_0` and `theta_1`?

  a. 0
  b. 1/6
  c. 1
  d. 14/6

8. [Video 10][w1v10] at 8'04":

Suppose `theta_1` is at a local optimum of `J(theta_1)`, such as shown in the
figure. What will one step of gradient descent

    theta_1 <= theta_1 - alpha * (diff wrt theta_1) J(theta_1)
    
do?

  ![Graph question](img/2.6-quiz-1-fig.jpg)

  a. Leave `theta_1` unchanged
  b. Change `theta_1` in a random direction
  c. Move `theta_1` in the direction of the global minimum of `J(theta_1)`
  d. Decrease `theta_1`

[mitch97]: Machine Learning. McGraw Hill. p. 2. ISBN 0-7-042807-7
[w1v1]: https://www.coursera.org/learn/machine-learning/lecture/RKFpn/
[w1v2]: https://www.coursera.org/learn/machine-learning/lecture/Ujm7v/
[w1v3]: https://www.coursera.org/learn/machine-learning/lecture/1VkCb/
[w1v4]: https://www.coursera.org/learn/machine-learning/lecture/olRZo/
[w1v5]: https://www.coursera.org/learn/machine-learning/lecture/db3jS/
[w1v6]: https://www.coursera.org/learn/machine-learning/lecture/rkTp3/
[w1v7]: https://www.coursera.org/learn/machine-learning/lecture/N09c6/
[w1v8]: https://www.coursera.org/learn/machine-learning/lecture/nwpe2/
[w1v9]: https://www.coursera.org/learn/machine-learning/lecture/8spIM/
[w1v10]: https://www.coursera.org/learn/machine-learning/lecture/GFFPB/
[w1v11]: https://www.coursera.org/learn/machine-learning/lecture/kCvQc/
