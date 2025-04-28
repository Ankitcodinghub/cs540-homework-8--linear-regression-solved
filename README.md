# cs540-homework-8--linear-regression-solved
**TO GET THIS SOLUTION VISIT:** [CS540 Homework 8- Linear Regression Solved](https://www.ankitcodinghub.com/product/cs540-hw8-linear-regression-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;117942&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS540 Homework 8- Linear Regression Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
Change Log

Assignment Goals

Implement a linear regression calculation Examine the trends in real (messy) data

Summary

Percentage of body fat, age, weight, height, and ten body circumference measurements (e.g., abdomen) are recorded for 252 men. Body fat, one measure of health, has been accurately estimated by an underwater weighing technique. Fitting body fat to the other measurements using multiple regression provides a convenient way of estimating body fat for men using only a scale and a measuring tape. In this assignment, you will be looking at the bodyfat dataset

(http://jse.amstat.org/v4n1/datasets.johnson.html) and build several models on top of it.

Program Specification

You will be using the bodyfat dataset (bodyfat.csv ) for this assignment. Complete the following Python functions in this template regression.py :

1. get_dataset(filename) — takes a filename and returns the data as described below in an n-by(m+1) array

2. print_stats(dataset, col) — takes the dataset as produced by the previous function and prints several statistics about a column of the dataset; does not return anything

3. regression(dataset, cols, betas) — calculates and returns the mean squared error on the dataset given fixed betas

4. gradient_descent(dataset, cols, betas) — performs a single step of gradient descent on the MSE and returns the derivative values as an 1D array

5. iterate_gradient(dataset, cols, betas, T, eta) — performs T iterations of gradient descent starting at the given betas and prints the results; does not return anything

6. compute_betas(dataset, cols) — using the closed-form solution, calculates and returns the values of betas and the corresponding MSE as a tuple

7. predict(dataset, cols, features) — using the closed-form solution betas, return the predicted body fat percentage of the give features.

8. sgd(dataset, cols, betas, T, eta) — performs stochastic gradient descent, prints results as in function 5

Get Dataset

The get_dataset() function should return an n-by-(m+1) array of data, where n is the number of data points, and m is the number of features, plus an additional column of labels. The first column should be bodyfat percentage, which is the target that our regression model aims for. We denote it as y in the rest of the write up. Starting from the second column, there goes a list of features, including density, age, weight, and more. We use index 1 to represent density, 2 to represent age, and so on… You should ignore the “IDNO” column as it merely represents the individual id of each participant.

Dataset Statistics

This is just a quick summary function on one feature, given in the parameter col, from the above dataset. When called, you should print:

1. the number of data points

2. the sample mean

3. the sample standard deviation

on three lines. Please format your output to include only TWO digits after the decimal point. For example:

You might find this guide (https://pyformat.info/) to python print formatting useful.

Linear Regression

This function will perform linear regression with the model

We first define the mean squared error (MSE) as the sum of squared errors divided by # data points:

The first argument refers to the dataset, and the second argument is a list of features that we wish to learn on. For example, if we would like to study the relationship of body fat vs age and weight, cols should be [2, 3]. In this case, the model should be

Gradient Descent

This function will perform gradient descent on the MSE. At the current parameter , the gradient is defined by the vector of partial derivatives:

This function returns the corresponding gradient as a 1-D numpy array with the partial derivative with

Iterate Gradient

Gradient descent starts from initial parameter and iterates the following updates

at time t = 1, 2, … , T:

and so on for the rest.

The parameters to this function are the dataset and a selection of features, the T number of iterations to perform, and (eta), the parameter for the above calculations. Begin from the initial value as specified in the parameter betas.

Print the following for each iteration on one line, separated by spaces:

1. the current iteration number beginning at 1 and ending at T

2. the current MSE

3. the current value of beta_0

4. the current value of other betas

As before, all floating point values should be rounded to two digits for output.

Try different values for eta and a much larger T, and see how small you can make MSE (optional).

Compute Betas

Instead of using gradient descent, we can compute the closed-form solution for the parameters directly.

For ordinary least-squares, this is

This function returns the calculated betas (selected by cols) and their corresponding MSE in a tuple, as (MSE, beta_0, beta_1, and so on).

Predict Body Fat

Using your closed-form betas, predict the body fat percentage for a given number of features. Return that value.

For example:

Stochastic Gradient Descent

Now let’s have some fun with randomness and implement Stochastic Gradient Descent (SGD). With everything the same as part 5, modify the gradient as follows: in iteration t, randomly pick ONE of the n

selection step, for grading purposes. Print the same information as in the previous function. For example:

Since n is small in our dataset, there is little advantage of SGD over standard gradient descent.

However, on large datasets, SGD becomes much more desirable…

Discovery

Experiment on different combinations of features, and learning methods (closed form solution, gradient descent, or SGD). Try to answer these questions:

What is the best feature that predicts well?

What are the best set of features that predict well?

Which learning method is the most effective in terms of training error (MSE)?

Which learning method is the most efficient (takes the least time)?

What will happen if our dataset has more than 1 million entries?

We won’t grade these questions, but feel free to share your thoughts on Piazza!

Submission

check so that it will not run if your code is imported to another program.

Be sure to remove all debugging output before submission. Failure to remove debugging output will be penalized (10pts).

HW8

Criteria Ratings Pts

get_dataset 10.0 to &gt;0.0 pts

print_stats 10.0 to &gt;0.0 pts

regression 20.0 to &gt;0.0 pts

gradient_descent 10.0 to &gt;0.0 pts

iterate_gradient 10.0 to &gt;0.0 pts

compute_betas 20.0 to &gt;0.0 pts

predict 10.0 to &gt;0.0 pts

sgd 10.0 to &gt;0.0 pts
