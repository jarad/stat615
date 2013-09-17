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

### Homework 2 (due 17 Sep in class)

This homework covers data augmentation approaches for probit and logistic regression.

1. Show that the following models are equivalent:
    - y~Ber(p), p = \Phi(Xb) where \Phi is the cdf of a standard normal
    - y=I(Z>0), Z ~ N(Xb,1)
1. Run an MCMC for the model below (you can use BUGS/JAGS) and describe (using a plot?) how non-identifiability affects the posterior. 
    - y=I(Z>a), Z~N(Xb,1) where X includes an intercept and a single explanatory variable and a and b are unknown parameters
1. Verify (or find the typo for) the likelihood for beta at the bottom of page 7 of [Polson et al](http://arxiv.org/pdf/1205.0310v3.pdf).


### Homework 3 (due 24 Sep in class)

1. Verify equation 2.10 in [Yu and Meng]({{BASE_PATH}}/papers/Yu_Meng_to_2011.pdf).
1. Consider the following Gibbs sampler: 'X|Y~ N(pY,1-p^2)' and 'Y|X~N(pX,1-p^2)' for a known 0<p<1. 
    a. What is the stationary distribution for this Gibbs sampler?
    a. Describe the transition kernel for moving from X to X', similar to equation 2.17 in Yu and Meng. 
    a. Verify that this transition kernel preserves the stationary distribution for X using the technique below equation 2.17 in Yu and Meng. 

