# 🕵️ X-IOCs-Extract

A lightweight Python tool to **automatically extract Indicators of Compromise (IOCs)** — such as domains, IPs, URLs, and hashes — from posts on **X (formerly Twitter)**. This script is intended for threat intelligence analysts and cybersecurity researchers looking to streamline IOC collection from OSINT sources.

---

## 🔧 Features

* 📥 Collect tweets from X using scraping or API
* 🧠 Parse and extract domains, IPs, URLs, and file hashes
* 📤 Export IOCs to structured dump files
* 🔄 Incremental updates — avoids duplicate collection
* ✍️ Modular extractor for easy integration and extension

---

## 📁 Project Structure

```
X-IOCs-Extract/
├── main.py         # Entry point: Handles tweet collection & orchestration
├── extractor.py    # IOC extraction logic (regexes, formats, filters)
├── README.md       # Project documentation
└── .gitignore      # IOC dumps and cache exclusions
```

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/rodanmaharjan/X-IOCs-Extract.git
cd X-IOCs-Extract
```

### 2. Install requirements

```bash
pip install -r requirements.txt
```

*Note: If you're scraping X, you may need additional headers/cookies or a Twitter API key.*

### 3. Run the script

```bash
python main.py
```

## 🧠 Use Cases

* **SOC teams** gathering emerging threats from infosec X accounts
* **Threat intel pipelines** automating IOC ingestion
* **OSINT analysts** monitoring malware or APT-related IOCs
* **CTI enrichment tools** fed by open social media sources

---

## 🛠 Example IOC Extraction

Given a tweet like:

```
🚨 New #malware campaign dropping from hxxp://malicious[.]com with payload hash: abcd1234... 
```

The tool will extract:

* Domain: `malicious.com`
* IP: `192.168...` 
* Hash: `abcd1234...`

---
