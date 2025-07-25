
# 👿 Malware

- Malicious Software
	- Bad
- Gather info
	- Keystrokes
- Advertise
- Viruses and worms
	- Encrypt your data

### 🏹 Types and Methods

- Viruses 
- Worms
- Ransomware
- Trojans
- Rootkit
- Spyware
- Bloatware
- Logic Bomb

### 👨‍💻 How its done

- Work together
	- Worm takes advantage of vulnerability
	- Then installs additional remote access backdoor malware
	- Additional malware is installed later
- Must run a program
	- Email link - Don't click links
	- Web page pop up
	- Drive by download
	- Worm
- Your computer is vulnerable
	- Keep your OS updated

### 🕶️ The Why

- Data is valuable
- Personal Data 
	- Family pictures
	- Videos
	- Important Documents
- Organization data
	- Planning documents
	- Employee PII
	- Financial Information
	- Company Private Data
- What's it worth?

### 🔒 Ransomware

- A particularly nasty malware
	- Data unavailable unless you pay
- Malware encrypts your data files
	- Pictures, documents, music, etc.
	- OS remains working
	- They want it running for you to see
- Must pay for the decryption key
	- Untraceable payment
	- Use of public key cryptography for evil
- Always have a backup
	- Offline backup
- Keep OS up to date
	- Patches
- Keep applications up to date
- Keep your antivirus/antimalware signatures up to date


# 🐛 Viruses and Worms

### 📱 Virus

- Malware that can reproduce
	- Needs a program execution
- Reproduce through the file system or the network
	- Just running a program wont work
- May or may not causes a problem
	- Some are invisible, some are annoying
- Antivirus is very common
	- Thousands of new viruses every week
- Keep signatures updated
- Different types 
	- Program Viruses
		- Part of the application
	- Boot sector viruses
		- No OS
	- Script viruses
		- Operating system and browser based
	- Macro viruses
		- Common in Microsoft Office
- File-less virus
	- Stealthy
		- Avoids antivirus detection
	- Operates in memory
		- Never installed in a file or application

### 🔪 Worms

- Malware that self-replicates
	- Doesn't need you to do anything
	- Uses the network for transmission
	- Self propagates and spreads quickly
- Take over systems quickly
- Firewalls and IDS/IPS can mitigate many infections
	- Not so helpful once the worm is inside


# 👀 Spyware and Bloatware

### 🔎 Spyware

- Malware that spies on you
	- Advertising, identity theft, affiliate fraud
- Can trick you into installing
- Browser monitoring
	- Captures habits
- Key-loggers
	- Captures everything you type
	- Send it to the attacker
- Maintain your antivirus/antimalware
- Always know what you're installing
	- Watch your options during the installation
- Backup
	- Might need it
	- Adware cleaning is a tall task
- Runs some scans
	- Looks for malware

### 🍎 Bloatware

- New computer or phone
	- Includes OS and other "important" apps
- Also includes not needed apps
- Apps are installed by manufacturer
	- You don't get a choice
- Uses storage space
	- Adds to resource usage
	- System slows down
	- Could be exploited
- Identify and remove
	- Easier said than done
- Use builtin uninstaller
	- Most applications
- Some apps have their own uninstaller
- Third party software for uninstalling and cleaning up your system
	- Backup


# 🦴 Other Malware

### ⌨️ Key-loggers

- Keystrokes contain valuable information
	- Login details, passwords, emails, etc.
- Save all of your inputs
	- Send it to the attacker
- Circumvents encryption protections
	- Can't encrypt key strokes
- Other data logging
	- Clipboard logging, screen logging, instant messaging, search engine queries

### 💣 Logic Bomb

- Waits for a predefined event
	- Revenge
- Time bomb
	- Time or date based
- User event
	- Logic bomb
- Difficult to find
	- Difficult to recover if it goes off
	- Each is unique
	- No predefined signatures
- Process and procedures
	- Formal change control
- Electronic monitoring
	- Alert on changes
	- Host-based intrusion detection, Tripwire, etc.
- Constant auditing
	- Help prevent privilege escalation
- March 19, 2013 - South Korea
	- Email with malicious attachment sent to Korean organizations
	- Posed as the bank
	- Trojan installed malware
	- Day later bomb went off
	- Storage and master boot record deleted, system rebooted
	- Operating system was removed

### 🌳 Rootkits

- Originally a Unix technique
	- Root in rootkit (superuser)
- Modifies core system files
	- Part of the kernel
- Can be invisible to the operating system
	- Wont see it in Task Manager
- Also invisible to traditional antivirus
	- Not easy to stop
- Look for unusual
	- Scans
- Use a remover specific to the rootkit
	- Usually built after the rootkit is discovered
- Secure boot with UEFI
	- Security in the BIOS


# 👊 Physical Attacks

- Old school security
	- No technology
- Many different ways to circumvent digital security
	- A physical approach must be considered
- If you have physical access you have full control
	- OS can't stop an in person attack
- Door locks only keep out the honest
	- Always a way in

### 🥾 Brute Force

- Physical version
	- No passwords
- Push through obstruction
	- Brawn
- Check your physical security
	- Windows
	- Doors
- Attackers will use anything
	- Be prepared

### 💳 RFID Cloning

- RFID is everywhere
	- Access badges
	- Key fobs
- Duplicators are cheap
- Takes seconds to do
	- Read one card
	- Copy to another
- MFA is important
	- Use another factor with the card

### 🏕️ Environmental Attacks

- Attack everything supporting the technology
	- Operating environment
- Power monitoring
	- Turn off power
- HVAC and humidity controls
	- Large data centers must be cooled
- Fire suppression
	- Watch for smoke or fire


# 🚫 Denial of Service

- Force a service to fail
	- Overload it
- Take advantage of a vulnerability or design failure
	- Patches
- Cause a system to be unavailable
	- Competitive Advantage
- Create a distraction for another exploit
	- Precursor to another attack
- Doesn't have to be complicated
	- Turn off power

### 😄 Friendly DOS

- Unintentional DoSing
	- Not always on purpose
- Network DoS
	- Layer 2 loop without STP
- Bandwidth DoS
	- Downloading multi-gigabyte Linux distros over a DSL line
- Water line breaks
	- Needs to be cleaned

### 🔌 Distributed Denial of Service (DDoS)

- Launch an army of computers to bring down a service
	- Use all the bandwidth or resources - traffic spike
- Why attackers have botnets
	- Thousands or millions of computers at your command
	- At its peak, Zeus botnet infected over 3.6 million PCs
	- Coordinated attack
- Asymmetric threat
	- The attacker may have fewer resources than the victim
- Turn a small attack into a big attack 
	- Often reflected off another device or service
- Increasingly common network DDoS technique
	- Turn internet services against the victim
- Uses protocols with very few authentication checks
	- NTP, DNS, ICMP
	- Common example of protocol abuse


# 💥 DNS Attacks

### ☠️ DNS Poisoning

- Modify the DNS server
	- Requires some good hacking
- Modify the client host file
	- Host files take precedent over DNS queries
- Send a fake response to a valid DNS request
	- Requires a redirection of the original request or the resulting response
	- Real time redirection
	- On path attack

### ⛵ Domain Hijacking

- Get access to the domain registration and you control where the traffic flows
	- No need to touch actual servers
	- Determines the DNS names and DNS IP addresses
- Many ways to gain access
	- Brute force
	- Social engineering
	- Gain access to the email
	- Usual things
- October 22, 2016 - Domain Registrations of 36 domains are changed
	- Brazilian bank
	- Desktop domains, mobile domains, and more
	- Under hacker control for 6 hours
	- Became the bank
	- 5 million customers, 27 billion USD in assets

### 🚙 URL Hijacking

- Make money from mistakes
	- Lot of advertising online
- Sell the badly spelled domain to the actual owner
- Redirect to a competitor
- Phishing site
- Infect with a drive by download
- Typosquatting/brandjacking
	- Take advantage of poor spelling
- Outright misspelling
- Different top-level domain


# 📟 Wireless attacks

- Wireless authentication
	- Wireless DoS attack
- 802.11 wireless includes a number of management features
	- Frames that make everything work
	- Never seen
- Important to the operation of 802.11 wireless
	- How to find access points, manage QoS, associate/disassociate with an access point, etc.
- Original wireless standards did not add protection for management frames
	- In the clear, no authentication or validation
- Protection against
	- IEEE already addressed the problem
		- Updates included with 802.11ac
	- Some of the important management frames are encrypted
		- Disassociate, deauthenticate, channel switch announcements, etc.
	- Not everything is encrypted
		- Beacons, probes, authentication, association

### 📻 RF Jamming

- DoS
	- Prevent wireless communication
- Transmit interfering wireless signals
	- Decrease the signal to noise ratio at the receiving device
	- The receiving device cant hear the good signal
- Sometimes not intentional
	- Interference
	- Microwave oven, fluorescent lights

### 📡 Wireless Jamming

- Different types
	- Constant, random bits / Constant, legitimate frames
	- Data sent at random times - random data and legitimate frames
	- Reactive jamming - only when someone else tries to communicate
- Needs to be close by
	- Difficult from a distance
- Time to go fox hunting
	- Directional antenna, attenuator


# 🏞️ On Path Attacks

- How can an attacker watch without you knowing
	- Formerly known as a man in the middle attack
- Redirects your traffic
	- Passes it on to a destination
	- No idea when traffic is redirected
- ARP Poisoning
	- On path attack on the local IP subnet
	- No security
- What if the middleman was on the same computer as the victim?
	- Malware/Trojan does all the proxy work
	- Man-in-the-browser
- Huge advantages
	- Easy to proxy encrypted traffic
	- Everything looks normal
- Malware in your browser waits for you to login
	- Cleans you out


# 📹 Replay Attacks

- Useful information is transmitted over the network
	- Hackers take advantage of this
- Need access to raw network data
	- Network tap, ARP poisoning, Malware
- The gathered information helps the attacker
	- Replay the data to appear as someone else
- Not an on path attack
	- Replay doesn't require the original workstation
- Avoid with salting or encryption
	- Can't capture session IDs if they cant see it
	- Encryption adds load on HTTPS server
	- Firefox extensions: HTTPS Everywhere, Force TLS
	- Many sites are HTTPS only now
- Encrypt end-to-end
- Encrypt end-to-somewhere
	- Avoid capture over a local wireless network
	- In the clear for part of the journey
	- Personal VPN 

### 🍪 Browser cookies and session IDs

- Cookies
	- Information stored on your computer by the browser
- Used for tracking, personalization, session management
	- Not executable, not generally a security risk
		- Unless someone gets access
- Could be a privacy risk
	- Lots of personal data
- Session IDs are often stored in the cookies
	- Maintains sessions across multiple browser sessions

### ⚽ Header Manipulation

- Information gathering
	- Wireshark, Kismet
- Exploits
	- XSS
- Modify headers
	- Tamper, Firesheep, Scapy
- Modify cookies
	- Cookie browser add-ons


# 🕴️ Malicious Code

- Attackers use any opportunity
	- Many types of malicious code
- Different forms
	- Executable, scripts, macro viruses, worms, Trojans, etc.
- Protection comes from many different sources
	- Anti-malware
	- Firewall
	- Continuous updates
	- Secure computing habits
- Examples
	- WannaCry ransomware
		- Executable exploited a vulnerability in Windows SMBv1
		- Arbitrary code execution
	- British Airways XSS
		- 22 lines of malicious JavaScript code on pages used to checkout
		- Information stolen from 380,000
	- Estonian Central Health Database
		- SQL injection
		- Breached all healthcare information for an entire country


# 📱 Application Attacks

### 💉 Injection Attack (see 2.3)


### 🏞️ Buffer Overflows (see 2.3)


### 📼 Replay Attack (see above)


### 🛫 Privilege Escalation

- Gain higher-level access to a system
	- Exploit a vulnerability
	- Might be a bug or design flaw
- Higher-level access means more capabilities
	- A concern for attackers
- High-priority vulnerability patches
	- Get it fixed very quickly
- Horizontal privilege escalation
	- User A can access User B's resources
- Update anti-virus/anti-malware software 
- Data Execution Prevention
	- Only data in executable areas can run
- Address space layout randomization
	- Prevent a buffer overrun at a known memory address

### ❌ Cross-Site Requests

- Cross-site requests are common and legit
	- You visit a website
	- The browser loads the content from the server
	- Browser loads videos and pictures
	- Different servers used to load
- HTML on the website directs requests from your browser
	- Normal and expected
	- Most of these are unauthenticated requests
- Website pages consist of client-side code and server-side code
	- Moving parts
- Client-side
	- Renders the page 
	- HTML, JS
- Server-side
	- Performs request from client
	- HTML, PHP
	- Transferring funds
	- Post media

### ☄️ Cross-site Request Forgery

- One-click attack, session riding
	- XSRF, CSRF (sea surf)
- Takes advantage of the trust a web application has for a user
	- Website trusts your browser
	- Requests are made without consent or knowledge
	- Attacker posts a Facebook status on your account
- Significant web application development oversight
	- The application should have anti-forgery techniques added
	- Usually a cryptographic token to prevent forgery

### 🚈 Directory Traversal / Path Traversal

- Read files form a web server that are outside of the website's file directory
- Users shouldn't be able to browse the Windows folder
- Web server software vulnerability
	- Won't stop users from browsing past the web server root
- Web Application code vulnerability
	- Take advantage of poorly written code


# 🔏 Cryptographic Attacks

- You encrypt data and send it off
	- Is it secure
	- How do you know
- The attacker doesn't have the key
	- So they break the cryptography
- Finding ways to undo the security
	- Many potential shortcomings
	- Problem is often the implementation

### 🎂 Birthday Attack

- Hash collision
	- The same hash for two different plaintexts
	- Found through brute force
- Attacker will generate multiple versions of plaintext to match the hashes
	- Protect with large has output sizes
- Hash digests are supposed to be unique
	- Different input data shouldn't create the same hash
- MD5 hash
	- Message digest Algorithm 5 
	- Published 1992
	- Collisions found 1996
- December 2008: Researchers created CA certificate that appeared legitimate when MD5 is checked
	- Built other certificates that appeared to be legit and issued by RapidSSL

### 🔽 Downgrade Attack

- Instead of using perfectly good encryption, use something that isn't so great
	- Force systems to downgrade their security
- SSL stripping
	- Combines an on path attack with a downgrade attack
	- Difficult to implement, but big rewards
	- Attacker must sit in the middle of the conversation
	- Victims browser page isn't encrypted
	- Strips the S from HTTPS


# 🔑 Password Attacks

- Some applications store passwords in the clear
	- Not encrypted
	- Rare
- Do not store passwords as a plaintext
	- Anyone with access to the password file or database has the credentials
- What to do 
	- Get better application
- Hash a password
	- Hashes represent data as a fixed-length string of text
		- Digest or fingerprint
	- Will not have a collision
	- One-way trip
		- No way to reverse engineer
	- Stored in a file
		- Different across OS

### 🚿 Spraying Attack

- Try to login with an incorrect password
	- Eventually locked out
- Are some common passwords
- Attack an account with the top three most common password
	- If this doesn't work move on to next account
	- No lockouts, no alarms, no alerts

### 🥾 Brute Force

- Try every possible password combination
- Might take some time
	- Strong hashing algorithms slow it down
- Receive the hash
- Match it to every possible iteration of passwords til correct
- Online
	- Very slow
	- Most accounts will lockout
- Offline
	- Obtain list of users and hashes
	- Calculate password hash and compare to stored hash
	- Large computational resource requirements


# ⚠️ Indicators of Compromise

- An event that indicates an intrusion
	- Confidence is high
- Indicators
	- Unusual activity on network
	- Change to file hashes
	- Irregular international traffic
	- Changes to DNS data
	- Uncommon login patterns
	- Spikes of read requests to certain files

### 🔒 Account Lockout

- Credentials are not working
	- Wasn't you
- Exceeded login attempts
	- Account is auto locked
- Account was administratively disabled
	- Large concern
- Might be a larger plan
	- Attacker locks account
	- Calls pretending to be user needing unlock

### 2️⃣ Concurrent Session Usage

- Can't be two places at once
- Multiple logins from multiple locations
	- Interactive access from a single user
- Can be difficult to track down
	- Multiple devices and desktops
	- Automated processes

### 🧱 Blocked Content

- An attacker wants to stay as long as possible
	- System is unlocked
	- Keep it that way
- Probably a patch available
	- Play keep away
- Blocked content
	- Auto-update connections
	- Links to security patches
	- Third party anti-malware sites
	- Removal tools

### ✈️ Impossible Travel

- Authentication logs can be telling
- Multiple logins from very different places should raise alarms
- Should be easy to identify

### 🖥️ Resource Consumption

- Every attacker's action has an equal and opposite reaction
	- Watch carefully for significant changes
- File transfers use bandwidth
	- Unusual spike
- Firewall logs show the outgoing transfer 
	- IP addresses, timeframes
- Often the first real notification of an issue
	- Attacker may have been there for a long time
- Inaccessibility
	- Servers down
	- Network disruption
		- Cover for other exploits
	- Server outage
		- Result of exploit gone wrong
	- Encrypted data
		- Ransomware
	- Brute force
		- Lockout

### 🚲 Out-of-cycle logging

- Occurs at an unexpected time
- Operating system patch logs
	- Occurring outside of normal patch times
	- Keep the system safe from attackers
- Firewall logging activity
	- Timestamps of every traffic flow
	- Protocols and applications used

### 🌲 Missing Logs

- Log information is evidence
	- Attackers will try to cover tracks
- Information is everywhere
	- Auth logs
	- File Access logs
	- Firewall logs
	- Server logs
	- Proxy logs
- Logs might be incriminating
	- Missing logs are suspicious
	- Logs should be secured and monitored

### 🖊️ Published / Documented

- Entire attack and data exfil may go unnoticed
- Company data may be published online
	- May be in conjunction with ransomware
- Raw data may be released without context
	- Researchers will try to find source






