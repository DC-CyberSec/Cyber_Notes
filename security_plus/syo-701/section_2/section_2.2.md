# 💨 Threat Vectors 

- Methods used by attackers 
	- Gain access to or infect targets
	- Also called attack vectors
- Lots of work goes into finding these
	- Some more dangerous than others
- Professional Careers in finding and monitoring these vectors

###  💬 Message based vectors

- One of the biggest and most successful threat vectors
	- Everyone uses messages
- Email
	- Malicious links
- SMS 
	- Attacks in texts
	- Direct to you
- Phishing attacks
	- People want to click links
	- Links sent via text or email
- Deliver malware to the user
	- Attach it in emails
	- Never launch untrusted links
- Social engineering attacks 
	- Invoice scams
	- Crypto scams

###  🖼️ Image based vectors

- Easy to identify a text based threat 
	- It’s more difficult to find these threats in an image
- Some image formats are threats
	- The SVG (scalable vector graphic) format
	- Image is described in XML (extensible markup language)
- Significant security concerns 
	- HTML injection
	- JavaScript attack code within
- Browsers must provide input validation 
	- Avoids running malicious code

### 📁 File based vectors

- More than just executables 
	- Malicious code can hide anywhere 
- Adobe PDF
	- A file format containing other objects
- ZIP/RAR files or any compression type
	- Contains many different files
- Microsoft office 
	- Documents with macros
	- Add in files

### 🗣️ Voice call vectors

- Vishing 
	- Phishing over phone
- Spam over IP 
	- Large scale phone calls
- War dialing
	- Unpublished phone numbers to gain access to
- Call tampering
	- DOS attack

### 💽 Removable device vectors 

- Get around the firewall
	- USB interface
- Malicious software on USB flash drives 
	- Infect air gapped network
	- Industrial systems, high security services 
- USB devices can act as keyboards 
	- Hacker on a chip
- Data exfiltration 
	- Terabytes of data walking out the door
	- Zero bandwidth usage 

### 📱 Vulnerable software vectors

- Client based
	- Infected executable
	- Known or unknown vulnerability 
	- Requires constant updates 
- Agentless
	- No installed executable 
	- Compromised software on the server would affect all users
	- Client runs a new instance each time

### 🧭 Unsupported systems vectors

- Patching is an important prevention tool
	- Ongoing security fixes
- Unsupported systems aren’t patched
	- May not be an option
- Outdated operating systems 
	- Eventually even the manufacturer gives up
- A single system could be an entry
	- Keep your records and inveotry up to date

### 🚠 Unsercure network vectors

- The network connects everything 
	- Ease of access for attackers
	- View all information in the clear
- Wireless
	- Don’t use outdated security protocols (WEP, WPA, WPA2)
	- Open or rogue networks are bad
- Wired 
	- Unsecure interfaces -  No 802.1X
- Bluetooth
	- Implementation vulnerability 
	- Recon

### ⛴️ Open service ports

- Most network based services use a TCP or UDP open port to connect
- Every open port is an opportunity for attacks 
	- Application vulnerability or misconfiguration 
- Every application has its own port
	- More services more open ports less security
- Firewall rules 
	- Must allow traffic to open ports 
	- Limits attack surface 

### 🔟 Default credentials

- Most devices have default credentials 
	- Change them
- The right credentials provide full access
	- Admin access
- Very easy to find default credentials

### 🏗️ Supply chain vectors

- Tamper with the underlying infrastructure or manufacturing process
- Managed service providers 
	- Access many different customer networks from one location 
- Gain access to a network using a vendor
	- 2013 Target CC breach
- Suppliers 
	- Counterfeit networking equipment 
	- Install back doors, substandard performance and availability 
	- 2020 Fake Cisco Catalyst switches


# 🎣 Phishing

- Social engineering with a touch of spoofing
	- Often delivered by email, text, etc.
	- Impressive when done well
- Don’t get fooled
	- Check the url
- Usually something that’s off
	- Spelling, fonts, graphics

### 📧 Business email compromise 

- We tend to trust email sources
	- Attackers take advantage of this
- Spoofed email addresses 
	- Not really a legitimate email
	- Looks like the same
- Financial fraud
	- Send out emails with changed banking information 
	- Modify wire transfers
- Have you click a link
	- Attachments have malware

###  🔮 Tricks and misdirection 

- How are they successful 
	- Digital slight of hand
- Typosquatting
	- A type of URL hijacking
- Pretexting
	- Lying to get information
	- Attacker is a character in a story they write 

### 🎏 Different types of Phishing 

- Vishing done over the phone
	- Caller ID spoofing
	- Fake security checks or bank updates
- Smishing is done by text
	- Spoofing is a problem here as well 
	- Forward links or ask for PI
- Variations on a theme
	- The fake check scam, phone verification code scam, CEO scam, advance fee scam


# 🕵️‍♂️ Impersonation 

### 🌟 Pretext

- Before the attack you have to set the trap
	- Actor and story
- Attackers pretend to be someone else
- Use some details from recon
	- Someone you trust
- Attack the victim as someone higher up
- Throw tons of jargon around
- Be friendly

###  ⚔️ Eliciting information

- Extracitng information from the victim
	- May not realize it
	- Hack the human
- Often used in Vishing
	- Easier over the phone
- Well documented psychological techniques 
	- Can't just ask

###  🕶️ Identity Fraud

- Your identity can be used by others
	- Keep personal information personal
- Credit card fraud
	- Open an account in your name or use your card information 
- Bank fraud
	- Attackers open a bank account in your name
- Loan fraud
	- Your information used for loans or leases
- Government benefits fraud
	- Attacker gets benefits on your behalf

### 🛡️ Protect against impersonation

- Never volunteer info
	- Most support teams don’t need passwords
- Don’t disclose personal information
	- Not over phone or email
- Always verify before revealing information 
	- Call back, third parties 
- Verification should be encouraged 
	- Especially with important information 


# 🐃 Watering Hole Attacks

- Used on really secure networks
- Try to gain access to systems people will use later on
	- Requires research
- Determine which website the victim uses
	- Local sites (cafes)
	- Industry related sites
- Infect the third party site
	- Site vulnerability 
	- Email attachments
- Infect all visitors 
	- Wait for a specific one

### 🔰 Prevention

- Defense in depth 
	- Layered defense
	- Never one thing
- Firewalls and IPS
	- Stops network traffic before things get bad
- Anti virus and anti malware signature updates
	- Stops attack code by generic signatures


# 🎩 Other Social Engineering Attacks

###  📳 Misinformation/disinformation 

- Disseminating factually incorrect information 
	- Create confusion and division
- Influence campaigns 
	- Sway public opinion on political and social issues
- Nation state actors
	- Divide distract and persuade 
- Advertising
	- Voice an opinion 
- Social media 
	- Very popular for misinformation 

### 🎢 The process

1. Create fake users
2. Create content
3. Post on socials
4. Amplify message
5. Real users share the information 
6. Mass media picks it up

###  ™️ Brand Impersonation 

- Pretend to be a well known brand
	- Apple, Coca Cola, Google, etc.
- Create thousands of impersonation sites
	- Get into the Google index, click an ad, get a pop up message
- Visitors hit with pop ups
	- Sweepstakes, you won so and so, etc.
- Malware infection is very common
	- Display ads, track sites you visit, data exfiltration