# Farm Allocation Algorithm

---

::: tip
Make sure you read about [Yield Farming](/products/amm-exchange/yield-farming) to understand the purpose of this page.
:::


## What is a Farm Allocation Algorithm?

Most DEX's use a developer selected multiplier on yield farms to reward in a native token. DogMoney has decided to do something else, and make this choice mathematical in a way to optimize amount of volume and ensure fairness of the platform. In essence, this means that the rewards from yield farming on DogMoney are determined by the properties of the trading pairs and how they compare to each other.

## How does DogMoney's algorithm work?

First, the DOGMONEY/wDOGE pair is given a 30% allocation. Then, the next top 29 pairs by volume are selected (making a total of 30 pairs). We set an allocation floor of 0.25% (Currently 0.25 DOGMONEY per block out of 100 total DOGMONEY issuance per block) for each. The total volume of the pair over the preceeding month is multiplied by the volatility of the pair over the preceeding month.

[You can view the algorithm here](https://github.com/dogmoneyswap/dogmoneyswap-analytics/blob/master/src/pages/pools/upcoming.js)

## Why was this algorithm selected?

We want to have an algorithm that closely matches risk-adjusted return of an asset to encourage maximum volume for DogMoney.

The focus on volume over just liquidity is to ensure that xDOGMONEY stakers are rewarded and that farm allocation cannot simply be due to unrealistically highly priced liquidity.

## How can my token get a farm?

Simply ensure your token has enough volume on DogMoney to be in the top 30 pairs.
