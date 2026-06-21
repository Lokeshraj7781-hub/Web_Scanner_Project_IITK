# My Web Scanner Project

A lightweight, efficient Python-based web scanning tool designed to automate security audits, discover vulnerabilities, and map web applications.

##  Features

* **Port Scanning:** Fast multi-threaded scanning for open ports and services.
* **Directory Busting:** Brute-forces hidden directories and files using a custom wordlist.
* **Vulnerability Detection:** Checks for common misconfigurations (e.g., missing security headers).
* **Subdomain Enumeration:** Discovers active subdomains to map the target's attack surface.
* **Clean Output:** Generates structured terminal output and logs results to a file.

##  Installation

### Prerequisites
Ensure you have Python 3.8+ installed on your system.

### Step-by-Step Setup
1. Clone the repository:
   ```bash
   git clone https://github.com
   cd My-Web-Scanner-Project
   ```

2. (Optional) Create and activate a virtual environment:
   ```bash
   python -bin/python3 -m venv venv
   source venv/bin/activate # On Windows use: venv\Scripts\activate
   ```

3. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
   *(Note: Create a requirements.txt file listing external libraries like `requests`, `beautifulsoup4`, or `colorama` if your script uses them).*

## Usage

Run the scanner directly from your terminal by specifying a target domain or IP address:

```bash
python scanner.py --target example.com --scan all
```

### Command Line Arguments

| Argument | Description | Example |
| :--- | :--- | :--- |
| `--target` | The target URL or IP address to scan | `example.com` |
| `--port` | Specific port or range to check | `80,443` or `1-1000` |
| `--output` | Save the scan results to a specific text/JSON file | `results.txt` |

## Sample Output

```text
[+] Starting scan on target: example.com
[+] Checking open ports...
    - Port 80 (HTTP): OPEN
    - Port 443 (HTTPS): OPEN
[+] Scanning hidden directories...
    - /admin [FOUND - 403 Forbidden]
    - /robots.txt [FOUND - 200 OK]
[+] Scan complete. Results saved to results.txt.
```
