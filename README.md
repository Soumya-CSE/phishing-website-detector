# 🛡️ Phishing Website Detector

A simple **Phishing Website Detector** built using **Python** and **HTML, CSS, JavaScript**. The project analyzes website URLs and identifies potential phishing attempts using rule-based security checks. It provides a phishing risk score along with detailed explanations for every detected indicator.

The project includes:

* 🐍 **Python CLI Version** – Analyze URLs from the command line with optional webpage content analysis.
* 🌐 **Web Version** – A modern browser-based interface that performs fast client-side URL analysis without sending data to any server.

---

## ✨ Features

* URL structure analysis
* HTTPS verification
* IP address detection
* Typosquatting detection
* Suspicious keyword detection
* Suspicious TLD detection
* URL shortener detection
* Long URL detection
* Random-looking domain (entropy) detection
* Punycode (IDN homograph) detection
* Risk score with detailed explanations
* Interactive web dashboard with animated results
* Optional live webpage analysis (Python version)

---

## 🛠️ Technologies Used

### Backend (Python)

* Python 3
* argparse
* re (Regular Expressions)
* ipaddress
* urllib.parse
* requests *(optional)*
* BeautifulSoup4 *(optional)*

### Frontend

* HTML5
* CSS3
* JavaScript (ES6)
* SVG (Risk Gauge)

---

## 📂 Project Structure

```text
phishing-detector/
│
├── phishing_detector.py      # Python CLI application
├── index.html                # Web interface
├── README.md
└── requirements.txt
```
## 🖥️ Screenshots

### 🏠 Home Interface

<img width="1920" height="1080" alt="Screenshot 2026-07-26 110412" src="https://github.com/user-attachments/assets/54c0e354-1b08-47a7-b11a-7067080b3cae" />

### 📊 Analysis Report

<img width="1920" height="1080" alt="Screenshot 2026-07-26 110638" src="https://github.com/user-attachments/assets/465b2a6e-fbe5-49ff-927d-138c75dc4108" />

---

## 🚀 How to Run

### Python Version

```bash
python phishing_detector.py https://example.com
```

With webpage analysis:

```bash
python phishing_detector.py https://example.com --fetch
```

---

### Web Version

Simply open the HTML file in your browser:

```text
index.html
```

or

```bash
start index.html
```

Enter a URL and click **SCAN** to receive an instant phishing risk report.

---

## 🧠 How It Works

The detector uses a **heuristic (rule-based)** approach instead of machine learning.

### URL Analysis

It checks for:

* HTTPS usage
* Raw IP addresses
* Long URLs
* '@' symbol
* Suspicious keywords
* Suspicious domain extensions
* Multiple subdomains
* URL shorteners
* Typosquatting
* Punycode domains
* High-entropy domain names

### Content Analysis (Python Version)

When the `--fetch` option is enabled, the program also checks:

* Password forms
* External form submissions
* Hidden iframes
* Obfuscated JavaScript
* Favicon mismatches
* Login pages served over HTTP

---

## 📊 Risk Levels

| Score  | Status        |
| ------ | ------------- |
| 0–14   | ✅ Likely Safe |
| 15–39  | ⚠️ Low Risk   |
| 40–69  | 🚨 Suspicious |
| 70–100 | ❌ High Risk   |

---

## 🎯 Future Improvements

* Machine Learning-based detection
* VirusTotal API integration
* WHOIS lookup
* DNS reputation analysis
* SSL certificate validation
* Browser extension
* Threat intelligence integration
* Database for scanned URLs

---

## 📄 License

This project is developed for educational purposes and cybersecurity learning.

