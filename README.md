# ResellerPaymentsOpen

**“Pay resellers by name in USDT on Polygon with automatic fee collection.”**

**Live dApp:** https://resellerairtimepaymentdex.netlify.app/  

---

## Overview
ResellerPaymentsOpen is a smart contract that allows anyone to register a unique reseller name (e.g., `"AliceShop"`) and receive payments directly in **USDT (Polygon, 6 decimals)**.  

- **Self-service registration** — resellers can claim, change, or relinquish names.  
- **Pay by name** — customers pay resellers using a human-readable name instead of copying wallet addresses.  
- **Automatic fee split** — a configurable fee (basis points) is taken from each payment and sent to a fee collector.  
- **Transparent** — all mappings and payments are recorded on-chain.  

---

## Key Functions
- `claimResellerName(string name)` → register a new unique name.  
- `changeMyResellerName(string newName)` → update your name.  
- `relinquishMyName()` → free up your name.  
- `payReseller(string name, uint256 netAmount)` → pay reseller by name (USDT).  
- `quoteTotal(uint256 netAmount)` → view helper to calculate total incl. fee.  
- `getResellerWallet(string name)` → resolve name to wallet.  

---

## Example Flow
1. **Reseller** claims name:  
   ```solidity
   claimResellerName("AliceShop");

   
