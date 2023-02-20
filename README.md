# Logistic-Regression-Advanced-Case-Study

## Logistic Regression - Height, Weight, & Gender

In this project, I built a logistic regression model that uses a person's height & weight to predict their gender with 92% accuracy.

## 1.
![image](https://user-images.githubusercontent.com/86930309/220212123-c53a6e19-f0c7-4ca2-9884-2db462c4d2d6.png)

This is a graph of our data to predict a person's gender.

## 2. These are the params and accuracy on the training and test data to predict geneder based upon the variables:

BEST PARAMS {'C': 0.01}

Accuracy on training data: 0.92

Accuracy on test data:     0.92

## 3.
![image](https://user-images.githubusercontent.com/86930309/220212458-a27e266e-c7ae-4112-9edc-cbe205d0b84e.png)

In the figure here showing the results of the logistic regression, we plot the actual labels of both the training(circles) and test(squares) samples. The 0's (females) are plotted in red, the 1's (males) in blue. We also show the classification boundary, a line (to the resolution of a grid square). Every sample on the red background side of the line will be classified female, and every sample on the blue side, male. Notice that most of the samples are classified well, but there are misclassified people on both sides, as evidenced by leakage of dots or squares of one color ontothe side of the other color. Both test and traing accuracy are about 92%.


## 4.
Logistic regression is what is known as a discriminative classifier as we learn a soft boundary between/among classes. Another paradigm is the generative classifier where we learn the distribution of each class.

Let us plot the probabilities obtained from predict_proba, overlayed on the samples with their true labels:
![image](https://user-images.githubusercontent.com/86930309/220212632-c00cf31a-c573-428b-a7e4-1bdf9800884f.png)

Notice that lines of equal probability, as might be expected are stright lines. What the classifier does is very intuitive: if the probability is greater than 0.5, it classifies the sample as type '1' (male), otherwise it classifies the sample to be class '0'. Thus in the diagram above, where we have plotted predicted values rather than actual labels of samples, there is a clear demarcation at the 0.5 probability line.

Again, this notion of trying to obtain the line or boundary of demarcation is what is called a discriminative classifier. The algorithm tries to find a decision boundary that separates the males from the females. To classify a new sample as male or female, it checks on which side of the decision boundary the sample falls, and makes a prediction. In other words we are asking, given 𝐱, what is the probability of a given 𝑦 , or, what is the likelihood  𝑃(𝑦|𝐱,𝐰)?
