---
layout: page
title: "Homework"
description: ""
---
{% include JB/setup %}

### Homework 6 (due 5 Nov in class)

(modified from exercise 5.7 of Hierarchical Modeling and Analysis for Spatial Data)

The [real estate data set](http://www.biostat.umn.edu/~brad/data/BatonRouge.dat) consists of information regarding 70 sales of single-family homes in Baton Rouge, LA, during the month of June 1989. 

1. Obtain the empirical variogram of the logarithm of selling prices.
1. Fit a standard regression model to the logarithm of selling price using all explanatory variables other than location.
1. Obtain the empirical variogram of the residuals to the fit above.
1. Perform a fully Bayesian analysis using an exponential spatial correlation function. Use a flat prior for the regression coefficients, inverse gamma priors for the variance components, and a Unif(0,10) prior on the range parameter. 
1. Provide a predictive distribution for the actual selling price for a home at location (long=-91.1174, lat=30.506) that has 938 sqft of living area, 332 sqft of other area, 25 years old with 3 bedrooms and 1 bathroom (no half baths). 

### Homework 5 (due 22 Oct in class)

1. Find the nugget, sill, and range (or effective range) for the linear, spherical, exponential, and Gaussian covariance function.
1. Plot the variograms for the linear, spherical, exponential, and Gaussian s using the same value for the nugget, sill, and range (or effective range).
1. Use Brook's Lemma to find the joint distribution for the conditional distributions  X|Y~ N(pY,1-p^2 ) and Y|X~N(pX,1-p^2 ).

### Homework 4 (due 15 Oct in class)

1. Find the stationary distribution for an autoregressive process of order 1.
1. Perform a Bayesian analysis of [this data set]({{BASE_PATH}}/data/dlm-data.csv), temperature measurements 25cm below the surface on an experimental plot in Wyoming. Here is some code to get you started:
   
{% highlight r %}
d = read.csv("dlm-data.csv")
d$date = as.Date(as.character(d$date), format="%m/%d/%y")

y = d$EHSR.25cm.T
y_tmp = y
y_tmp[1180] = mean(y[c(1179,1181)])
n = nrow(d)
de = decompose(ts(y_tmp, start=d$date[1], end=d$date[n], freq=24))
plot(de)
{% endhighlight r %}
    


### Homework 3 (due 24 Sep in class)

1. Verify equation 2.10 in [Yu and Meng]({{BASE_PATH}}/papers/Yu_Meng_to_2011.pdf).
1. Consider the following Gibbs sampler: X|Y~ N(pY,1-p^2 ) and Y|X~N(pX,1-p^2 ) for a known 0<p<1. 
    - What is the stationary distribution for this Gibbs sampler?
    - Derive the transition kernel for moving from X to X', similar to equation 2.17 in Yu and Meng. 
    - Verify that this transition kernel preserves the stationary distribution for X using the technique below equation 2.17 in Yu and Meng. 
1. Recreate the comparison between Hamiltonian Monte Carlo and Metropolis (or even Gibbs sampling) in the bivariate normal example used in [MCMC using Hamiltonian Dynamics](http://www.cs.utoronto.ca/~radford/ham-mcmc.abstract.html). Feel free to use [this HMC function](http://www.cs.utoronto.ca/~radford/ham-mcmc-simple), but otherwise you should write your own code.



### Homework 2 (due 17 Sep in class)

This homework covers data augmentation approaches for probit and logistic regression.

1. Show that the following models are equivalent:
    - y~Ber(p), p = \Phi(Xb) where \Phi is the cdf of a standard normal
    - y=I(Z>0), Z ~ N(Xb,1)
1. Run an MCMC for the model below (you can use BUGS/JAGS) and describe (using a plot?) how non-identifiability affects the posterior. 
    - y=I(Z>a), Z~N(Xb,1) where X includes an intercept and a single explanatory variable and a and b are unknown parameters
1. Verify (or find the typo for) the likelihood for beta at the bottom of page 7 of [Polson et al](http://arxiv.org/pdf/1205.0310v3.pdf).



### Homework 1 (due 10 Sep in class)

This homework covers two topics: Bayesian hypothesis testing (question 1) and regularized regression (questions 2-4). For the regularized regression problems, we assume the data are of the form y=Xb+e where e~N(0,s^2 ).

1. Derive equation (4) in [Sharpening Ockham's Razor on a Bayesian Strop]({{BASE_PATH}}/papers/ockham.pdf).
2. Show that independent normal priors on regression components lead to the ridge estimator on page 5 of [Ridge Regression in Practice]({{BASE_PATH}}/papers/Ridge_Regression_in_Practice.pdf).
3. Show that independent [Laplace](http://en.wikipedia.org/wiki/Laplace_distribution) priors on regression coefficients lead to the LASSO estimator on page 1 of [Bayesian LASSO](http://www.stat.ufl.edu/~casella/Papers/Lasso.pdf).
4. Derive the form of the prior distribution for the [elastic net estimator](http://en.wikipedia.org/wiki/Elastic_net_regularization). 



