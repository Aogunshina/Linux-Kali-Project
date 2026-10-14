# System Information & Network Testing
 
**Project Date:** 22 September 2026  
**Category:** Linux Fundamentals | System Administration | Network Troubleshooting  
**Environment:** Kali Linux

## 📌 Project Overview

This project focuses on using basic Linux commands to inspect system information, identify hardware resources, navigate the file system, and test network connectivity.

The assignment provided practical experience with the Kali Linux command-line interface and introduced essential techniques for understanding a computer's operating environment and checking communication with an external host.

The project is divided into two main parts:

1. **System Information and Hardware Inspection** — identifying the current user, hostname, working directory, operating system, CPU, memory, disk space, and system uptime.
2. **Basic Network Connectivity Testing** — using the `ping` command to test connectivity to Google, examine packet loss, interpret round-trip time, and identify the IP address returned by DNS resolution.

This project represents my developing practical knowledge of Linux systems and basic networking.

## 🎯 Project Objectives

The main objectives of this assignment were to:

- Identify the currently logged-in Linux user.
- Determine the computer's hostname.
- Locate the current working directory.
- Inspect operating system and kernel information.
- Examine CPU architecture and processor details.
- Check memory usage and available RAM.
- Review disk space usage.
- Determine how long the system has been running.
- Test network connectivity to an external host.
- Interpret packet loss and round-trip time.
- Understand the purpose of the `-c 4` option in a ping command.
- Record the IP address returned for `google.com`.

## 🧰 Tools and Technologies

- **Operating System:** Kali Linux
- **Command-Line Interface:** Linux terminal
- **System Inspection Commands:** `whoami`, `hostname`, `pwd`, `uname`, `lscpu`, `free`, `df`, `uptime`
- **Network Testing Command:** `ping`
- **Network Target:** `google.com`

## 🖥️ Part 1: System Information and Hardware Inspection

### Step 1: Identifying the User and Current Location

This step involved identifying the current user, the computer's hostname, and the working directory.

#### 1. `whoami`

**Purpose:** Displays the username of the currently logged-in user.

```bash
whoami
```

**Recorded result:**

```text
kali
```

**What I learned:** This command provides a quick way to confirm which user account is active in the terminal session.

#### 2. `hostname`

**Purpose:** Displays the name assigned to the computer.

```bash
hostname
```

**Recorded result:**

```text
kali
```

**What I learned:** A hostname helps identify a computer within a system or network environment.

#### 3. `pwd`

**Purpose:** Prints the current working directory.

```bash
pwd
```

**Recorded result:**

```text
/home/kali
```

**What I learned:** Knowing the current working directory helps with file navigation and executing commands in the correct location.

### Step 2: Operating System and Hardware Information

This step involved inspecting operating system details, processor information, memory usage, disk space, and system uptime.

#### 1. `uname -a`

**Purpose:** Displays operating system and kernel information, including system and architecture details.

```bash
uname -a
```

**Recorded kernel version:**

```text
7.1.5-amd64
```

**What I learned:** System information commands help identify the environment in which applications and services are running.

#### 2. `lscpu`

**Purpose:** Displays CPU information, including architecture, processor details, CPU modes, and available processor or thread information.

```bash
lscpu
```

**What I learned:** CPU information can help establish the hardware characteristics of a system and provide useful context when investigating performance.

#### 3. `free -h`

**Purpose:** Displays memory usage in a human-readable format.

```bash
free -h
```

**Recorded total RAM:**

```text
2.0 GiB
```

**What I learned:** Memory information helps users understand the amount of RAM available to the operating system and how memory resources are being used.

#### 4. `df -h`

**Purpose:** Displays disk space usage for mounted file systems in a human-readable format.

```bash
df -h
```

**Recorded available space on the main partition:**

```text
59 GiB
```

**What I learned:** Monitoring disk capacity is important for identifying storage constraints and ensuring that sufficient space is available for system operations.

#### 5. `uptime`

**Purpose:** Displays how long the system has been running.

```bash
uptime
```

**What I learned:** Uptime information can help establish whether a computer has been running continuously or has recently restarted. The assignment did not record a specific uptime value.

## 🌐 Part 2: Basic Network Connectivity Testing

### Step 1: Testing Connectivity to Google

The assignment used a ping test to examine network connectivity to an external host.

The `ping` command sends ICMP echo requests and reports responses where available.

Example command:

```bash
ping -c 4 google.com
```

The `-c 4` option instructs the command to send four echo-request packets and then stop.

### Recorded Test Results

| Test Metric | Recorded Result |
|---|---|
| Target host | `google.com` |
| Average round-trip time | Approximately `175.227 ms` |
| Packet loss | `0%` |
| Packets requested | 4, as explained in the assignment |

**Interpretation:**

- **Round-trip time:** The recorded average was approximately 175.227 milliseconds. This represents the time taken for a request to travel to the destination and for a response to return.
- **Packet loss:** The assignment recorded 0% packet loss, meaning no packet loss was observed during that test.
- **Connectivity:** The recorded results are consistent with successful connectivity to the destination during the test.

These observations apply to the test environment and time at which the assignment was completed. Network latency and packet loss can vary across different networks and testing sessions.

### Step 2: Understanding the `-c 4` Option

The assignment asked what the `-c 4` option means.

```bash
ping -c 4 google.com
```

Explanation:

- `ping` initiates a network connectivity test.
- `-c` specifies the number of packets to send.
- `4` specifies the number of echo requests.

Therefore, `-c 4` means **send four echo-request packets and stop**, rather than continuing to send requests indefinitely.

### Identifying the IP Address

The assignment recorded the following IP address for `google.com`:

```text
172.217.76.100
```

This is the address returned during the assignment. DNS responses may differ depending on the location, network, and time of the query.

## 📊 Summary of Findings

| Category | Command or Test | Recorded Finding |
|---|---|---|
| Logged-in user | `whoami` | `kali` |
| Hostname | `hostname` | `kali` |
| Working directory | `pwd` | `/home/kali` |
| Kernel version | `uname -a` | `7.1.5-amd64` |
| Total RAM | `free -h` | `2.0 GiB` |
| Available disk space | `df -h` | `59 GiB` on the main partition |
| System uptime | `uptime` | Command practised; specific value not recorded |
| Average round-trip time | `ping` | Approximately `175.227 ms` |
| Packet loss | `ping` | `0%` |
| Resolved IP address | `google.com` | `172.217.76.100` |

## 🧠 Key Learning Outcomes

Through this assignment, I developed a foundational understanding of:

- Using Linux commands to gather system information.
- Identifying user accounts and navigating the file system.
- Inspecting operating system, kernel, and CPU information.
- Reviewing memory and storage capacity.
- Understanding the purpose of system uptime monitoring.
- Performing basic network connectivity tests.
- Interpreting latency and packet loss.
- Understanding how a hostname can resolve to an IP address.
- Recording technical results in a structured format.

These skills provide a foundation for further learning in Linux administration, IT support, and network troubleshooting.

## 🔍 Practical Applications

The concepts demonstrated in this project are relevant to several IT support activities:

- **System diagnostics:** Checking basic operating system and hardware information.
- **Resource monitoring:** Reviewing RAM and disk space when investigating performance or storage issues.
- **Connectivity troubleshooting:** Using ping to investigate whether a destination responds to network requests.
- **Network diagnostics:** Examining latency and packet loss as part of an initial connectivity investigation.
- **Technical documentation:** Recording commands, observations, and results for future reference.

A successful ping test alone does not establish that every network service is working correctly, but it is a useful first diagnostic step.

## 🚀 Future Improvements

I plan to build on this assignment by:

- Repeating system checks and comparing outputs across different Linux environments.
- Learning additional Linux commands for process management, permissions, and networking.
- Exploring `ip addr` and `ip route` to inspect network interfaces and routing information.
- Practising DNS lookup commands such as `nslookup` or `dig`.
- Testing connectivity to multiple approved destinations.
- Documenting troubleshooting scenarios, observations, and resolutions.
- Expanding my Cisco Packet Tracer practice with additional network configurations.
- Exploring how system monitoring and network diagnostics support IT operations and information security.

## 📁 Suggested Repository Structure

```text
system-information-network-testing/
├── README.md
├── commands/
│   └── linux-commands.md
├── results/
│   └── test-results.md
└── screenshots/
    └── terminal-results.png
```

This is a suggested structure for organising the project. The folders and files can be added as supporting documentation and screenshots become available.

## 👨‍💻 About Me

I'm Adebayo Oyeniyi Ogunshina, a professional with over 10 years of experience across banking, healthcare, logistics, compliance, and operational management.

I'm developing my technical skills in Linux, networking, and IT support while drawing on my existing strengths in problem-solving, documentation, risk awareness, and customer service.

I'm particularly interested in opportunities where technical troubleshooting, reliable service delivery, governance, and continuous improvement come together.

## 📫 Contact

- **Location:** Kettering, Northamptonshire, United Kingdom
- **GitHub:** Explore my repositories to follow my learning journey.

---

**Thank you for visiting this project!**

This assignment is part of my ongoing development in Linux fundamentals, system information gathering, and basic network troubleshooting.
