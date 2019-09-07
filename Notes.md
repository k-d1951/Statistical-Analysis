### Bayes Theorem
When we know Probablity of B given A and to find probablity of A given B


``P(A|B) = P(B|A)P(A) / P(B)``
``P(B|A)=P(B union A)/P(A)``

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
