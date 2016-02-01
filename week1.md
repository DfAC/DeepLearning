# Session 1

* need a lot of data
* simple tools for complex problems

## logistic classification

$WX + B = Y$

* use softmax function to calculate probabilities from scores (logits) $s(y_i)=\frac{e^{y_i}}{\sum_j e^{y_j}}$

## We will focus on

* logistic classification
* tsotchsti optimalisation
* data and parameter tuning
* deep networks
* regularisation

## Cross entropy

If you increase size of the outputs (score) you classifier becomes very confident, if you reduce it it will be unsure. We want our classifier to gain confidence as it learns, leading to one-hot encoding - only one class is correct with probability of 1. THis will become problem with sparse matrices.

We get our answer by comparing two vectors - one from classifier (scores) and one corresponding to the labels (probabilities). Distance between two vectors can be measured by cross-entropy (D(S,L) =  - \sum_i L_i log(S_i)). It is not symmetric ($D(S,L) \neq D(L,S)$)

### Multinomial logistic classification

Input is converted by linear model $$WX + B = Y$$ into logit y which is then converted by softmax function into probabilities S(Y). Ten by cross entropy D(S,L) we obtain hot labels L.
Aim is to get weights W, B so we got low distance for correct class and high for incorrect one.

* we can calculate training loss - average cross entropy across whole training set $L = \frac{1}{N} \sum_i D(S(WX_i + b), L_i)$
	* its massive calculation
	* we want to find minimum loss function
	* simple approach is gradient descent using derivatives



## Installing TensorFlow

Check [details here](https://www.tensorflow.org/versions/master/get_started/os_setup.html#download-and-setup)

