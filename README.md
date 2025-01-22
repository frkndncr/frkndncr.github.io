
# Web Analysis Tool

## Overview
The Web Analysis Tool is a comprehensive Python-based solution designed to analyze various aspects of a domain. It collects WHOIS information, DNS records, subdomains, SEO and analytics tags, web technologies, and performs advanced security analysis.

---

## Features
- **Domain WHOIS Information**: Fetch registrar details, creation date, expiration date, and DNSSEC status.
- **DNS Records**: Retrieve A, AAAA, MX, TXT, and NS records with response time.
- **Subdomain Discovery**: Use `Subfinder` to uncover subdomains.
- **SEO and Analytics Tags**: Analyze meta tags, Open Graph, Twitter tags, analytics tools, and more.
- **Web Technologies**: Detect backend/frontend technologies, CDN, caching, and compression.
- **Security Analysis**: Perform advanced checks on WAF, SSL certificates, CORS policies, and security headers.

---

## Installation

### Prerequisites
- Linux/Unix system (tested on Ubuntu/Kali Linux)
- Python 3.8 or higher
- Go programming language
- Subfinder tool

### Installation Steps
1. Clone this repository:
    ```bash
    git clone https://github.com/your-repo/web-analysis-tool.git
    cd web-analysis-tool
    ```

2. Run the setup script:
    ```bash
    ./setup.sh
    ```

---

## Usage

1. Run the tool:
    ```bash
    python3 main.py
    ```

2. Enter a domain name when prompted:
    ```
    Please enter a domain name (e.g., example.com):
    ```

3. View the results in the terminal and as a JSON file saved in the `logs` directory.

---

## Outputs
All analysis results are saved in the `logs` folder. Each domain has its directory containing:
- `results.json`: Consolidated analysis output.
- `robots.txt`: Content of robots.txt if found.
- `sitemap.xml`: Content of sitemap.xml if found.
- Subdomain list file (`<domain>-sub.txt`).

---

## Modules and Details

### Domain Info Module
- Fetch WHOIS information using `WhoisXML API`.
- Retrieve registrar, creation date, expiration date, DNSSEC status, privacy protection, and physical location.

### DNS Records Module
- Fetch A, AAAA, MX, TXT, and NS records.
- Measure DNS response time.

### Subdomain Finder Module
- Use Subfinder to discover subdomains.
- Save results in the domain-specific folder.

### SEO and Analytics Tags Module
- Analyze meta tags, Open Graph, Twitter tags, and verification tags.
- Detect analytics tools like Google Analytics, Tag Manager, and Facebook Pixel.
- Check for `robots.txt` and `sitemap.xml`.

### Web Technologies Module
- Detect backend technologies like PHP, WordPress, Django, and Node.js.
- Identify frontend frameworks such as React, Angular, and Bootstrap.
- Detect CDN providers, compression methods, and caching mechanisms.

### Security Analysis Module
- Detect Web Application Firewalls (WAF).
- Analyze security headers like CSP, HSTS, X-Frame-Options.
- Retrieve SSL certificate details.
- Identify CORS policy.

---

## Contribution
Feel free to fork the repository, submit pull requests, or report issues. Your contributions are welcome!

---

## License
This project is licensed under the MIT License.
