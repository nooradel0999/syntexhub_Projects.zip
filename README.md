# syntexhub_Projects.zip
# Port Scanner (Project 1)

Multi-threaded TCP port scanner written in pure Python.

## Features
- Scan a single port, a comma-separated list, or a full range (`1-1024`)
- Multi-threaded scanning with a bounded thread pool
- Reports OPEN / CLOSED / TIMEOUT per port with exception handling
- Common service-name mapping (22=SSH, 80=HTTP, 443=HTTPS ...)
- Results logged to `scan_results.log`

## Usage
    python port_scanner.py example.com -p 20-100
    python port_scanner.py 192.168.1.1 -p 22,80,443 -t 2

> Only scan systems you own or are explicitly authorized to test.




# Password Manager (Project 2)

Local, encrypted password manager using AES-256-GCM.

## Features
- Master password protected (PBKDF2-HMAC-SHA256, 200,000 iterations)
- Encrypted JSON storage on disk (`vault.enc`)
- Operations: add, retrieve, delete, search, list
- AES-GCM authenticated encryption (tamper-evident)

## Install & Run
    pip install -r requirements.txt
    python password_manager.py

## Security Notes
- The master password is never stored; only its derived key is used.
- AES-GCM detects any modification of the vault file.

