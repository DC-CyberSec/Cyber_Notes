
# 👿 Malware

- Malicous Sofwatre
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
	- then installs additional remote access backdoor malware
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


