<p align="center"><img src="https://i.imgur.com/xgaojFM.png"></p>
<h4 align="center">
OSINT Tool to Find Passwords for Compromised Email Accounts
</h4>
<p align="center">
<img src="https://img.shields.io/badge/HaveIBeenPwned-v2-blue.svg?style=plastic">
<img src="https://img.shields.io/badge/Python-3-brightgreen.svg?style=plastic">
<img src="https://img.shields.io/badge/Termux-✔-red.svg?style=plastic">
<img src="https://img.shields.io/badge/NetHunter-✔-red.svg?style=plastic">
</p>

pwnedOrNot uses [**haveibeenpwned**](https://haveibeenpwned.com/API/v2) v2 api to test email accounts and tries to find the **password** in **Pastebin Dumps**.

## Features
[**haveibeenpwned**](https://haveibeenpwned.com/API/v2) offers a lot of information about the compromised email, some useful information is displayed by this script:
* Name of Breach
* Domain Name
* Date of Breach
* Fabrication status
* Verification Status
* Retirement status
* Spam Status

And with all this information **pwnedOrNot** can easily find passwords for compromised emails if the dump is accessible and it contains the password

#### Tested on
* **Kali Linux 18.2**
* **Ubuntu 18.04**
* **Kali Nethunter**
* **Termux**

## Installation
**Ubuntu / Kali Linux / Nethunter / Termux**

```bash
chmod 777 install.sh
./install.sh
```

[![asciicast](https://asciinema.org/a/200221.png)](https://asciinema.org/a/200221)

## Usage
```bash
python3 pwnedornot.py -h

usage: pwnedornot.py [-h] [-e EMAIL] [-f FILE] [-d DOMAIN] [-n] [-l]
                     [-c CHECK]

optional arguments:
  -h, --help                  show this help message and exit
  -e EMAIL, --email EMAIL     Email Address You Want to Test
  -f FILE, --file FILE        Load a File with Multiple Email Addresses
  -d DOMAIN, --domain DOMAIN  Filter Results by Domain Name
  -n, --nodumps               Only Check Breach Info and Skip Password Dumps
  -l, --list                  Get List of all pwned Domains
  -c CHECK, --check CHECK     Check if your Domain is pwned

# Examples

# Check Single Email
python3 pwnedornot.py -e <email>
#OR
python3 pwnedornot.py --email <email>

# Check Multiple Emails from File
python3 pwnedornot.py -f <file name>
#OR
python3 pwnedornot.py --file <file name>

# Filter Result for a Domain Name [Ex : adobe.com]
python3 pwnedornot.py -e <email> -d <domain name>
#OR
python3 pwnedornot.py -f <file name> --domain <domain name>

# Get only Breach Info, Skip Password Dumps
python3 pwnedornot.py -e <email> -n
#OR
python3 pwnedornot.py -f <file name> --nodumps

# Get List of all Breached Domains
python3 pwnedornot.py -l
#OR
python3 pwnedornot.py --list

# Check if a Domain is Pwned
python3 pwnedornot.py -c <domain name>
#OR
python3 pwnedornot.py --check <domain name>
```

[![asciicast](https://asciinema.org/a/200225.png)](https://asciinema.org/a/200225)

## Demo
[YouTube](https://www.youtube.com/watch?v=R_Y_QzVmERA)
