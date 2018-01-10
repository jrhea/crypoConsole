# cryptoConsole

This repo currently subscribes to the GDAX websocket API to listen for order book and ticker data.

## Usage

```
Usage: cryptoConsole fetch [options]

cryptocurrency tools

Options:

  -w, --websocketUrl [value]   websocket url
  -p, --product <value>        product to query
  -f, --outputFields <values>  comma seperated list of output fields
  -s, --outputStyle <value>    format options for output (default: pretty)
  -h, --help                   output usage information
```

## Examples

**Fetch Ticker Data**
```
cryptoConsole fetch orderBook -p ETH-USD -s raw
```

**Fetch Order Book Data**
```
cryptoConsole fetch orderBook -p ETH-USD -s csv
```

**Get raw ticker data and pipe it back into cryptoConsole so it can be pretty printed**
```
cryptoConsole fetch ticker -p ETH-USD -s raw | cryptoConsole fetch ticker -p ETH-USD -s pretty
```
