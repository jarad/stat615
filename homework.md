---
layout: page
title: "Homework"
description: ""
---
{% include JB/setup %}


### Homework 1 (due 10 Sep in class)

This homework covers two topics: Bayesian hypothesis testing (question 1) and regularized regression (questions 2-4). For the regularized regression problems, we assume the data are of the form y=Xb+e where e~N(0,s^2 ).

1. Derive equation (4) in [Sharpening Ockham's Razor on a Bayesian Strop]({{BASE_PATH}}/papers/ockham.pdf).
2. Show that independent normal priors on regression components lead to the ridge estimator on page 5 of [Ridge Regression in Practice]({{BASE_PATH}}/papers/Ridge_Regression_in_Practice.pdf).
3. Show that independent [Laplace](http://en.wikipedia.org/wiki/Laplace_distribution) priors on regression coefficients lead to the LASSO estimator on page 1 of [Bayesian LASSO](http://www.stat.ufl.edu/~casella/Papers/Lasso.pdf).
4. Derive the form of the prior distribution for the [elastic net estimator](http://en.wikipedia.org/wiki/Elastic_net_regularization). 

### Homework 2 (due 12 Sep in class)

This homework covers data augmentation approaches for probit and logistic regression.

1. Show that the following models are equivalent:
    - y~Ber(p), p = \Phi(Xb) where \Phi is the cdf of a standard normal
    - y=I(Z>0), Z ~ N(Xb,1)
1. Run an MCMC for the model below and describe (using a plot?) how non-identifiability affects the posterior. 
    - y=I(Z>a), Z~N(Xb,1) where X includes an intercept and a single explanatory variable and a and b are unknown parameters

