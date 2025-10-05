## Team Watchmakers

# Use-cases

### Goal
The product aims to improve access to open source software within the Philippines by providing a low-latency, distributed mirror for Debian, Ubuntu, Fedora and other Open Source software repositories

### Users
- Students
- Teachers
- Government
- Private companies

### Discovery
This product aims to integrate with DOST systems

### Entry
This product comes into play when a user attempts to
download and/or update open source software found within
their computer systems

### Step 1
Develop Mirror Solution

### Step 2
Engage with DOST VII and other possible partners

### Step 3
Configure & Deploy system

### Step 4
Quantify improvements via 

# Words
mirroring open-source education accessibility outreach enablement empowerment community elevation

# Tentative Tech Stack
- Pulp to host the software (Debian/Ubuntu, Python, NPM, Container Registry, etc)
- NGINX can also do the file hosting thingymajig
- Simple, headless RPi OS Image
- Cron jobs for scheduling
- Bash scripts to rsync for synchronization
