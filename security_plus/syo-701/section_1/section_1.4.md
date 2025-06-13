# 🔑 Public Key Infrastructure

- Polices, procedures, hardware, software, or people responsible for creating, distributing, managing, storing, or revoking digital certificates
- Big endeavor
	- Lots of planning and decisions
- Associated with binding public keys to people or devices
	- In conjunction with Certificate Authority
	- Based around trust

### 🔠 Symmetric Encryption

- Single, shared key to encrypt and decrypt
- If lost you'll need another key
- Secret key algorithm
	- Shared secret
- Doesn't scale well
	- Hard to distribute
- Very fast
	- Less overhead than asymmetric
	- Often combined with asymmetric

### 🔢 Asymmetric Encryption

- Public key cryptography
	- Uses two or more mathematically related keys
- Private key
	- Do not share
	- No access
- Public key
	- Give it away
	- Anyone can access
- Private key is the only key that decrypt data encrypted with public keys
	- Can't derive private key from the public one
- Key Pair
	- Key Generation
		- Build both public and private key at the same time
		- Lots of randomizing
		- Large Prime Numbers
		- Lots of math
- Protect the private key!
- Key Escrow
	- Someone holds on to your keys
		- Third Party
		- Within Organization
	- Legitimate business arrangement
		- Business needs to access employee information 
		- Government agencies may need to decrypt partner data
	- Controversial


# 🔏 Encrypting Data

### 🏪 Stored Data

- Protect Data on storage devices
	- HDD, SSD, USB, cloud storage, etc
	- Data at rest
- May be certain files
- May be full disk/partition/volume encryption
- Bitlocker, FileVault
- File Encryption
	- EFS, third party utils

### 💽 Database

- Protects stored data and transfer of data
- Transparent encryption
	- Symmetric key encrypts everything in database
	- Must be encrypted and decrypted each time information is pulled
- Record-level encryption
	- Encrypt individual columns
	- Allows for picking and choosing data to encrypt

### 🚇 Transport

- Protect data traversing the network
- Application encrypting
	- HTTPS
- VPNs
	- Provides an encrypted tunnel you can send information through over a network
	- Client-based using SSL/TLS
	- Site-to-site using IPsec

### ➕ Algorithms

- Both sides must have the same algorithms for successful encryption/decryption
- Many different ways
- Details aren't seen by end user
- Advantages and Disadvantages based on algorithm
	- Security, Speed, Complexity

### 🔑 Cryptographic Keys

- While algorithms are usually well known the keys aren't
	- Prevents reverse engineering
	- Key determines the output
	- Keep private keys private
- Keys are subject to attacks
	- Larger keys are harder to brute force
- Symmetric keys
	- 128 bit or larger are common
	- Numbers will grow larger as time goes on
- Asymmetric keys
	- Larger than symmetric
	- Complex calculations of numbers
	- 3072 bits or larger are common
- Weak keys aren't secure by themselves
	- Strengthened by hashing, then hashing again, then hashing again...
	- Called key stretching


# 💱 Key Exchange
