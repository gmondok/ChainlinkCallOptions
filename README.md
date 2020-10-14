# ChainlinkCallOptions
Contract that allows writing, buying and exercising of ETH and LINK call options using Chainlink pricefeeds

//Takes which token, a strike price(USD per token w/18 decimal places), premium(same unit as token), expiration time(unix) and how many tokens the contract is for  
```
function writeOption(string memory token, uint strike, uint premium, uint expiry, uint tknAmt)
```

//Purchase a call option, needs desired token, ID of option and payment  
```
function buyOption(string memory token, uint ID) public payable
```

//Exercise your call option, needs desired token, ID of option and payment  
```
function exercise(string memory token, uint ID) public payable
```

All uints input (strike, premium, tknAmt) are 18 decimal fixed point (meaning 1 is represented as 1e18 or 1 * 10^18) 
with the exception of expiry which is Unix time formatted.

