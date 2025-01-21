# Mean Reversion Trading Algorithm

## What is "Mean Reversion"?
Mean Reversion assumes that asset prices (Such as Stocks) tend to return to their historical average (mean) prices and that deviations are temporary, and that over long periods of time, price will oscillate around the mean.  Mean is often calculated through historical data, such as price, returns, and earnings, however, in this script I have chosen to use historical returns in order to create the Buy/Sell rule.

### Limitations of Mean Reversion
- The market is dynamic, not all Assets or Markets may experience Mean Reversion due to external factors that make the old mean obselete such as signficant breakthroughs and news, changing market dynamics, changes in fundamentals which can cause a large shift in average values moving forwards
- Underlying economic events, such as financial crises or transformations (2008 financial crisis, dotcom bubble)
- Uncertainty in Timing the Reversion of a mean, predicting the exact date and time the reversal may take place is extremely difficult even if its expected to happen.
- Large macroeconomic changes can up end prior historical prices affecting the mean, for example if a central bank or treasury were to make signficant changes to a country's monetary or fiscal policy.

### How an Algorithm can manage risk
- Real-TIme dynamic adjustment of the mean by adjusting the threshold of mean reversion based on market conditions.  If a signficant Mean Reversion occurs an algorithm may widen or narrow the expected ranged based on recent volatility, macroeconomic, and risk factors using Moving averages and other smoothing techniques (such as EMA).
- Stop-Loss and Take-Profit strategies to mitigate and manage risk of a position that is deviating further away from the expected mean, automatically closing once an acceptable price point has been reached or if the price has moved too far in an undesirable direction.


## Installation

### Openpyxl

openpyxl is a Python Library to read and write Excel xlsx/xlsm/xltx/xltm files. Available [here](https://openpyxl.readthedocs.io/en/stable/).

You can install it through `pip`:

```bash
pip install openpyxl
```

### Alpaca

Alpaca is a Trading API that connects your algorithm to a Live or Paper trading service. Available [here](https://alpaca.markets/).

You can install it through `pip`:

```bash
pip install alpaca_trade_api
```

## Set Up and Running the Script

After these are installed the script is easy to run, just keep it running in the background while: Market is active, Excel file is `closed` while the script is fetching data, otherwise an error will occur, although its okay to view the excel data while its asleep (to clarify, during market hours as well).

## Currently Working On:
- Timezone-Aware
- load credentials from an environmental variable (config.py)
- finalise formatting
