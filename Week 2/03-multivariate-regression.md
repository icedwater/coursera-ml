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

## Multiple Features
## Multiple Features
## Multiple Features
## Multiple Features
## Multiple Features
