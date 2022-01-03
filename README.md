## Creating Index Fund using Mixed Integer Programming

Equity money management strategies are largely classified as either ‘active’ or ‘passive’. The most common 
passive strategy is that of “indexing” where the goal is to choose a portfolio that mirrors the movements of 
the broad market population or a market index. Such a portfolio is called an index fund. For example, the QQQ 
Index fund tracks the NASDAQ-100 index.  
Constructing an index fund that tracks a specific broad market index could be done by simply purchasing all n 
stocks in the index, with the same weights as in the index. However, this approach is impractical (many small 
positions) and expensive (rebalancing costs may frequently be incurred, price response to trading). An index 
fund with m stocks, where m is substantially smaller than the size of the target population, n, seems desirable. 

In this project, we will create an Index fund with m stocks to track the NASDAQ-100 index. We will do this in 
multiple steps. First, we will formulate an integer program that picks exactly m out of n stocks for our 
portfolio. This integer program will take as input a ‘similarity matrix’, which we will call 𝜌. The individual 
elements of this matrix, 𝜌!", represent similarity between stock i and j. An example of this is the correlation 
between the returns of stocks i and j. But one could choose other similarity metrics 𝜌!". 
Next, we will solve a linear program to decide how many of each chosen stock to buy for your portfolio and 
finally evaluate how well our index fund does as compared to the NASDAQ-100 index, out of sample.  We 
will examine the performance for several values of m. 

## Methodology Overview

Brief summary of methodology for constructing Index fund:
1. Stock Selection: As a first step, we will formulate an integer program that picks exactly m out of n stocks for our portfolio. This integer program will take as input a similarity/correlation matrix (𝜌), with individual elements of this matrix 𝜌ij, representing similarity between stock i and j. 
2. Calculating Portfolio Weights: Next, we will solve a linear program to decide how many of each chosen stock to buy for our portfolio (weight of each stock in our fund)
3. Performance evaluation: Finally, we will evaluate how well our index fund performs in comparison to the NASDAQ-100 index. We will also test the performance for several values of m.
