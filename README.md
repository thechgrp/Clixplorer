# Clixplorer

Clique consensus (EIP-225) block explorer

More info at https://github.com/ethereum/EIPs/issues/225

## Compile

```npm run-script build```

Dependency: browserify

## Configuration

1) Edit the following three lines in your js/index.js
And replace the value with your ethereum websocket hostname and port.

var endpoint = 'ws://rinkeby.eth.6120.eu/ws'
var hostUrl = 'https://6120.eu'
var urlLabel = 'Rinkeby/6120'

2) If you are setting up an ethereum Clicque using proof of authority conensus (POA), you will want to make sure you set up websocket on your geth startup. Here's a basic sample, be sure to review which IP you will allow to connect:
   --ws --wsaddr '0.0.0.0' --wsport 8546 --wsorigins "*" --wsapi 'personal,db,eth,net,web3,txpool,miner'

## To run
Use a node http server such as node serve: npm install -g serve.
Then to run: serve

## Issue

Buffer issue
After running ```npm install``` remove ```rm -r node_modules/browserify/node_modules/buffer```

## License

This project is licensed under the GPLv3 License - see the [LICENSE](LICENSE) file for details

## Donation

ETH: 0xc8f8371BDd6FB64388F0D65F43A0040926Ee38be
