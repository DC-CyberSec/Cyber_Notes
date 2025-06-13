# 📊  Change Management 

- Scope of change in a corporate environment is big
	- Requires formal process for many tasks (upgrade software, patching, hardware upgrades, etc)
- Change is 
	- Constant
	- Very common
	- Risky
	- Overlooked
	- Uncomfortable
- Clear change policies help
	- Frequency, duration, installation, rollback
- Change can be very difficult
### 🏗️  Change Approval Process

- Good idea to have a formal process for managing change
	- Avoids downtime, confusion, and errors
- Typical process
	1. Fill out formal change process form
	2. Determine in this form why the change is needed
	3. Determine the scope of the change
	4. Schedule dates for the change
	5. Analyze systems affected and impacted
	6. Analyze risk associated
	7. Get approval from change control board
	8. End user assessment after the change is complete
### 👑  Ownership

- Change usually begins with the owner 
	- Own the process
	- Don't typically make the change
- Owner manages the process
	- Is informed of progress as change happens
	- Tests the change after completion
- Example
	- Shipping and receiving own address label printers
	- IT actually upgrades them

### 💲 Stakeholders

- Who is impacted by the change
	- Will have input
- Not as obvious as you think
	- Never know who could be affected

### 💥 Impact Analysis

- Determine risk value
	- High, Medium, Low
	- 1-10
- This risks can be minor or far reaching
	- Fix doesn't work
	- Fixing breaks something else
	- Data corruption
	- System failure
- Risk of not making the change
	- Downtime
	- Vulnerabilities
	- Unavailability

### 📝 Test Results

- Testing helps mitigate risk before production
- Sandbox
	- Perform as many tests as you want
	- No affect on production
	- Technological safe space
- Back-out Procedure
	- If something breaks you better know how to roll it back
	- Always prepare for the worst, hope for the best
	- Some changes can be incredibly difficult to reverse
	- Always have a backup

### 👷 Maintenance Window

- When is the change going to happen?
	- Finding time is hard
	- Not during workday?
		- Change would cause downtime
	- Usually happens during off hours
		- Difficult for 24 hour environments
	- Time of year matters for some
		- Retail freezes changes during holidays

### 📜 Standard Operating Procedures

- Change management is critical and should be in SOPs
- Process should be well documented and available to everyone in the org
- Should be updated as time goes on


# 👨‍💻 Technical Change Management

- Change will have to be executed
- No such thing as a simple upgrade
	- Many moving parts
	- Separate events
- Change management is often concerned with what needs to change 
- Technical team is tasked with how to change it

### ✅ Allow list/Deny list

- Used to allow or disallow certain applications
	- Applications can have vulnerabilities, malware, etc
- Security Policy controls app execution
- Allow List
	- Nothing runs unless its on the list
	- Very rigid and restrictive
- Deny List 
	- Nothing on the list can run 
	- Antivirus, Anti-Malware
	- Very flexible

### ⛓️ Restricted Activities

- When change happens a restrictive scope is established
	- Defines exactly what components are covered
- Change approval windows aren't permission to change everything
- Due to unforeseen outcomes change scope can be expanded during the window
	- Scope must be expanded to reach the goal
- Good documentation should include what steps to take if this occurs

### 👎 Downtime

- Services will typically become unavailable
	- May not always be the case
	- Usually done during non production hours
- If possible its better to prevent downtime
	- Secondary systems to switch to
- Minimize any downtime events
	- Automate the process
	- If issues occur switch back to secondary system
	- Part of back-out plan
- Alert the organization
	- Calendar or emails

### ♻️ Restarts

- Common procedure
- Rebooting
	- Implement new configs
	- Test if the system can recover form outages
- Restarting services
	- Task Manager
	- Relatively quick
- Restarting applications
	- Close out/Log out
	- Launch new instance

### 🗝️ Legacy Applications

- Some applications are just old 
	- Still required
- No longer supported
- Often not touched because no one knows what will happen
	- Documentation helps with the fear of the unknown
- May have to create specific process for these systems

### 👥 Dependencies

- To complete A you have to complete B
	- Service wont start without other active ones
	- Application requires specific library version
- Can complicate things
	- Can evolve into multiple components that need change
- Can occur across systems
	- Firewall must be upgraded before the firewall software

### 📄 Documentation

- Change can be a challenge
- Updating documentation should be a part of the change process
- Don't let documentation go out of date
- Update diagrams, charts, process, procedures, etc
- Version control 
	- Track changes to file or configuration data over time
	- Allows for reverting back
	- Used for router configs, OS patches, application registry entries, etc
	- Some devices have it built in 
	- Some need additional software