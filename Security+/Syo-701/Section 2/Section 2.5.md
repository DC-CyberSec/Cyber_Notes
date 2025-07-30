# ➗ Segmentation and Access Control

### 🔣 Segmentation

- Physical, logical, virtual
	- Devices, VLANs, virtual networks
- Performance
	- High bandwidth
- Security
	- Users should not talk directly to database serves
	- Only cores apps are SQL and SSH
- Compliance
	- Mandated segmentation (PCI compliance)
	- Makes change control easier

### 📋 Access Control Lists (ACL)

- Allow or disallow traffic
	- Grouping categories
	- Source IP, Destination IP, port numbers, time of day, application, etc.
- Restrict access to network devices
	- Limit by IP address or other identifier
	- Prevent regular user / non-admin access
- Be careful when configuring
	- Could lock out
- Lists the permissions
	- Bob can read files
	- Fred can access the network
	- Jane can access specific network using only specific ports
- Many operating systems use ACLs to provide access to files

### ☑️ Application Allow List / Deny List

- Any application is a risk
	- Vulnerabilities, Trojans, malware
- Security policy controls app execution
- Allow list 
	- Nothing runs unless its on the list
	- Very restrictive
- Deny list
	- Nothing on the bad list runs
	- Anti-virus, anti-malware
- Decisions are made in the OS
	- Often built-in to operation system management
- Application hash
	- Only allows apps with unique identifier
- Certificate
	- Allow digitally signed apps from certain publishers
- Path 
	- Only runs apps in these folders
- Network Zone
	- The apps can only run from these network zones


# 🛡️ Mitigation Techniques

### 📦 Patching

- Important
	- System Stability, security fixes
- Monthly updates
	- Incremental and important
- Third-party updates
	- Application developers, device drivers
- Auto-update
	- Not always the best option
- Emergency out of band updates

### 🔒 Encryption

- Prevent access to application data files
	- File system encryption
- File level encryption
	- Windows EFS
- Full disk encryption (FDE)
	- Encrypt everything on the drive
	- BitLocker, FileVault, etc.
- Application data encryption
	- Managed by the app
	- Stored data is protected
- Encrypt all network communication
	- VPNs
	- Application encryption

### 🖥️ Monitoring

- Aggregate information from devices
	- Built-in sensors
	- Integrated into servers, switches, routers, firewalls, etc.
- Sensors
	- Intrusion prevention systems, logs
- Collectors
	- Proprietary consoles (IPS, Firewalls), SIEM consoles, syslog servers
	- Many SIEMs include a correlation engine to compare diverse sensor data

### 🔹 Least Privilege

- Rights and permissions should be set to bare minimum
	- You only get exactly what you need
- All users accounts should be limited
	- Applications should run with minimal privileges
- Don't allow users to run with admin privileges
	- Limits the scope of malicious behavior

### 🚔 Configuration Enforcement

- Perform a posture assessment 
	- Each time a device connects
- Extensive check
	- OS patch version
	- EDR (Endpoint Detection and Response) version
	- Status of firewalls and EDRs
	- Certificate status
- Systems out of compliance are quarantined
	- Private VLAN with limited access
	- Recheck after making corrections

### 🗑️ Decommissioning

- Should be a formal policy
	- Don't throw your data in the trash
	- Someone will find it
- Mostly associated with storage devices
	- HDD, SSD, USB
- Many options for physical devices
	- Recycle the device for use in another device
	- Destroy the device


# 🔨 Hardening Techniques

- Many and varied
	- Windows, Linux, iOS, Android, et al.
- Updates
	- OS updates / service packs, security patches
- User accounts
	- Minimum password lengths and complexity
	- Account limitations
- Network access and security
	- Limit network access
- Monitor and secure
	- Anti-virus, anti-malware

### 🔒 Encryption (see above)


### 🔚 Endpoint

- The user's access 
	- Applications and data
- Stop attackers
	- Inbound attacks
	- Outbound attacks
- Many different platforms
	- Mobile, desktop
- Protection is multi-faceted
	- Defense in depth
- EDR
	- Different method of threat protection
		- Scales to meet increasing number of threats
	- Detect a threat
		- Signatures aren't the only detection tool
		- Behavioral analysis, machine learning, process monitoring
		- Lightweight agent on the endpoint
	- Investigate the threat
		- Root cause analysis
	- Respond to the threat
		- Isolate the system, quarantine the threat, rollback to previous config
		- API driven, no user or technician intervention required

### 🧱 Host-based Firewall

- Software-based firewall
	- Personal firewall, runs on every endpoint
- Allow or disallow incoming or outgoing application traffic
	- Control by application process
	- View all data
- Identify and block unknown processes
	- Stop malware before it starts
- Managed centrally

### 💉 Intrusions

- Host-based Intrusion Prevention Systems (HIPS)
	- Recognize and block known attacks
	- Secure OS and application configs, validate incoming service requests
	- Often built into endpoint protection software
- HIPS identification
	- Signatures, heuristics, behavioral
	- Buffer overflows, registry updates, writing files to Windows folder
	- Access non-encrypted data

### 🚢 Open ports and Services

- Every open port is a possible entry
	- Close everything not required
- Control access with a firewall 
	- NGFW would be ideal 
- Unused or unknown services
	- Installed with the OS or form other applications
- Applications with broad port ranges
	- Open port 0 - 65,535
- Use Nmap or similar port scanner to verify
	- Monitoring is important

### 💬 Default Password Changes

- Every network device has a management interface
	- Critical systems, other devices
- Many applications also have management or maintenance interfaces
	- Contain sensitive data
- Change default settings
	- Password

### 💥 Removing Unnecessary Software

- All software contains bugs
	- Some bugs are security vulnerabilities
- Every application seems to have different patching process
	- Can be challenging to mange ongoing updates
- Remove all unused software
	- Reduce risk 
	- Easy fix

