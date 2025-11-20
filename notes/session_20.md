# A map of Mathematics
- Arithmetic
    - Number theory
- Algebra
    - Linear Algebra
    - Abstract Algebra
    - Group theory 
- Geometry
- Topology
- Trignometry
- Set theory
- Logic
- Probability
- Calculus
    - Differential
    - Integral 
- Real Analysis
- Statistics

# Mathematics of Data Science
- Linear Algebra
- Probability
- Calculus
- Statistics

# Probability for Data Science
- Dealing with uncertainity

## Frequentist definition of probability

## Law of Large numbers (LLN)
- The law of large numbers states that the more experiments we run, the closer we will tend to get tot the expected probability

# Classroom Activity 1: Compute Empirical probability of getting head

## Events and Sample Spaces
- Coin Toss example
- Dice throwing example

## Essential Set Theory & Combinatorics
- Union
- Intersection
- Factorial

## Dependent and Independent Events
## Joint probability
## Marginal Probability

## Conditional Probability
- Similarity to Hypothesis testing

## Bayes theorem
- Prior
- Likelihood
- Posterior
	
## Difference between conditional probability and Bayes theorem
## Revisiting Likelihood
## Random Variables and Expectations
## Expected value

## Probability Distributions
## Common Probability Distributions
- Bernoulli / Binomial
- Normal & Gaussian
- Uniform
- Log-normal

# Classroom Activity 2: Examining data distribution
Analyze a given textual data, hight of participants and examine what type of distribution it follows

Analyze their prior assignment submission time delta and find the probability distribution it matches.

## Probability Mass Function
## Probability Density Function
## Cumulative Distribution Function
## Central Limit Theorem (CLT)

## Essense of Information theory
- Quantifying uncertainity
- Entropy
- Entropy curve calculation
- Cross entropy

# Problem 1: Medical Test Accuracy
A certain disease affects 1% of population. A test of the disease is 99% accurate meaning
- If a person has the disease the test will be positive 99%
- If the person does not have disease, the test will be negative 99%

$P(D)$ : Probability of person has disease
$P(T)$ : Probablity of test is positive

$P(D)$ = 0.01

$P(D')$ = 1-$P(D)$ = 1-0.01 = 0.99

$P(T|D)$ = 0.99

$P(T'|D')$ = 0.99

$P(T|D')$ = 1-$P(T|D)$ = 1-0.99 = 0.01

Find $P(D|T)$  and $P(D|T')$


# Problem 2: Spam Email Classification
Suppose and email is classified as spam if it contains the word "money". Past statistics show:
- 5% of all emails are spam
- 2% non-spam emails contains the word money
- 60% spam emails contains the word money
Find $P(Spam|money)$ and $P(Spam|money')$


# Problem 3: Sample Space
- List the sample space for tossing two coins 
- What is the sample space for rolling two dice?
- How many possible outcomes exist in selecting a card from a standard deck of 52 playing cards?
- If an experiment consists of flipping a coin and rolling a die, what is the total number of outcomes?


# Problem 4: Dependent and Independent Events**
- A bag contains 4 red balls and 6 blue balls. If you pick one ball and then another with replacement, are the events independent or dependent?


# Problem 5: Joint and Marginal Probability**
- A dataset shows that 40% of customers purchase Product A, 25% purchase Product B, and 15% purchase both. What is the probability that a customer purchases at least one product? 


# Problem 6:  Expected Value**
- A lottery ticket costs ₹10 and has a 1% chance of winning ₹500. What is the expected value of the ticket?**  
  

# Problem 7:  Entropy & Information Theory**
- What is the entropy of a fair coin toss?**  
 $H(X) = - (0.5 \log_2 0.5 + 0.5 \log_2 0.5)$ = 1
- A probability distribution is $P(X) = (0.8,0.2)$. Calculate its entropy 
