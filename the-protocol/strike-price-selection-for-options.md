# Strike Price Selection for Options

Strategies based on options selling need to calculate the option strike price at which the options need to be sold. For that purpose strategy developers need to provide a pricing algorithm. For option pricing we use Black\&Scholes formula. It requires inputs such as historic weekly price volatility, implied volatility and other parameters that minimise risk and maximise returns. This algorithm is implemented off chain and uses data from oracles such as Chainlink.

For example, for covered calls selling, options need to be out of the money. So the algorithm will calculate the required strike price based on historical volatility, implied volatility, and required delta (typically less than 0.2). Risk is also managed using position sizing. If there are no good prices available, the amount sold can be reduced or it can be zero.

\
