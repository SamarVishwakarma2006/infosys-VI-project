WebScanPro: Automated Web Application Security Scanner
An automated penetration testing tool built to detect OWASP Top 10 vulnerabilities in Single Page Applications (SPAs).

📖 Overview
WebScanPro is a modular security testing framework developed during an 8-week internship. Unlike traditional static scanners, WebScanPro utilizes Selenium WebDriver to interact with modern, dynamic web applications.

It autonomously navigates the target application, bypasses UI obstructions, performs complex attacks (SQLi, XSS, IDOR), and generates a professional HTML security report.

🎯 Key Features
Dynamic Scanning: Handles client-side rendering (Angular/React) using browser automation.
SQL Injection Engine: Automates authentication bypass attacks on login forms.
XSS Detector: Identifies Reflected Cross-Site Scripting using direct URL injection.
IDOR Tester: Detects Horizontal Privilege Escalation by manipulating API object references.
Auth Analysis: Performs brute-force testing and analyzes session cookies for security flags.
Auto-Reporting: Generates a "Client-Ready" HTML & JSON Report with severity ratings and mitigation advice.
🛠️ Technology Stack
Language: Python 3
Automation: Selenium WebDriver (Chrome)
Target Environment: Docker (OWASP Juice Shop v14.x)
Reporting: Custom HTML/CSS Engine + JSON
🚀 Installation & Setup
Prerequisites
Python 3.x installed.
Docker Desktop installed and running.
Google Chrome browser installed.
Step 1: Clone the Repository
git clone [https://github.com/your-username/WebScanPro.git](https://github.com/your-username/WebScanPro.git)
cd WebScanPro
Step 2: Install Dependencies
pip install -r requirements.txt
(Note: If requirements.txt is missing, run: pip install selenium webdriver-manager)

Step 3: Launch the Target (Juice Shop)
Run the following Docker command to start the isolated testing lab:

docker run --rm -p 3000:3000 bkimminich/juice-shop
Wait until the terminal says "Server listening on port 3000".

💻 Usage
Run the main scanner script:

python main.py
(Note: Replace main.py with your script name, e.g., webscan_week7_final.py)

automated Workflow:
Initialization: Launches Chrome and clears "Welcome" banners/popups via JavaScript.
Crawl: Maps application endpoints.
Attack: Executes SQLi, XSS, Auth, and IDOR modules sequentially.
Report: Saves vulnerability_report.json and opens final_security_report.html.
📸 Screenshots & Proof of Concept
1. SQL Injection (Authentication Bypass)
Bypassed admin login using payload ' OR 1=1 --

2. Reflected XSS
Triggered browser alert via search parameter injection.

3. IDOR (Data Leak)
Accessed unauthorized shopping basket JSON data.

4. Final HTML Report
Generated security audit report.

🗺️ Project Roadmap (8-Week Timeline)
Week 1: Environment Setup (Docker & Git).
Week 2: Scanning Module (Transitioned from BeautifulSoup to Selenium).
Week 3: SQL Injection Module (Login Bypass).
Week 4: Cross-Site Scripting (XSS) Module.
Week 5: Authentication & Session Management Testing.
Week 6: Access Control & IDOR Testing.
Week 7: Reporting Engine (HTML/JSON).
Week 8: Final Documentation & Presentation.
⚠️ Disclaimer
This tool is developed for educational and testing purposes only. It is designed to be used on locally hosted, intentionally vulnerable applications (like OWASP Juice Shop) or systems where you have explicit permission to test. Do not use this tool on unauthorized targets.

📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

