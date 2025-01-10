# RecScan - DNS Record Checker

## Overview
RecScan is a Python-based tool for analyzing DNS records of domains. It checks various DNS records like SPF, DKIM, DMARC, A, MX, and more. The results are presented in a user-friendly format either in the terminal or saved to an Excel file for further analysis.

---

## Features
- **DNS Record Analysis**: Supports multiple DNS records including TXT, MX, NS, A, CNAME, AAAA, SPF, DKIM, DMARC, SOA, PTR, SRV, and CAA.
- **Single and Bulk Domain Support**: Analyze a single domain or a list of domains from a file.
- **Excel Export**: Save DNS analysis results to an Excel file for better visualization and documentation.
- **Color-Coded Output**: Displays results in a color-coded format for better readability.
- **Beautiful ASCII Art**: Enjoy colorful ASCII art during execution.

---

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-repository>/RecScan.git
   cd RecScan
   ```

2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage
### Syntax
```bash
python recscan.py [domain] [-l list_of_domains.txt] [-o output.xlsx]
```

### Parameters
- **`domain`**: The domain name to analyze (for single domain analysis).
- **`-l` or `--list`**: Path to a text file containing a list of domains (one per line).
- **`-o` or `--output`**: Path to save the results in an Excel file.

### Examples
#### Analyze a Single Domain
```bash
python recscan.py example.com
```

#### Analyze Multiple Domains from a File
```bash
python recscan.py -l domains.txt
```

#### Save Results to an Excel File
```bash
python recscan.py -l domains.txt -o results.xlsx
```

---

## Output Format
### Terminal
Displays DNS records for each domain with color-coded results:
- **Green**: Record Found
- **Red**: Record Not Found

### Excel
Generates an Excel file with the following columns:
- **Domain**
- **Records**
- **Output**
- **Found**

---

## Requirements
- Python 3.7+
- Dependencies (install via `requirements.txt`):
  - `dns.resolver`
  - `argparse`
  - `termcolor`
  - `itertools`
  - `openpyxl`

---

## Credits
Developed by **Garv Thakkar**.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

---
