.. _logistic_regression:

Logistic Regression
###################

Model
~~~~~~

- Classification predictor :math:`G(x)`.
- Models the posterior probability :math:`P(G=k | X=x)` of :math:`K` classes via linear functions.
- The model has the form:

.. math::

    \ln \frac{P(G=k | X=x)}{P(G=l | X=x)} = \theta_{k, 0} + \theta_{k, 1}^T x

- Although the last class is used as dominator in the odds-ratios, the choice of denominator is aribitrary.
- The posterior probability is given by:

.. math::

    P(G=k | X=x) = \frac{\exp(\theta_{k, 0} + \theta_{k, 1}^T x)}{1 + \sum_{l=1}^{K-1} \exp(\theta_{l, 0} + \theta_{l, 1}^T x)}

    P(G=K | X=x) = \frac{1}{1 + \sum_{l=1}^{K-1} \exp(\theta_{l, 0} + \theta_{l, 1}^T x)}

- Loss function: :math:`L(\Theta) = \sum_{i=1}^{N} \ln P(G=y_i | X=x_i)` where :math:`N` is the sample size.
  The loss function is the log-likelihood for the :math:`N` observations. The best estimates of the parameters
  is when the log-likelihood is maximized.
- Alternately loss function: :math:`L(\Theta) = - \sum_{i=1}^{N} \ln P(G=y_i | X=x_i)`. Here the loss function is
  the information content in the :math:`N` observations. Training attempts to capture the information in the data
  which in turn results in decrease of the remaining information content in the sample.
- The above model is also known as multinomial logistic regression. It can be directly used for even polynomial
  regression.


Example
~~~~~~~~

TODO

Observations
~~~~~~~~~~~~~

TODO
