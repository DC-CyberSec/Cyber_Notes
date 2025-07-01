
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

