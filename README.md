# BugBusterVM
"BugBusterVM is a custom-built vulnerable machine created for educational purposes in cybersecurity. It allows users to practice identifying and exploiting SQL Injection vulnerabilities and uncover hidden flags, enhancing their penetration testing and ethical hacking skills."
# BugBusterVM

*A vulnerable machine for cybersecurity training and educational purposes.*

---

## Overview
BugBusterVM is a custom-built vulnerable machine designed to simulate SQL Injection vulnerabilities and hidden flag challenges. It provides a hands-on learning experience for cybersecurity enthusiasts and ethical hackers to practice penetration testing and vulnerability exploitation in a controlled environment.

---

## Features
- **SQL Injection Vulnerabilities**: Learn how to exploit insecure database queries.
- **Hidden Flags**: Three hidden flags are placed across the system to challenge users.
- **Educational Focus**: Perfect for beginners to gain practical skills in ethical hacking and vulnerability assessment.

---

## System Requirements
- **Hardware**: At least 2 GB RAM and 20 GB disk space.
- **Software**:
  - VirtualBox or any OVA-compatible virtualization tool.
  - Ubuntu Server (pre-configured in the OVA).
  - Tools for exploitation, such as SQLmap.

---

## Setup Instructions

### 1. Download the OVA File
Click the green **Code** button in this repository and select **Download ZIP** to get the OVA file.

### 2. Import the OVA File
1. Open VirtualBox.
2. Go to **File** > **Import Appliance**.
3. Select the downloaded OVA file and follow the import wizard.

### 3. Start the Machine
1. Boot up the virtual machine.
2. Access the web application hosted on the machine via the provided IP address.
3. Begin exploring and exploiting the vulnerabilities.

---

## Exploitation Guide

### SQL Injection Vulnerability
- The login page is vulnerable to SQL Injection.
- Use tools like SQLmap or manual techniques to bypass authentication and retrieve sensitive data.

### Hidden Flags
- **Flag 1**: Located in `/var/www/html/flag1.txt`.
- **Flag 2**: Located in `/root/flag2.txt`.
- **Flag 3**: Found in the database using SQL Injection.

---

## Setup Details

### Commands Used to Configure the Machine:
1. Install necessary packages:
   ```bash
   sudo apt install python3 python3-pip sqlite3
   ```
2. Create directories:
   ```bash
   sudo mkdir -p /var/www/html
   sudo mkdir -p /root
   ```
3. Set permissions:
   ```bash
   sudo chown -R www-data:www-data /var/www/html
   sudo chmod -R 755 /var/www/html
   ```
4. Run the vulnerable machine script:
   ```bash
   sudo python3 /home/anonymous/vulnerable_machine/vulnerable_machine.py
   ```

---

## Tools Used
- **SQLmap**: Automates SQL Injection exploitation.
- **Burp Suite**: For intercepting and manipulating requests.
- **Nmap**: For initial reconnaissance.

---

## Disclaimer
BugBusterVM is intended solely for educational purposes. Use it responsibly and only in authorized environments.

---

## Contributing
If you’d like to contribute or report issues, feel free to open a GitHub issue or submit a pull request.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
