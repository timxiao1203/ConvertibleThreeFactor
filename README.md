# Convertible Three Factor Model

The buyer of a convertible bond (CB) receives periodic coupon payments from the issuer, but can also convert the CB into the issuer’s stock.  The convertible bond may also include call and put provisions, which respectively allow the issuer to buy back the convertible bond and the owner to put the convertible bond for respective preset amounts.  A three factor trinomial tree based model is presented for pricing the CB.

Here the short interest rate process is assumed to be of Ho-Lee form under the bond’s coupon currency risk-neutral probability measure, and the stock price and foreign exchange rate processes are assumed to follow geometric Brownian motion with drift under their respective risk-neutral probability measures.  

The stock price process is then expressed under the bond’s coupon currency risk neutral probability measure by means of a quanto adjustment.   Under the bond’s coupon currency risk neutral probability measure, then, the short interest rate, stock price and foreign exchange rate processes respectively follow geometric Brownian motion with drift, but are driven by pair-wise correlated Brownian motions.  

We define three related random variables, which are each taken to be particular linear combinations of the original short interest rate, stock price and foreign exchange rate random variables.  Here the respective linear combinations are chosen such that the processes for the new random variables are now driven by pairwise uncorrelated Brownian motions.

We next construct respective trinomial trees to approximate the processes for each new random variable, but with each tree based on the same time slice partition of the CB tenor.  A new tree, which combines these respective trees, is then defined such that the set of nodes on a particular time slice of the combined tree equals the cross product of the set of nodes in each of the three respective trees at this time slice.  

Each node on the combined tree then has   children; and, since the processes for the new random variables are driven by pairwise independent Brownian motions, the probability of branching to any of these children nodes is given by the product of the corresponding probabilities on each of the individual trees.  The values for the original short interest rate, stock price and foreign exchange rate are now obtained, at each node on the combined tree, by inverting a related linear system of equations.

At each tree time slice we keep track of the call strike, put strike and stock conversion level at this time; we note, however, that FP does not include accrued interest in the respective call and put strike levels at tree times where a coupon is not paid.  FP assumes that the CB owner can choose to hold, put or convert the bond into stock.  The CB issuer can then choose to call the bond.  If the bond is called, however, the owner can then force the bond to be converted into stock.  

The CB is then valued by traversing the combined tree using backward induction.  At each tree node we apply the hold, put or call logic above, discounting by the corresponding stochastic interest rate. Since the bond issuer may default, the CB value is affected by credit risk.  FP models this effect by reducing the coupon amounts paid by the underlying bond in the CB valuation. 

We note that FP constructs an individual trinomial tree by first defining a related binomial tree.  A trinomial tree approximation is then constructed by coalescing adjacent pairs of binomial tree time slices into corresponding single trinomial tree steps.  Here the trinomial tree branching probabilities are taken as particular products of the probabilities on the two corresponding binomial tree time slices.  

References:

https://finpricing.com/lib/EqCliquet.html

https://osf.io/pbjf8/download
