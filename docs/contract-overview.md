# Smart Contract Overview

---

##  Contract Addresses (Sepolia Testnet)

- **Public EIC (Genesis/Reward):**  
  `0x8be78900292364Dc68EF5F2e395fE2906abA28C1`  
  *Used for mint/claim, PoI rewards*

- **Vault / Treasury:**  
  `0x29F6aa585956E85C6F188e6CADA19a07eA0b5253`  
  *Reserve storage, not for direct minting*

---

## ⚔️ Core Functions

### Public (Genesis/Reward)
- `name()` → Token name ("Energy Intelligence Coin")  
- `symbol()` → "EIC"  
- `decimals()` → 18  
- `totalSupply()` → Current circulating supply  
- `mint(address, amount)` → Mint new tokens (restricted/PoI logic)  
- `claim()` → Claim allocation (for PoI participants)  
- `balanceOf(address)` → Query wallet balance  

### Vault / Treasury
- `treasury()` → Returns treasury address  
- `remainingFor(address)` → Shows remaining allocation for a participant  
- `deposit()` → Add reserves (internal)  
- `withdraw()` → Controlled release from treasury  

---

## ️ Contract Roles
- **Owner / Deployer:** Oversees upgrades and initial distribution.  
- **Participants:** Claim and interact through Public contract.  
- **Vault:** Holds long-term reserves, prevents accidental depletion.  

---

##  Verification
Both contracts are deployed and verifiable on Sepolia Etherscan.  
Always confirm you are interacting with the **Public contract** for PoI and rewards.
