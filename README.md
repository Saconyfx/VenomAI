# VenomAI
An AI-powered cybersecurity agent

## Table of Contents
* [Introduction](#introduction)
* [Features](#features)
* [Requirements](#requirements)
* [System-Requirements](#System-Requirements)
* [Installation](#installation)
* [Usage](#usage)
* [Options](#options)
* [License](#license)
* [Contributing](#contributing)
* [Disclaimer](#disclaimer)

# Introduction
VenomAI is an autonomous AI agent designed for cybersecurity analysis, threat evaluation, and intelligent automation. Built with Flask and PhiData, VenomAI allows users to interact naturally while performing offensive and defensive security tasks such as subdomain discovery, port scanning, SSL certificate checks, and more. This intelligent agent combines real-time plugin execution with large language model reasoning making it an ideal AI companion for ethical hackers, defenders, and researchers alike. YouTube video link https://youtu.be/ZM2gbXFGcTs

# Features
AI-powered chat interface using OpenAI (via PhiData integration)
Built-in plugin system for various offensive and defensive cybersecurity utilities
Web-based GUI with dark mode, plugin selector, and chat history
Supports both natural language input and plugin-based analysis


# Requirements
Python 3.8+
Flask
PhiData
OpenAI API Key
Nmap (for port scanning plugin)

# System Requirements
Before installing Python dependencies, ensure the following are installed:

Python 3.8+
pip
Rust & Cargo (required for some packages)

To install Rust & Cargo on Debian-based systems (like Kali Linux):

```bash
sudo apt update
sudo apt install cargo
```

# Installation
Follow these steps to set up and run VenomAI locally:

1. Sign Up for API Keys
To enable AI and security features, you’ll need two API keys:

OpenAI API Key: Get it from https://platform.openai.com/account/api-keys

VirusTotal API Key: Get it from https://www.virustotal.com/gui/my-apikey

2. Clone the Repository
git clone https://github.com/Saconyfx/VenomAI.git

cd VenomAI

3. Set Your API Keys in the .env File
Navigate into the ai folder and edit the .env file. Add your API keys like this:

OPENAI_API_KEY=your_openai_api_key_here
VT_API_KEY=your_virustotal_api_key_here
Or run this from the project root (adjusting with your keys):

## Linux/macOS

echo "OPENAI_API_KEY=your_openai_api_key_here" >> .env && echo "VIRUSTOTAL_API_KEY=your_virustotal_api_key_here" >> .env

## Windows CMD

echo OPENAI_API_KEY=your_openai_api_key_here>> ai\.env && echo VT_API_KEY=your_virustotal_api_key_here>> ai\.env

4. Create a Virtual Environment (Recommended)
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate

5. Install Dependencies
pip install -r requirements.txt
pip install openai

7. Run the Flask Server
python3  venomai.py

Visit http://localhost:3841 in your browser to start using VenomAI.


# Usage
To use VenomAI, follow these simple steps:
Select a plugin from the dropdown (e.g., Port Scanner, DNS Lookup, SSL Checker, etc.)
Type your query or target domain into the message input field or ask general cybersecurity questions like “What is the difference between IDS and IPS?”
Click Send VenomAI will either run the selected plugin or provide an intelligent AI-generated response based on your input.

# Options
Plugin Options<br>
Port Scanner – Uses Nmap to scan open ports.<br>
Subdomain Finder – Extracts subdomains using crt.sh.<br>
Find Pages – Finds public pages using HackerTarget API.<br>
SSL Checker – Retrieves SSL grade and certificate chain from SSL Labs.<br>
Security Headers – Scans for missing HTTP security headers.
Virus Check – Uses VirusTotal to assess domain reputation.
Whois Lookup – Performs WHOIS domain lookup.
DNS Lookup – Queries DNS records.
IP Address Lookup – Fetches geolocation and ASN info from ipinfo.io

# License
VenomAI is released under the GNU General Public License version 3 (GPL-3.0).
This means you are free to redistribute or modify the software under the terms of the GPL as published by the Free Software Foundation, either version 3 of the License or (at your option) any later version.

This software is distributed in the hope that it will be useful, but without any warranty—not even the implied warranty of merchantability or fitness for a particular purpose.
For more details, please refer to the GNU General Public License.

# Contributing
Contributions are always welcome! If you'd like to contribute to VenomAI, feel free to fork the repository, work on your improvements or ideas, and submit a pull request — whether it's bug fixes, new features, or enhancements to existing capabilities.


# Disclaimer
VenomAI is released under the GNU General Public License version 3 (GPL-3.0).
This means you are free to redistribute or modify the software under the terms of the GPL as published by the Free Software Foundation, either version 3 of the License or (at your option) any later version.

This software is distributed in the hope that it will be useful, but without any warranty—not even the implied warranty of merchantability or fitness for a particular purpose.
For more details, please refer to the GNU General Public License.

