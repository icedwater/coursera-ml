# Multivariate Linear Regression

## Multiple Features

Note: [7:25 - `θT` is a 1 by `(n+1)` matrix and not an `(n+1)` by 1 matrix]

Linear regression with multiple variables is also known as "multivariate linear
regression".

We now introduce notation for equations where we can have any number of input
variables.

    x(i)j = value of feature j in the ith training example
    x(i) = the input (features) of the ith training example
    m = the number of training examples
    n = the number of features

The multivariable form of the hypothesis function accommodating these multiple
features is as follows:

    hθ(x)=θ0+θ1x1+θ2x2+θ3x3+⋯+θnxn

In order to develop intuition about this function, we can think about `θ0` as
the basic price of a house, `θ1` as the price per square meter, `θ2` as the
price per floor, etc. `x1` will be the number of square meters in the house,
`x2` the number of floors, etc.

Using the definition of matrix multiplication, our multivariable hypothesis
function can be concisely represented as:

    hθ(x)=[θ0θ1...θn]⎡⎣⎢⎢⎢⎢x0x1⋮xn⎤⎦⎥⎥⎥⎥=θTx

This is a vectorization of our hypothesis function for one training example;
see the lessons on vectorization to learn more.

Remark: Note that for convenience reasons in this course we assume `x(i)0=1`
        for (i ∈ 1,…,m). This allows us to do matrix operations with theta
        and x. Hence making the two vectors `θ` and `x(i)` match each other
        element-wise (that is, have the same number of elements: n+1).

### Gradient Descent for Multiple Features

The gradient descent equation itself is generally the same form; we just have
to repeat it for our 'n' features:

    repeat until convergence: {
        θ0 <= θ0−α1m∑i=1m(hθ(x(i))−y(i))⋅x(i)0
        θ1 <= θ1−α1m∑i=1m(hθ(x(i))−y(i))⋅x(i)1
        θ2 <= θ2−α1m∑i=1m(hθ(x(i))−y(i))⋅x(i)2
        ⋯
    }

In other words:

    repeat until convergence: {
        θj:=θj−α1m∑i=1m(hθ(x(i))−y(i))⋅x(i)j
        for j := 0...n
    }

The following image compares gradient descent with one variable to gradient
descent with multiple variables:

![multiple-gradient-descent](img/03-multi-gd.png)

## Feature Scaling

We can speed up gradient descent by having each of our input values in roughly
the same range. This is because θ will descend quickly on small ranges and
slowly on large ranges, and so will oscillate inefficiently down to the optimum
when the variables are very uneven.

The way to prevent this is to modify the ranges of our input variables so that
they are all roughly the same. Ideally:

−1 ≤ x(i) ≤ 1

or

−0.5 ≤ x(i) ≤ 0.5

These aren't exact requirements; we are only trying to speed things up. The goal
is to get all input variables into roughly one of these ranges, give or take a
few.

Two techniques to help with this are feature scaling and mean normalization.
Feature scaling involves dividing the input values by the range (i.e. the
maximum value minus the minimum value) of the input variable, resulting in a new
range of just 1. Mean normalization involves subtracting the average value for
an input variable from the values for that input variable resulting in a new
average value for the input variable of just zero. To implement both of these
techniques, adjust your input values as shown in this formula:

xi:=xi−μisi

Where μi is the average of all the values for feature (i) and si is the range of
values (max - min), or si is the standard deviation.

Note that dividing by the range, or dividing by the standard deviation, give
different results. The quizzes in this course use range - the programming
exercises use standard deviation.

For example, if xi represents housing prices with a range of 100 to 2000 and a
mean value of 1000, then, xi:=price−10001900

## Learning Rate

Debugging gradient descent. Make a plot with number of iterations on the x-axis.
Now plot the cost function, J(θ) over the number of iterations of gradient
descent. If J(θ) ever increases, then you probably need to decrease α.

Automatic convergence test. Declare convergence if J(θ) decreases by less than E
in one iteration, where E is some small value such as 10−3. However in practice
it's difficult to choose this threshold value.

![plotting J to see cost trend](img/03-multi-plotj.png)

It has been proven that if learning rate α is sufficiently small, then J(θ) will
decrease on every iteration.

![learn rate implications](img/03-multi-diff-learnrate.png)

To summarize:

If α is too small: slow convergence.

If α is too large: may not decrease on every iteration and thus may not
converge.

## Multiple Features
## Multiple Features
## Multiple Features
