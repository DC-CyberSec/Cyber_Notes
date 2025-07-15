
# 🧠 Memory Injections

- Malware runs in memory
	- Memory forensics can find malicious code
- Memory is a bunch of running processes
	- DLLs (Dynamic Link Libraries)
	- Threads
	- Buffers
	- Memory Management functions
	- Etc.
- Malware is in there somewhere
	- Malware runs its own process
	- Also injects itself into legit processes
- Add code into the memory of an existing process
	- Then can hide malware inside of the process
- Gets access to the data in that process
	- Same rights and permissions as the process it injected itself into
	- Perform privilege escalation

### 📖 Dynamic Link Libraries (DLL) Injections

- Dynamic Link Library
	- A windows library containing code and data
	- Used by many applications
- Attackers inject a path to a malicious DLL
	- Runs as part of the target process
- One of the most popular memory injection methods
	- Relatively easy


# 💪 Buffer Overflows

- Overwriting a buffer of memory
	- Overflows into another area of memory
- Developers perform bounds checking
	- Attackers spend time looking for openings
- Not a simple exploit
	- Takes time to avoid crashes
	- Takes time to make it do what you want
- A useful buffer overflow is one that is repeatable
	- Always able to compromise a machine


# 🏎️ Race Conditions

- A programming conundrum
	- Things can happen at the same time
	- Bad if its not planned
- Time-of-check to time-of-use attack (TOCTOU)
	- Check the system
	- When do you see the results?
	- Something might change between the check and use
- Can cause big problems
	- 2004 - Mars rover "Spirit"
		- Reboot if problem is identified
		- File system problem occurs so reboot
		- Result is a reboot loop
	- 2023 Pwn2Own Vancouver - Tesla Model 3
		- TOCTOU attack against the Tesla's infotainment using Bluetooth
		- Elevated privileges to root
		- Won the competition


# ⬆️ Malicious Updates

### 🥎 Software Updates

- Always keep your OS and applications up to date
	- Updates often include security patches and bug fixes
- This update process has its own security concern
	- Not every update is secure
- Follow best practices
	- Always have a backup
	- Install from trusted sources
	- BACKUP

### ⬇️ Downloading/Updating

- Install updates form a downloaded file
	- Always consider the actions
	- Every installation could be dangerous
- Confirm the source
	- A random pop up may not be legit
- Visit the developers site directly
	- Don't trust random update buttons
- Many OS's only allow updates that are digitally signed
	- Always enable those security controls

### 🛺 Automatic Updates

- The app updates itself
	- Often includes security checks and digital signatures
- Relatively trustworthy
	- Comes directly from the developer
- SolarWinds Orion supply chain attack
	- December 2020 reported
	- Attackers gained access to the entire SolarWinds development system
	- Added their own malicious code to the updates
	- Gained access to hundreds of government agencies and companies


# 🖥️ Operating System Vulnerabilities

### 🏗️ Operating Systems

- Foundational computing platform
	- Used by everyone
	- Very big target
- Remarkably complex
	- Millions of lines of code
	- More code means more security issue chances
- Vulnerabilities are there
	- Just haven't been found yet

### 📈 Monthly Example

- Windows patches are rolled out every month
	- Patch Tuesday - 2nd Tuesday of every month
	- Other companies have similar schedules
- May, 9 2023 - Nearly 50 security patches
	- 8 Elevation of Privilege vulnerabilities
	- 4 Security features bypass vulnerabilities
	- 12 Remote code execution vulnerabilities
	- 5 DOS vulnerabilities
	- 8 Information disclosure vulnerabilities
	- 1 Spoofing vulnerability

### 🏆 Best Practices

- Always Update
	- Monthly or on demand
	- Race between attackers and you
- May require testing before deployment
	- Patch might break something
- May require a reboot
	- Save everything
- Have a backup


# 💉 Code Injection 

- Adding your own information into a data stream
- Enabled by bad programming
	- The application should properly handle inputs and outputs
- Many different types
	- SQL, XML, LDAP, HTML, etc.

### 💽 SQL Injection

- SQL - Structured Query Language
	- Most common relational database management system language
- Injections - (SQLi)
	- Put your own SQL requests into an existing application
	- Shouldn't be allowed
- Can be executed in a web browser
	- Inject into a form or field
- This could be very bad
	- View all database information, delete database, make changes, or bring the database down

### ❎ Cross Site Scripting (XSS)

- Originally called cross site scripting because of vulnerabilities found in browsers
	- Information from one site shared with another
- One of the most common web app vulnerabilities
	- Takes advantage of the trust a user has for a site
	- Complex and varied
- XSS commonly uses JavaScript
	- Allowing scripts?

### ⌛ Non-persistent (reflected) XSS attack

- Web site allows scripts to run in user input
	- Search box is a common source
- Attacker emails a link that takes advantage of this vulnerability
	- Runs a script that sends information to the attacker
- Scripts embedded in URLs run in the victims browser
	- Looks like it came from the server
- Attackers uses stolen credentials, cookies, session IDs to steal victims information without their knowledge

### ⏳ Persistent (stored) XSS attack

- Attacker posts a message on social media
	- Includes malicious payload
- Now "persistent"
	- Stored 
	- Everyone gets the payload
- No specific target
- For social networking sites this can spread quickly
	- Everyone who views this message could post it

### 🚗 Subaru Example

- June 2017, Aaron Guzman
	- Security Researcher
- When authenticating with Subaru users get a token
	- Token never expired (!!)
- A valid token allows any service request on your vehicle
	- Even adding your email address to someone else account
	- Full access to someone else's car
- Web front-end included a XSS vulnerability
	- User clicks a malicious link, and you have their token

### 🛡️ Protecting against XSS

- Be careful with untrusted links
	- Never blindly open random links
- Consider disabling JavaScript
	- Controlled with browser plugins
	- Limited protection
- Keep browser and applications updated
	- Avoids vulnerabilities
- Validate input
	- Don't allow users to add scripts to input fields


# 🔌 Hardware Vulnerabilities

- We are surrounded by hardware devices
	- Not always an easy accessible operating system
- Anything connected to the network is a security risk 
	- Entry point for attackers
- IoT
	- Internet of things
	- Light bulbs, door locks, fridge, garage doors
- Security landscape always growing

### 📏 Firmware

- The software inside of hardware
	- Operating system of hardware devices
- Vendors are the only ones who can really fix their hardware
	- Assumes they care and know how to fix
- Trane Comfortlink 2 thermostats
	- Control temperature from a mobile device
	- Trane was notified of three vulnerabilities in April 2014
	-  Finally fully patched by January 2016

### 🔚 End of Life 

- EOL
	- Manufacturer stops selling a product
	- May still be supporting the product
	- Important for security patches and updates
- End of service life (EOSL)
	- Manufacturer stops selling
	- Support no longer available
	- No ongoing security patches or updates
	- May have a premium support option 
- Tech EOSL is a significant concern
	- Security patches are very important

### 👴 Legacy platforms

- Some devices remain installed for a long time
- Legacy devices
	- Old operating systems, applications, middle-ware
- May be running EOL software
	- Compare risk to the return
- May require additional security protections
	- Additional rules
	- IPS signatures for older operating systems


# 🏞️ Virtualization Vulnerabilities

- Very different form non-virtual machines
	- Can appear anywhere
- Quantity of resources vary between VMs
	- CPU, memory, storage
- Many similar aspects to physical machines
	- Complexity adds opportunity for the attackers
- Virtualization vulnerabilities
	- Local privilege escalation
	- Command injection
	- Information disclosure

### 🦿 VM escape prevention

- The virtual machine is self contained
	- No way out USUALLY
- VM escape
	- Break out of the VM and interact with the host operating system or hardware
- Once you escape the VM you have great control
	- Control the host and control other VMs
- Huge exploit
	- Full control of the virtual world
- March 2017 - Pwn2Own competition 
	- Hacking competition
	- Used a bug in the javascript engine of Microsoft Edge
		- Code executed in Edge sandbox
	- Windows 10 kernel bug
		- Compromise the guest operating system
	- Hardware simulation bug in VMWare 
		- Escape to host

### ♻️ Resource Reuse

- The hypervisor manages the relationship between virtual and physical resources
	- Available RAM, CPU, storage space, etc.
- These resources can be reused between VMs
	- Hypervisor with 4 GB of RAM
	- Supports three VMs with 2 GB of RAM each
	- RAM is allocated and shared between VMs
- Data can be inadvertently shared between VMs
	- Time to updated the memory management features
	- Security patches can mitigate risk


# 🌥️ Cloud Vulnerabilities

- Cloud adoption has been nearly universal
	- Its difficult to find a company NOT using the cloud
- We've put sensitive data in the cloud
	- Attackers want
- We're not using the best practices
	- 76% of organizations aren't using MFA for management console users
	- 63% of code in production is unpatched
	- Vulnerabilities rated high or critical (CVSS >= 7.0)

### 🌩️ Cloud Attacks

- Attacks on Service
	- Denial of Service
		- Fundamental attack type
	- Authentication bypass
		- Take advantage of weak or faulty authentication
	- Directory traversal
		- Faulty configurations put data at risk
	- Remote code execution
		- Take advantage of unpatched systems
- Attacks on Applications
	- Web application attacks have increased
		- Log4j and Spring Cloud function
		- Easy to exploit, rewards are extensive
	- Cross Site scripting 
		- Take advantage of poor input validation
	- Out of bounds write
		- Write to unauthorized memory areas
		- Data corruption, crashing, or code execution
	- SQL Injection
		- Direct access to databases


# 🚚 Supply Chain Vulnerabilities

- The chain contains many moving parts
	- Raw materials, suppliers, manufacturers, distributors, customers, and consumers
- attackers can infect any step along the way
	- Infect different parts without suspicion
	- People trust their suppliers
- One exploit can poison the entire chain
	- Lot at stake

### 👨‍🔧 Service Providers

- You can control your own security posture
	- Cant control a service provider
- Service providers usually have access to internal systems
	- Opportunity for attackers
- Many different types of service providers
- Consider ongoing security audits of all providers
	- Included in contract
- Target Corp Breach - November 2013
	- 40 million credit cards stolen
	- HVAC firm was infected
		- Malware delivered in email
		- VPN credentials stolen for HVAC techs
	- HVAC vendor was Target's supplier
		- Attacker used these networks to infect the cash registers

### ⌨️ Hardware Providers

- Can you trust your new router/firewall/system/switch/software?
	- Supply chain risk
- Use a small supplier base
	- Tighter control
- Strict controls over policies and procedures
	- Ensure proper security in place
- Security should be a part of overall design
	- Limit to trust
- All network traffic flows through switches and routers
	- Perfect visibility and pivot point
- July 2022 - DHS arrests reseller CEO 
	- Sold over 1 billion counterfeit Cisco products
	- Created over 30 companies
	- Been selling since 2013
	- Knocks-offs made in China
	- Sold as authentic Cisco products
	- Broke and caught on fire

### 🍦 Software Providers

- Trust is a foundation of security
	- Every software installation questions our trust
- Initial installation
	- Digital signature should be confirmed upon installation
- Updates and patches
	- Some software updates are automatic
	- How secure are the updates
- Open source is not immune
	- Compromising the source code itself
- SolarWinds Orion
	- Used by 18,000 customers
	- Fortune 500 customers and Federal Government
	- Software Updates were compromised March and June 2020
	- Not detected until December 2020


# 💥 Misconfiguration Vulnerabilities

- Open Permissions
	- Easy to leave a door open
		- Someone will find it
	- Increasingly common with cloud storage
		- Statistical chance of finding an open permission
	- June 2017 - 14 million Verizon records exposed
		- Third party left an Amazon data repository open
		- Researchers found it before any one else
- Unsecured Admin Accounts
	- Linux root account
		- Windows Admin or superuser account 
	- Can be a misconfiguration 
		- Intentionally configuring a easy to guess password
	- Disable direct login to the root account
		- Use the su or sudo option
	- Protect accounts with root or admin access
- Insecure Protocols
	- Some protocols aren't encrypted
		- All traffic in the clear
		- Telnet, FTP, SMTP, IMAP
	- Verify with a packet capture
		- View everything sent over the network
	- Use encrypted version
		- SSH, SFTP, IMAPS, etc.
- Default settings
	- Every application and network device has a default login
		- Not always changed
	- Mirai botnet
		- Takes advantage of default credentials
		- Takes over IoT devices
		- 60+ default configurations
		- Cameras, routers, doorbells, garage door openers, etc.
		- Open source
	- Open ports/services
		- Services will open ports
			- Manage access
		- Often managed via Firewall
			- Manage traffic flows
			- Allow or deny based on port number or application
		- Firewall rulesets can be complex
			- Easy to mess up
		- Always test and audit


# 📱 Mobile Device Vulnerabilities

- Challenging to secure
	- Often need additional policies and procedures to provide security
- Relatively small
	- Can almost be invisible
- Almost always in motion
	- Never know where it is
- Packed with sensitive data
	- Personal and organizational
- Constantly connected to the internet
	- Anyone can gain remote access

### ⛓️ Jailbreaking/rooting

- Mobile devices are purpose built
	- Don't have access to operating system
- Gaining access
	- Android - rooting
	- IOS - Jailbreaking
- Install custom firmware
	- Replaces existing firmware
- Uncontrolled access 
	- Circumvent security features and MDMs

### 📂 Sideloading

- Malicious apps can be a significant concern
	- One Trojan can contain a data breach
- Manage installation sources
	- Global or local app store
- Sideloading circumvents security
	- Apps can be installed manually without any app store
	- No use for MDM


# 🎃 Zero-day Vulnerabilities

- Many applications have vulnerabilities that haven't been found yet
- Someone is working hard ti find the next big vulnerabilities
	- Good guys share with developers
- Attackers keep these vulnerabilities to themselves
	- Used for personal gain

### 👊 Zero-day Attacks

- Attackers search for unknown vulnerabilities
	- Create exploits against these
- Vendor has no idea
	- Don't have a fix
- Zero day attacks
	- An attack without a patch or mitigation method
	- Race to exploit or create a patch
	- Difficult to defend against the unknown
- Common Vulnerabilities and Exposures (CVE)
- April 2023 - Chrome zero-day
	- Memory corruption, sandbox escape
- May 2023 - Microsoft zero-day
	- Secure boot zero-day vulnerability
	- Attacker can run UEFI-level self signed code
- May 2023 - Apple IOS and IpadOS zero-day
	- Three patches
	- Sandbox escape, disclosure of sensitive information, arbitrary code execution
	- Active exploitation





