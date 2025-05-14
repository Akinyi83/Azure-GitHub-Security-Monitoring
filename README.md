#  Integrating Static Analysis Tools into the Development Lifecycle – Microsoft Defender for DevOps

** Report by:** Vallary Akinyi Ogolla  
** ID:** CS-CNS06-24142

---

##  Introduction

In this lab, I explored the integration of static analysis tools into the development lifecycle using **Microsoft Defender for DevOps**.

This exercise involved configuring **Microsoft Security DevOps**, a command-line application that automates the installation, configuration, and execution of various static analysis tools to enhance security and compliance in software development.

Through hands-on experience with tools like **Bandit**, **ESLint**, **CredScan**, and more, I gained practical insights into how these tools can be integrated within **Azure DevOps** and **GitHub Actions** to identify and address potential security vulnerabilities early in the development process.

---

##  Objectives

By the end of this lab, I aimed to achieve the following:

-  Conduct a Static Application Security Testing (SAST) scan locally using **Bandit**
- Configure the **Microsoft Security DevOps** extension within Azure DevOps
- Set up **Microsoft Security DevOps GitHub Actions** for automated security scanning
-  Utilize the **DevOps Security Workbook** to gain insights into security metrics and findings

---

##  Lab Environment

- Azure DevOps  
- GitHub Actions

---
 Here is the link to my Project report ![DevOps Report](MS_AppInnovation.md) 
##  Methodology

###  Exercise 1: Import the Vulnerable Code

1. On GitHub, fork the vulnerable code from:  
   [`https://github.com/S2FrdQ/VulnDjango`](https://github.com/S2FrdQ/VulnDjango)

2. On Azure DevOps:
   - Create a new **Private project** named `VulnDjango`
   - Navigate to **Repos** and import the code

---

###  Exercise 2: SAST Scan Using Bandit Locally

> Bandit is a tool designed to find common security issues in Python code.

**Steps:**

```bash
# Download the vulnerable code
git clone https://github.com/S2FrdQ/VulnDjango webappdjango
cd webappdjango

# Install Bandit
pip3 install bandit

# (Optional) Add to PATH if required
export PATH="/home/kali/.local/bin:$PATH"

# Run basic Bandit scan
bandit -r .

# Output scan in JSON
bandit -r . -f json | tee bandit-output.json
