# Cost Function

We can measure the accuracy of our hypothesis function by using a cost
function. This takes an average difference (actually a fancier version
of an average) of all the results of the hypothesis with inputs from x's
and the actual output y's.

    J(θ0,θ1) = ½m∑i=1m(y^i−yi)2 = ½m∑i=1m(hθ(xi)−yi)2

To break it apart, it is `½x¯` where x¯ is the mean of the squares of
`hθ(xi)−yi`, or the difference between the predicted value and the actual
value.

This function is otherwise called the "Squared error function", or "Mean
squared error". The mean is halved (½) as a convenience for the computation
of the gradient descent, as the derivative term of the square function will
cancel out the ½ term. The following image summarizes what the cost function
does:

![cost function](img/05-cost.png)
