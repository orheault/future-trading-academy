# CFTC

Approach futures markets with caution: Volatile and risky venture for individual investors

Basic of Futures trading:
- Contract to buy or sell a commodity at a future date
- Price and amount are fixed at the time of the agreement
- Some contract allow cash settlement instead of delivery
- A future option is the right to buy or sell a contract at a future date for a price

Users of futures markets: hedgers, speculators, commercial or institutional.

Regulation: 
- Handling customer fund -> register to NFA
- CFTC protect customers

# CME GROUP

## Future contracts

What is a futures contract: allow participants to offset the risk of a price change over time

Contract specification: Contain underlying asset, quanity, delivery location and delivery date.

## Trading codes


Each calendar month (month code) expiration is identified by a single letter as follows:

January – F
February - G
March -H
April -J
May - K
June - M
July - N
August - Q
September -U
October - V
November -X
December -Z

Year code: last digit -> year 2019, code is 9


E-mini S&P 500 futures: ES
January: F
Year code: 2019

ESF9

## Expiration 

A contract expire, traders can rollover the position

## Settlement

This is the legal delivery of the original contract

## Tick Movements

Minimum price fluctuation known as tick

ES tick: tick size is 1/4 of one point -> 0.25 * 50 = 12.50$

## Price limits and banding

This is the maximum price range allowed for a contract in a trading session.

Indexes futures have
- downside: 7%, 13%, 20%
- up: 7%

Price banding: order price validation rejects orders outside the band to maintain ordely markets.

# Contract notional value

Contract unit: standardized size unique to each futures contract based on Volume, eight, financial measurement.

Example: 
- COMEX golad contract unit (GC) = 100 troy ounces -> measured by weight
- NYMEX WTI crude oil (CL) is 1000 barrels of oil -> measured by volume
- E-mini S&P 500 contract unit (ES) is based on a fixed multiplier times the S&P 500 index

Notional value is Contract unit X contract price = notional value

100 (troy ounces) X 1000$ = 100 000$

Notional value is used to calculate hedge rations versus other futures.

# Mark to market

Mark to market is used to update the margin at the end of the day.

Initial margin deposited: $10,000
Maintenance margin: $8,000
Mark-to-market loss: −$2,500
New margin balance: $7,500

# Margin

Securities margin is the money borrowed to purchase stock.

Futures margin is the amount of money required in the account to trade.

Type of Future margin:
- Initial margin: minimum amount to open a position
- Maintenance: minimum to maintained at any given time
- Intraday margin: during the day
- Overnight margin: during the night -> a bit higher

# Future expiration and contract roll

Future contract expired, on the third Friday of the expiration month.

Liquidating the position: selling the position to exit the trade
Rollover: move his position to the next month
Settlement: buy the underlying asset.

# Price discovery

Determining a common price for an asset. Bid and ask price are available.

This is the interaction between sellers and buyers, supply and demand.

# Calculating profit or loss

Current value:

The current value of the contract is multiplying the current price of underlying times the contract size.

Example: WTI futures is $54, $54 x $1000 = 54 000 $

Value of a one-tick move:

The dollar value of a one tick move is calculated by multiplying the tick size by the size of the contract.

WTI is $0.01 x 1000 = $10

# Part C

Why do futures markets exist?

Future market exist to allow participant to trade the underlying product. Participant are hedger, speculator or even buyer that settle with the real product. Seller and buyer can better manage their cash flow through the month. Let's take a farmer that want to sell corn, they can sell a volume of corn in 3 month at X price. This protect the farmer to price fluxuation. The same principle apply for the buyer.

What is the economic difference between a hedger and a speculator?

A hedger is a participant that want to protect (hedge) another asset by selling the opposite. For example, a fund manager that has a $100 k in the S&P may want to hedge his position by selling $100 k ES during the time the market will fall. The speculator is a market participant that will take position on going long or short depending on what he belivieve the market will do.

Why is futures margin not the maximum amount at risk?

Future margin is the amount of money required in the account to open/maintain a trading position. Initial marge is the required amount to open a position. Maintenance marge is the minimum so keep the position open. A position with a stop loss can loose more than configured du to the slippage, gap, fast market execution.

What does the clearinghouse do?

A clearing house execute trade between seller and buyer. It also maintain the market to allow search liquidity. The clearinghouse is the central entity that exchange positions, calculate margin requirement daily and collect daily guarantee. It reduce buyer risk that does not respect his conditions.

Why can a USD 10,000 account still have exposure far larger than USD 10,000?

Price varies with the size of the contract and the tick to market. A $ 10K can be one full ES contract, the difference in fluxuation is the amount deducted or added. The difference is calculated by multiplying the tick size by the size of the contract.

What is the difference between cash settlement and physical delivery?

Physical delivery is the underlying product being sold and shiped to the buyer when the contract expired. The settlement is the participant that close his position because he does not want to receive delivery.

Why must a retail trader know the contract month and expiration process?

The contract month is the expiration. this usually happen the third friday of the month. Future tickers are spelled using the symbol + letter month + year number. If the participant do not settle or rollover his position, he will have to setlle and take delivery. Toward the end of the contract month, participants move over the next contract month.

What does “only risk capital” mean in your personal situation?

Only risking capital is the principal to only trade with capital that I can affort loosing. 

## Part D — Ecosystem map

```tex
Trader → Broker/Introducing Broker → FCM → Exchange → Clearinghouse
                    ↘ Platform / Data service
Regulators and self-regulators: CFTC / NFA
```

For each component, state:

- what it does;
- what it does not guarantee;
- one question you would ask before opening an account.

### Trader
What it does: 
Trader are participant that trade, enter position long or short, in an exchange. They trade money in exchange of a product.

what it does not guarantee:
Trader are not always humain in the market. Some traders are algorithmes based.

one question you would ask before opening an account:
What is the mental load of being a trader on the day to day. What are the typical work hours during the day.

### Broker/Introducing Broker
What it does: Brokers are entities that connect the trader to the FCM through trading software. It also provide trading software.
What it does not guarantee: Brokers are not always certified or regulated. The trader must choose a regulated broker to ensure proper fund transit to FCM, payout, etc.
One question to ask before opening an account: what are the legetimate broker, well regulated, in Canada that allows trading Futurs and commodities.

### FCM
What it does: FCM are future commission merchant. It hold trader funds, record position, collects marging and connect the trading software to the clearing system.
What it does not guarantee: trader being profitable or not.
Question: What are the fatest executor FCM and they support which brokers?

### Exchange
What it does: the exchange is the place where futures contract are listed and traded. The exchange, CME, standardized the contract, rules. The exchange execute the trade.
What it does not guarantee: The exchange does not guarantee the price of the contract that the trader want.
question: What are the exchange specification like opening hours, where can i get contract information or product information?

### Clearinghouse
What it does: it act as a middle man to handle money between buyer and seller
What is  a questeion: what is the clearinghouse for ES contract?
 
### Platform / Data service
What it does:the platform is the trading software, while the data service provides market information like price, volume, etc.
What it does not guarantee: to hold the trader fund.
Question to ask: what the broker can provide me?

### Regulators and self-regulators: CFTC / NFA
What it does: They are independant entities enforcing regulations, oversees exchanges, clearinghouse and other market participant.
What it does not guarantee: Broker solvency
Question to ask: is the broker and fcm registered?



