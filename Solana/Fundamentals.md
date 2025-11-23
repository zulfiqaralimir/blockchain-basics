# 🌐 Solana Fundamentals

## 🧾 What is an Account?
On Solana, **everything is an account**.  
An account is a **data container** on the blockchain. It stores:
- Data (state)
- Lamports (Solana tokens)
- Ownership information (which program controls it)

**Types of accounts:**
- User accounts (wallets)
- Program accounts (smart contracts)
- PDA accounts (program-owned data)
- Token accounts
- NFT metadata accounts

**Key idea:**  
Ethereum = contracts store state inside themselves  
Solana = contracts store state in **separate accounts**

---

## 🧠 What is a Program?
A **program** is Solana’s version of a **smart contract**.

- Written in **Rust** (usually with Anchor)  
- Deployed as **read-only**  
- Contains **instructions** (functions)  
- Cannot store data inside itself  
- Works on data stored in **accounts**

Programs = logic  
Accounts = storage

---

## ✍️ Signers
A **signer** is any account that **approves a transaction**.

Signers include:
- Wallets (public/private keys)
- PDAs (signed programmatically)
- Any authority account

A signer proves:
> “I authorize this action.”

No signature = no permission.

---

## 🏦 Rent
Solana accounts must pay **rent** to stay alive.

- Accounts need **lamports** deposited  
- Rent-exempt = permanent  
- Not rent-exempt = may be deleted if lamports run out  
- More data → higher rent requirement

Rent ensures the network doesn’t store abandoned accounts forever.

---

## 🌍 Clusters
A **cluster** is a Solana network environment.

Solana has 3 major clusters:

### 1. **Mainnet**
Real money, real SOL  
Production apps run here

### 2. **Devnet**
Free SOL faucet  
Used for testing

### 3. **Testnet**
Used by core Solana engineers for network experiments

Each cluster = separate blockchain.

---

## 🔐 Keypairs
A **keypair** = (public key + private key)

- Public key = your **address**
- Private key = **signing authority**
- Stored in:
  - JSON files
  - Phantom/Solflare wallet
  - Hardware wallets
  - Env variables (never recommended)

In Solana:
- Keypairs sign transactions
- Programs **never** hold private keys

---

## 🌐 RPC Nodes
RPC = **Remote Procedure Call**

An RPC node lets your app:
- Read blockchain data  
- Send transactions  
- Fetch logs  
- Access account state  

RPC = the gateway to Solana.

Popular RPC providers:
- Helius  
- Triton  
- QuickNode  
- Ankr  
- Custom local validator  

Your code → RPC → Solana blockchain.


