

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

### API Credentials

There are two ways to run API credentials in this script:

Creating a seperate file (Config.py) to store the keys then importing them into the algorithm can be considered as the more secure option if needed (the method used in this repository).

The second option is to replace the following line

```
from config import ALPACA_API_KEY, ALPACA_SECRET_KEY, ALPACA_ENDPOINT
```

with the config.py code directly.

```
ALPACA_API_KEY = "ALPACA_API_KEY"
ALPACA_SECRET_KEY = "ALPACA_SECRET_KEY"
ALPACA_ENDPOINT = "ALPACA_ENDPOINT"
```




