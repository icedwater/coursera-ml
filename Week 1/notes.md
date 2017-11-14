# Notes from the course

1. Unsupervised learning lecture:

    - Cocktail party algorithm (2-source?) [S. Roweis, Y. Weiss, E. Simoncelli]:

        [W,s,v] = svd((repmat(sum((x .* x), 1), size(x, 1), 1) .* x) .* x');

    What does this mean?

2. Model (linear regression) video:

    - training set T has i examples (x^i, y^i)
      - x is an input variable
      - y is an output variable
    - hypothesis h maps inputs x to outputs y
      - linear regression is first try
      - h_theta (x) = theta_0 + theta_1 * x

3. Cost Function video:

    - Given `h_theta (x) = theta_0 + theta_1 * x`,
      try to minimize squared error cost function `J(theta_0, theta_1)`:

        J(theta_0, theta_1) = 1/2m * sum( i = 1, m, (h_theta(x^i) - (y^i))^2 )

4. Gradient Descent video:

    - repeat until convergence {
        theta_j <= theta_j - alpha * (diff wrt theta_j) J(theta_0, theta_1)
      }

      where `alpha` is the learning rate
    - thetas should be updated simultaneously.
