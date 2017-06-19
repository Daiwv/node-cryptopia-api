### MAJOR WIP node.js wrapper for cryptopia.
Public only for now.

Setup:

#### Install dependencies:
npm install --save request crypto-js querystring

#### Public Calls:
##### Add file require to your code:
```javascript
var cryp = require('./node.cryptopia.js');

cryp.GetMarket(100, 6, function(data){
  console.log(data.Data)
  console.log(data.Data.AskPrice.toFixed(8))  
})
```
##### Output:
```
{ TradePairId: 100,
  Label: 'DOT/BTC',
  AskPrice: 0.00000101,
  BidPrice: 9.7e-7,
  Low: 8.7e-7,
  High: 0.000001,
  Volume: 10276284.9076486,
  LastPrice: 9.7e-7,
  BuyVolume: 83517762.1633753,
  SellVolume: 38612723.84007953,
  Change: 10.23,
  Open: 8.8e-7,
  Close: 9.7e-7,
  BaseVolume: 9.63535472,
  BuyBaseVolume: 15.48592503,
  SellBaseVolume: 13284488.84584638 }
0.00000101
```

##### Private calls:
Private calls will be something, i tell ya.

##### Example Key file
To use private calls first setup a private key file:
```
module.exports.tester = {
    api_key: 'api_key',
    api_secret: 'api_secret'
}
```
Name your key file, then please be very sure to add your key file name to
your dot gitignore for your project.  Pushing private keys is a very common
mistake.
