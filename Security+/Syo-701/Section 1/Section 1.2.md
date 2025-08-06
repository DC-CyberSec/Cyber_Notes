# 📐 The CIA Triad

- Easy way to remember the fundamentals of security
- Confidentiality
	- Prevent disclosure of information to unauthorized individuals
- Integrity
	- Data cannot be modified without detection
- Availability 
	- All systems remain up and running

### 💼 Confidentiality

- Certain information needs to be kept secret
- Encryption
	- Encode messages so only one person can read it
- Access controls
	- Restrict access to certain resources
- MFA
	- Additional checks before information is given

### 🤝 Integrity

- Data is stored and transferred as originally intended
	- No unidentified modification
- Hashing
	- Create a string of code specific to the data and map it to that data
	- String is changed if the data is modified
- Digital Signatures
	- Hashes encrypted with asymmetric encryption
	- Verifies integrity of sender
- Certificates
	- Used with signatures to verify sender
- Non-repudiation
	- Confirms integrity

### 🔓 Availability

- Information is accessible to the right people
- Redundancy
	- Systems are designed to always be available
- Fault tolerance
	- Systems can keep running even when they break
- Patching
	- Increases stability
	- Closes vulnerabilities


# 🗨️ Non-repudiation

- You can't take back words or signatures
- Contracts
	- Signatures can be verified
- Authentication perspective of cryptography

### 🗄️ Proof of Integrity

- Verification that data is the same
	- Accurate and consistent
- Hashing
	- Short string of text that is created based on data within plain text
		- Message digest or fingerprint
		- If data changes so does the hash
		- Only used to see if data is modified nothing else

### 🆕 Proof of Origin

- Prove the message is the same (Integrity)
- Prove the source of the message (Authenticity)
- No fake signatures (Non-repudiation)
- Private keys are cryptography's signatures
	- No one else can use this key
- Private keys are verified with public keys associated with them


# 🖼️ Authentication, Authorization, and Accounting

- Identification
	- Who you claim to be
- Authentication
	- Prove who you are
- Authorization
	- What do you have access to
- Accounting
	- Log what happens

### 💻 Authenticating Systems

- Manage many devices youll probably never see
- Computers cant type passwords for proof
- Digitally signed certificates on devices used for authentication
	- Access to VPNs
	- Management software

### 🎫 Certificate Authentication

- Certtificate Authority
	- Most orgs have their own
	- Creates a certificate for a device
	- Signs the certifcate over and can now be used as validation

### 📉 Auth Models

- What do authorized users have access to?
- Authorizes user and services to certain types of data
- Helps with scalability
- Abstraction
	- Reduces complexity
	- Defines relationships between users and resources
	- Streamlines administration


# 🌉 Gap Analysis

- Where we are vs where we want to be
- Understand what is needed in the future
- Complex Process
- Can take weeks or months to compile information

### 🖼️ Frameworks

- Known baseline
	- Internal set of goals 
	- Formal standards
- Organizations for baselines
	- NIST 800-171 Revision 2
	- ISO/IEC 27001
- Analysis of People
	- Experience
	- Training
	- Knowledge of security policies and procedures
- Evaluation of central IT systems

### 🔍 Compare/Contrast

- Evaluate existing systems
- Identify weakness and what is needed to change
- Detailed analysis
	- Broad understanding broken down into different pieces
- Final Report
	- Detailed baseline objectives
	- Clear view of the current state
	- Path from current state to goal
		- Include time, money, change control
	- Document recommendations


# 0️⃣ Zero Trust

- Many networks are very open once inside
- Zero trust is a holistic approach to network security
	- Trust no one
	- Covers every device, process, user, etc
	- Everything must be verified

### ✈️ Planes of Operation

- Helpful for implementing zero trust
- Split network into smaller functional planes
	- Applies to physical, virtual, and cloud
- Data Plane
	- Processes frames, packets, and network data
	- Processing, forwarding, trunking, encrypting, NAT
- Control Plane
	- Manages the actions of data plane
	- Policies, rules, configurations
	- Routing tables, session tables, NAT tables
	- Dynamic routing protocols
- Management Plane
	- Configure and manage device
	- SSH, Browser, API
- Separate into functional tasks
	- Incorporate into hardware and software

### 🤝 Trust Control

- Adaptive Identity
	- Examines identity of individual and apply controls
	- Considers source and the requested resources
	- Risk Indicators - Relationships, location, connection type, IP, etc
	- Increase authentication if needed
- Threat scope reduction
	- Limit places used to get into network
	- Decrease entry points
- Policy driven access control
	- Examines all data points and combines them to determine what authentication should be used

### 🚥 Security Zones

- Where is someone connecting from?
- Security is more than just a one-to-one relationship
- Where is someone trying to connect to?
- Create different sections of security
	- Allows for rules to be set depending on the section
	- Example: Auto deny anyone access coming from an untrusted to trusted zone
	- Implicit trust: Devices are automatically trusted coming from these zones

### 🚔 Policy Enforcement Point

- Used to enforce security rules
- Any subjects and systems that pass through will be evaluated
- Gatekeeper
- Allow, monitor, and terminate connections

### 👨‍⚖️ Policy Decision Point

- Responsible for examining information from PEP and making a decision on authentication 
- Made up of Policy Engine and Administrator
- Policy Engine
	- Evaluates requests and compares the result to predefined security polices
	- Grants, denies, revokes
- Policy Administrator
	- Takes the decision from Policy Engine and provides it to the PEP 
	- Generates access tokens or credentials


# 🛢️ Physical Security

### 🚫 Barricades/Bollards

- Prevents access 
- Channel people through certain access points
	- Allow foot traffic prevent automotive traffic
- Security notices
	- Safety concerns
- Extreme cases
	- Moats, bridges 

### 🚡 Access Control Vestibule

- Doors start unlocked
	- Opening one door causes the others to lock
- All door start locked
	- Unlocking one prevents unlocking of others
- One door unlocked other locked
	- When one door is open the other cannot be unlocked
- Manage control and access through a particular area

### 🤺 Fencing

- Perimeters
	- Obvious 
	- Transparent or opaque
	- Robust and strong
	- Razor wire to prevent climbing

### 📸 Video Surveillance

- CCTV
	- Replaces physical guards
	- Features are important
		- Motion detection
		- Object detection
		- Thermal
	- Often in numbers
		- Networked together
		- Record together

### 📛 Guards/Access Badges

- Guards
	- Physical Protection
	- Validates employee identity
	- Two person integrity
		- Minimize attack risk
		- Separation of power
- Access Badge
	- On lanyard 
	- Worn at all times
	- Provides personal information that can be logged and verified

### 🔦 Lighting

- More light means more security
	- Attackers avoid lights
	- Easier to see
- Designs
	- Consider overall light levels
	- Angles are important
	- Avoid shadows and glare

### 📹 Sensors

- Infrared
	- Detects radiation in both light and dark
	- Common in motion detectors
- Pressure Sensors
	- Windows and floors
- Microwave
	- Detects movement in large areas
- Ultrasonic
	- Sends signals and receives sound waves
	- Detect motion and collision


# 👿 Deception and Disruption

### 🍯 Honeypots

- Attracts attackers and traps them
- Creates a virtual world that attracts automated process and attackers to explore it
- Battle between real and fake

### 🍯🍯 Honeynets

- Larger infrastructures of honeypots
- Many different devices 
- More believable 

### 📁 Honeyfiles

- Create files with fake important information
- Make it bright and shiny
- Normal production network should not access
- Put alerts on if the file is accessed

### 💰 Honeytokens

- Traceable data added to honeynet
- Not useful data
- Provides tracking when used 
- See who is using the data

