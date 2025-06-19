# 🔑 Public Key Infrastructure

- Polices, procedures, hardware, software, or people responsible for creating, distributing, managing, storing, or revoking digital certificates
- Big endeavor
	- Lots of planning and decisions
- Associated with binding public keys to people or devices
	- In conjunction with Certificate Authority
	- Based around trust (TEST)

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

- Important to only have keys for the person encrypting or decrypting the data
- Logistical challenge
	- How do you share the keys without transferring them in an unsafe way?
- Out-of-band key exchange
	- Not sent over the net
	- Phone, courier, in person, etc
- In-band key exchange
	- Some information must be sent over the network
	- Faster time
	- Use additional encryption (asymmetric encryption to send a symmetric key)

### 🕐 Real-time Encryption/Decryption

- Need for fast security without compromising security
- Typically done by sharing a symmetric session key using asymmetric encryption
	- Client encrypts a random (symmetric) key with a server's public key
	- Server decrypts shared key and uses it to encrypt data
	- Produces the session key
- Use session keys cautiously
	- Need to be changed often (ephemeral)
	- Need to be unpredictable
- Use public and private key cryptography to create symmetric keys


# 🔐 Encryption Technologies

### 💾 Trusted Platform Module (TPM)

- Piece of hardware specifically designed to provide cryptographic functions
- Generates random numbers and keys
- Has persistent memory so unique keys are burned into memory
- Versatile
	- Storing keys, hardware configuration information
	- Stores Bitlocker keys
- Password protected
	- No way to brute force it
- Used for a single device

### 🔌 Hardware Security Module (HSM)

- Used in larger environments
	- Usually clustered together
	- Redundant
	- Securely store thousands of cryptographic keys
- High-end cryptographic hardware
	- Sometimes a separate device
- Stores keys
	- Used for backups
- Cryptographic accelerators
	- Used to take the load off of the CPU

### 👔 Key Management System

- Can be run on many different devices
	- On-premises, cloud based
- Manage many different keys for many different services from one console
	- Keeps keys and data separate
	- Often third party software
	- Create specific keys for specific services
	- Associate keys with specific users
	- Rotate keys
	- Log key use and events

### 👀 Challenges of keeping data private

- Data is in many different places
	- Phones, computers, laptops, cloud
	- Most private data is usually the physically closest to us
- Attackers are always learning
	- Race to stay one step ahead
- Data is constantly changing

### 📠 Secure Enclave

- Security processor built into systems we're using
	- Sole purpose is data privacy
	- Hardware processor
	- Many different names
- Provides multiple security features
- Own boot ROM
- Monitors system boot process
- Has true random number generator
- Can do real time encryption of data in memory
- Root cryptographic keys
- Performs AES encryption in hardware
- And more


# 🎛️ Obfuscation

- The process of making something unclear
	- Makes things more difficult to understand
	- Not impossible if you know what to understand
- Hide information in plain sight
	- Have to know how it was hidden

### 🖌️ Steganography

- Greek for "concealed writing"
- Hide data in images
	- Security through obscurity
- Message is invisible but still there
- Document containing the data is the cover-text
- Network-based
	- Embedded messages in TCP packets
- Image based
- Watermarking
	- Hide messages in invisible water marks
	- Yellow dots on printers
- Audio based
	- Hide information within audio file or track
- Video based
	- Can be used to hide lots of information

### 📱 Tokenization

- Replace sensitive data with a non-sensitive placeholder
- Commonly used with credit card processing
	- Use temp tokens during payments
	- Attackers can't capture the card number and use it later
- Not encryption or hashing
	- No mathematical relation

### 🤿 Data Masking

- Hides some of the original data
- Protects PII and sensitive data
- Only hidden from view
	- Data can still be in storage
	- Control the view based on permissions
- Different techniques
	- Substituting, shuffling, encrypting, masking, etc


# 🖊️ Hashing/Digital Signatures

### 🍳 Hashes

- Represent data as a short string of text
	- Can be called message digest or fingerprint
- One way 
	- Impossible to recover original message from the digest
- Used for storing passwords/confidentiality
- Can verify downloads (Integrity)
- Can be a digital signature
	- Authentication, non-repudiation, and integrity
- SHA256 hash
	- 256 bit/64 hexadecimal characters
- Collision
	- Hashes should be unique
	- Inputs shouldn't ever create the same hash if they do its called a collision
	- Practically probably wont happen
	- Example
		- MD5 algorithm
- Practicality
	- Verify downloaded files
		- Compare downloaded file hash with posted hash
	- Password storage
		- Instead of strong passwords store salted hashes
		- Compare during authentication
		- Actual password is not shown
- Salting
	- Random data that's added during the hashing process to a password
	- Every user gets their own random salt
		- Commonly stored with the password
	- Protects from rainbow tables
		- Rainbow tables are tables with every possible input and every possible hash associated with those inputs
	- Slows down brute forcing
	- Salting allows different hashing to be created from the same password

### 🖊️ Digital Signatures

- Prove the message was not changed (Integrity)
- Prove the source of the message (Authentication)
- Make sure the signature isn't fake (Non-repudiation)
- Signed with a private key
	- Only signed by one person
- Verify with a public key
	- Any change in the message will invalidate the signature


# ⬛ Blockchain Technology

- Distributed ledger
	- Used to keep track of transactions
- Everyone on the blockchain can manage this ledger
	- Record and replicates to anyone
- Used for anything that requires keeping track of transactions
	- Payment processing
	- Digital identification
	- Supply chain monitoring
	- Digital voting
- Process
	1. Transaction occurs
	2. Results sent to everyone
	3. Results added to a larger block of all transaction results
	4. Hash is added to the block to add integrity
	5. Copy is sent to everyone (all nodes)
	6. Transaction is complete
	7. If the transaction is later modified the hash is invalidated
	8. Everyone becomes aware of the invalid block


# 🎫 Certificates


