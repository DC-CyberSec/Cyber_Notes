# ☁️ Cloud Infrastructures

### ✖️ Cloud Responsibilty Matrix

- IaaS, Paas, SaaS, etc.
	- Who is responsible for security
- Security should be well documented
	- Most cloud providers provide a matrix of responsibilities
	- Everyone knows up front
- These can vary
	- Different providers
	- Contractual agreements

### ✌️ Hybrid Situations

- Hybrid cloud
	- More than one public or private cloud
	- Adds complexity
- Network protection mismatches
	- Authentication across platforms
	- Firewall configurations
	- Server settings
- Different security monitoring
	- Logs are diverse and cloud specific
- Data leakage
	- Data is shared across the public internet

### 3️⃣ Third Party Vendors

- You, the cloud provider, and third parties
	- Infrastructure technologies
	- Cloud-based appliances
- On-going vendor risk assessments
	- Part of an overall vendor risk management policy
- Include third party impact for incident response
	- Everyone has a part
- Constant monitoring
	- Watch for unusual changes

### 💻 Infrastructure as Code

- Describe an infrastructure
	- Define servers, network, applications as code
- Modify the infrastructure and create versions
	- Same way you version application code
- Use the code to build other application instances
	- Build it the same way every time based on the code
- An important concept for cloud computing
	- Build a perfect version every time

### 📵 Serverless Architecture

- Function as a Service (FaaS)
	- Applications are separated into individual, autonomous functions
	- Removes the OS from the equation
- Developer still creates the server-side logic
	- Runs in a stateless compute container
- May be event triggered and ephemeral
	- May only run for one event
- Managed by a third-party
	- All OS security concerns are at the third-party

### 🦠 Micro-services and APIs

- Monolithic applications 
	- One big application does everything
- Application contains all decision making processes
	- User interface
	- Business logic
	- Data input and output
- Code challenges
	- Large code-base
	- Change control challenges
- APIs
	- Application Programming Interfaces
- API is the "glue" for micro-services
	- Work together to act as the application
- Scalable
	- Scale just the micro-services you need
- Resilient
	- Outages are contained
- Security and compliance
	- Containment is built-in


# 🌐 Network Infrastructures

### 🕳️ Physical Isolation

- Devices are physically separate
	- Air gap between Switch A and Switch B
- Must be connected to provide communication
	- Direct connect, or another switch or router
- Web Servers in one rack
	- Database servers on another
- Customer A on one switch, customer B on another
	- No opportunity for mixing data
- Physical Segmentation

### 👨‍💻 Logical Segmentation

- VLANs (Virtual Local Area Networks)
	- Separated logically instead of physically 
	- Cannot communicate between VLANs without a Layer 3 device / router

### 🍦 Software Defined Networking (SDN)

- Networking Devices have different functional planes of operation
	- Data, control, and management
- Split the functions into separate logical units
	- Extend functionality and management of a single device
	- Perfect for the cloud
- See Section 1.2


# 🔌 Other Infrastructure Concepts

### 🏢 On-premises

- Customize your security posture
	- Full control over everything
- On-site IT team can manage security better
	- Local team can ensure everything is secure
	- Local team can be expensive and difficult to staff
- Local team maintains up-time and availability
	- System checks can occur at any time
	- No phone call for support
- Security changes can take time
	- New equipment, configurations, and additional costs

### 🌃 Centralized vs. Decentralized

- Most organizations are physically decentralized
	- Many locations, cloud providers, operating systems, etc.
- Difficult to manage and protect so many diverse systems
	- Centralize the security management 
- A centralized approach
	- Correlated alerts
	- Consolidated log file analysis
	- Comprehensive system status and maintenance/patching
- It's not perfect
	- Single point of failure, potential performance loss

### 🖥️ Virtualization

- Virtualization
	- Run many different OSs on the same hardware
- Each application instance has its own OS
	- Adds overhead and complexity
	- Can be expensive

### 🏗️ Application Containerization

- Container 
	- Contains everything you need to run an application
	- Code and dependencies
	- A standardized unit of software
- An isolated process in a sandbox
	- Self-contained
	- Apps can't interact with each other
- Container image 
	- A standard for portability
	- Lightweight, uses the host kernel
	- Secure separation between applications

### 💡 Internet of Things (IoT)

- Sensors
	- Heating and cooling, lights
- Smart devices
	- Home automation
	- Video doorbells
- Wearable tech
	- Watches, health monitors
- Facility automation
	- Temperature, air quality, lighting
- Weak defaults
	- IoT manufacturers are not security professionals

### 🎛️ SCADA / ICS

- Supervisory Control and Data Acquisition System (SCADA)
	- Large-scale, multi-site Industrial Control Systems (ICS)
- PC manages equipment
	- Power generation, refining, manufacturing equipment
	- Facilities, industrial, energy, logistics
- Distributed control systems
	- Real-time information
	- System control
- Requires extensive segmentation
	- No access from the outside

### 🚗 Real-Time Operating Systems (RTOS)

- An OS with a deterministic processing schedule
	- No time to wait for other processes
	- Industrial equipment, automobiles, military environments
- Extremely sensitive to any security concerns
	- Non-trivial systems
	- Need to always be available
	- Difficult to know security posture

### ⌚ Embedded Systems

- Hardware or software designed for a specific function
	- Or to operate as a larger system
- Is built with one sole purpose
	- Can be optimized for size and/or cost
- Common examples
	- Traffic lights
	- Digital watches
	- Medical Imaging systems

### 🔼 High Availability

- Redundancy doesn't always mean availability
	- May need to be powered on manually
- Always on, always available 
- May include many different components working together
	- Active/Active can provide scalability advantages
- Higher availability almost always means higher costs
	- There's always another contingency you could add
	- Upgraded power, high quality server components, etc.


# 💭 Infrastructure Considerations

### ⌨️ Availability

- System up-time
	- Access data, complete transactions
	- Foundation of IT security
- Balancing act with Security
- We spend a lot of time and money on it
	- Monitoring and redundant systems
- Important metric
	- Total available time

### 🔧 Resilience

- Eventually something will happen
	- Can you maintain availability
	- Can you recover
	- How fast
- Based on many different variables
	- Root cause
	- Replace hardware
	- Software patches
	- Redundant systems
- Commonly referenced as MTTR
	- Mean time to repair

### 💳 Cost

- How much money is required?
	- Everything ultimately comes down to costs
- Initial installation
	- Different across platforms
- Ongoing maintenance
	- Annual ongoing costs
- Replacement or repair costs
	- Might need more than one
- Tax implications
	- Operating or capital expense

### ⏱️ Responsiveness

- Request information
	- Get a response
	- How quick?
- Especially important for interactive applications
	- Humans are sensitive to delays
- Speed is an important metric
	- All parts of the application contribute
	- There's always a weakest link

### 🗄️ Scalability

- How quickly and easily can we increase or decrease capacity?
	- Might happen many time a day
	- Elasticity
- There's a resource challenge
	- What preventing scalability?
- Needs to include security monitoring
	- Increases and decreases as the system scales

### 🚀 Ease of Deployment

- An application has many moving parts
	- Web server, database, caching server, firewall, etc.
- This might be an involved process
	- Hardware resources, cloud budgets, change control
- This might be simple
	- Orchestration / automation
- Important to consider during the product engineering phase
	- One missed detail can cause deployment issues

### 🔓 Risk Transference

- Many method to minimize risk
	- Transfer risk to third-party
- Cyber-security insurance
	- Attacks and downtime can be covered
	- Popular with the rise in ransomware
- Recover internal losses
	- Outages and business downtime
- Protect against legal issues from customers
	- Limit costs associated with legal proceedings

### 🔙 Ease of Recovery

- Something will go wrong
	- Time is money
	- How easy is it to recover
- Malware infection
	- Reload OS from original media - 1 hour
	- Reload from corporate image - 10 minutes
- Another important design criteria
	- May be critical for the final product

### 📦 Patch Availability

- Software isn't usually static
	- bug fixes, security updates, etc.
- This is often the first task after installation
	- Make sure you're running the latest version
- Most companies have regular updates
	- Microsoft's monthly patch schedule
- Some companies rarely patch
	- Significant concern

### 📭 Inability to Patch

- What if patching isn't an option?
	- Happens more than you think
- Embedded systems
	- HVAC controls
	- Time clocks
- Not designed for end-user updates
	- Shortsighted these days
- May need additional security controls
	- Firewall for the time-clock

### 🔌 Power

- A foundational element
	- This can require extensive engineering
- Overall power requirements
	- Data-center vs. office buildings
- Primary power 
	- One or more providers
- Backup services
	- UPS (Uninterruptible Power Supply)
	- Generators

### 💻 Compute

- An application's heavy lifting
	- More than just a single CPU
- Compute engine
	- More options available in the cloud
- May be limited to a single processor
	- Easier to develop
- Use multiple CPUs across multiple clouds
	- Additional complexity
	- Enhanced scalability