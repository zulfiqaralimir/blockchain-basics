# 🌐 Solana Fundamentals

- An Account is like a box that stores data on the Solana blockchain.
- Account = storage place.
- A Program is a smart contract on Solana.

- Program = rules.
- Account = storage.

- A Signer is someone/something that gives permission for a transaction.
- A signer must use a private key to approve an action.

- Without a signer → the blockchain will not accept the transaction.
- Signer = authorization.

- Solana requires rent (lamports) to store data in accounts.
- Rent = fee for storing data.

- A Cluster is a different Solana environment.
- Cluster = different versions of the Solana network.

- A Keypair is a combination of:
- Public key → your address
- Private key → your password/signing key

- Public key = bank account number
- Private key = ATM PIN

- An RPC Node is a gateway that lets your program talk to the Solana blockchain.
- RPC = the bridge between your code and the blockchain.

- PDAs (Program Derived Addresses)
- A PDA is a special address that belongs to a program, not a human.
- A locker that only the program can open.

- Seeds are the small pieces of data used to create a PDA.
- Think of seeds as ingredients used to calculate a unique address.

- A bump is a small number (0–255) used to make a PDA valid.
- Think of bump as a “fixing number” to make the PDA safe.

- CPIs (Cross-Program Invocations)
- A CPI is when one Solana program calls another program.
- One app calling another app’s function.

- A lamport is the smallest unit of SOL.
- 1 SOL = 1,000,000,000 lamports
- Lamports = tiny pieces of SOL.

- A Program ID is the public key of a Solana program.
- A program’s permanent address on the blockchain.

- An instruction is one command you tell the blockchain.
- Instruction = one action.
- A transaction is a bundle of instructions sent together.
- Think of a transaction as a package containing multiple commands.

## ✅ Summary in One Line Each

- PDA: Program-owned address with no private key

- Seeds: Data used to generate a PDA

- Bump: Extra number used to make a PDA valid

- CPI: One program calling another program

- Lamports: Smallest unit of SOL

- Program ID: Address of a smart contract

- Instruction: One command

- Transaction: A group of commands executed together


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


