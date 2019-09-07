### Bayes Theorem
When we know Probablity of B given A and to find probablity of A given B


``P(A|B) = P(B|A)P(A) / P(B)``


``P(B|A)= P(B union A) / P(A)``

### Central Limit Theorem
With large enough number of samples from the same population the sample means will be normally distributed. Dosent make any assumption about the underlying distribution. Helps in hypothesis testing. Gives the likelihood that a given mean came from a particular distribution and based on this we reject or fail to reject the Hypothesis. 

    from numpy.random import randint

    # Adapt code for 100 samples of size 30
    means = [randint(1, 7, 1000).mean() for i in range(0,1000)]

    # Create and show a histogram of the means
    plt.hist(means)
    plt.show()


### Law of Large Numbers
As the size of sample increase the estimate of the sample mean will get closer to the population mean.

The Central limit Theorem states that when sample size tends to infinity, the sample mean will be normally distributed. The Law of Large Number states that when sample size tends to infinity, the sample mean equals to population mean.

### Probability Distributions
* Describes the Likelihood of an outcome. 
* Probablities must add up to 1.
* Can be Discreet - Die
* Or Continuous - Rainfall

### Bernoulli Distribution 
    # Generate bernoulli data
    from scipy.stats import bernoulli
    data = bernoulli.rvs(p=0.5, size=1000)

    # Plot distribution
    plt.hist(data)
    plt.show()

### Binomial Distribution
is used to model the number of successful outcomes in trials where there is some consistent probability of success.
    # Generate binomial data
    from scipy.stats import binom
    data = binom.rvs(n=10, p=0.8, size=1000)

    # Plot the distribution
    plt.hist(data)
    plt.show()

    # Assign and print probability of 8 or less successes
    prob1 = binom.cdf(k=8, n=10, p=0.8)
    print(prob1)

    # Assign and print probability of all 10 successes
    prob2 = binom.pmf(k=10, n=10, p=0.8)
    print(prob2)


### Poisson Distribution
Count the number of times something has happened . Counting events over time given some continous rate.
