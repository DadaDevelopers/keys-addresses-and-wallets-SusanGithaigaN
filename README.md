[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/vhoKWTLf)
# assignment-2

#### 1. Generate legacy addresses, bech32 addresses and bech32m addresses
[See output.txt](output.txt)


#### 2. What is the difference between hardened and non hardened keys
| **Hardened Key** | **Non Hardened Key** |
|------------------|----------------------|
| Computed with the hash parent's **private key** | Computed with the hash parent's **public key** |
| Considered more secure because even if someone obtains your extended public key (**xpub**), they cannot derive the parent key. | It’s considered less secure because if an attacker obtains your extended public key (**xpub**) and any one child private key, they can reconstruct your master private key. |



#### 3. Why should a wallet developer prefer deterministic wallets over non deterministic wallets

#### Simplified Backups
Deterministic wallets need only **one seed phrase** for full recovery, while non-deterministic ones require backing up every individual private key.

##### Improved User Experience
With deterministic wallets, users don’t need to manually save new keys after every transaction.  
The wallet can automatically regenerate all addresses from the seed phrase at any time.

#### Scalability
Developers can generate **millions of unique addresses** from one seed without storing each private key.  
This makes deterministic wallets ideal for exchanges and applications that need many addresses.

#### Support for Modern Features
Deterministic wallets are foundational to the **Lightning Network’s architecture** because they can generate all unique keys needed for payment channels from a single master seed.  
This allows thousands of channels to be managed and recovered with one backup — making Lightning node management both simple and secure.
