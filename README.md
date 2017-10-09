# Yahoo-Finance-API-and-Neural-Net-Work
Exercise questions from Devin Bost

1.       Starting from the logistic sigmoid cost function:
Machine generated alternative text:
E(yi + (1 — yi) log(l 
he(x) = g(9Tx) 
1 
g(z) 
ho(xi))) 
Show how to derive the gradient:

 
You should show your work on paper. If you get stuck, you may request a table of rules of differentiation or other math rules, upon request. 
 
2.       Upon completion, in Python, write the cost function using the following example:
a.       Consider that a group of students spent between 0 and 6 hours studying for an exam. We wish to write a cost function to estimate the probability that a student passed the exam by using gradient descent. Your function should accept as input parameters, the weight vector theta, the input vector X (of values we're calculating the cost of), the label vector Y (of values we're trying to predict). For this exercise, we will not use gradient descent yet, but assume that the weights of theta will be provided. (For development purposes, you may initialize the weights with random values between 0 and 1.)
3.       Write a function in Python that queries the Yahoo finance API for Google daily open, high, low, and close prices and volume for the last 3 years.
4.       Write a function to calculate log price changes across the closing prices
5.       Write a function that computes a rolling sum of price changes for a given number of days (e.g. 7 days), and apply this function to the log price changes.
6.       Write a function that calculates the z-score on the rolling sum of log price changes to determine how many standard deviations the upcoming rolling (sum of) log price changes (from the function in the above step) are from the mean.
7.       Write a function that rounds the z-score to the nearest integer
8.       Write a function that returns 1 if the upcoming sum of log price changes is more than 2 standard deviations above the mean
9.       Later, we will:
a.       write a cost function that takes:
                                                i.            theta, a set of input weights that are initialized with random values between 0 and 1
                                              ii.            X, a matrix with the set of open, high, low, and close prices and volume (5 columns)
                                            iii.            Y, a set of labels \in {0,1} that indicate 0 if the upcoming sum of rolling log price changes is not more than 2 standard deviations above the mean or 1 if the upcoming sum of rolling log price changes is more than 2 standard deviations above the mean
b.       and we will create a model using PyTorch that we will use to train a neural network to predict if a window of 30 days of (O,H,L,C,V) values can predict if the upcoming week of rolling price changes will sum to more than 2 standard deviations above the mean
