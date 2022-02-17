![](img/hackathon.png)

## Technical Setup

1. Create a single github account with a public repository for each team and or individual if you are not with a team
2. Install git on your local machine
3. Install docker on your locak machine (Optional)
4. Clone this repo ``git clone https://github.com/TradeBlock/tb-hackathon.git``
5. install [python version 3.10](https://www.python.org/downloads/) on your local development environment.
8. run ``pip install -r requirements.txt`` in directory you cloned
9. create .env file # for AWS credentials

## Optional Setup - Create Python Virtual Environment
1. Create the environment with ``python3.10 -m venv .venv``
2. Activate the environment before step 8 in Technical Setup with ``source .venv/bin/activate``
3. Continue with step 8 in Technical Setup

## Problem Statement 

### Summary

* To be RELEASED Thurs. 2/17/22

### Constraints

* Trades can only be a BUY or a SELL with a crytocurrency amount
* SELL trades can only be done after BUYS (i.e. no short sell)

## Links


## Response Data Object Definitions

### Fill

```
{
  “price”: decimal.Decimal,       # fill price
  “volume”: decimal.Decimal,      # fill volume
  “error_code”: str               # Optional. “rejected”
  “error_msg”: str                # Optional. description of error
  “unfilled”: dict[str, Decimal]  # unfilled portion of trades (xbt,eth)
}
```

### Unfilled

```
{
  “xbt”: decimal.Decimal,         # unfilled xbt volume
  “eth”: decimal.Decimal,         # unfilled eth volume
}
```
