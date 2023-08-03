# Shark Fin

We decided to consider the “Shark Fin” structured products due to its popularity. It is provided by many centralised exchanges and asset management companies. Shark Fin is a capital protected product which offers some participation in the upside or downside of the underlying. There are bullish and bearish variants. The name of “shark fin” come from the shape of its yield curve:

![](https://lh6.googleusercontent.com/K3svUS1fsIZIDkCKA1gbdaNl6LpF8ricrm26hXoMhgmMAyYDvwqF0Wpx\_tcbztXmf7OXBlZWh8kz-JRVYIb9SbadPFT8kCtDzjjddG9N9PHJ-wqIPdqBGPQRec2LNkf97ZIGg5VB3ua3xcyA-dOcuvU)

Bullish Shark Fin\


If the price rises above the predetermined level, the investor receives the principal investment back in USDC, plus the minimum coupon (e.g. 15% as in the graph above). If the price falls below the buy level, the investment and the guaranteed coupon gets converted to the underlying asset (e.g. Bitcoin) at the buy level. As such, the downside of this product is that if prices fall, the investor is obliged to buy the underlying asset at a higher-than-market price.

\


A Vault implementing weekly Shark Fin could continuously roll over and accrue profits

\
