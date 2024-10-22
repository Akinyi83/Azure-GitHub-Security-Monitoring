django.nV
=========
## Azure GitHub Workflow for Security Monitoring

This project connects Microsoft Azure to GitHub to monitor security inconsistencies using Bandit (Python security analyzer) and MSDO tools. Automated alerts are triggered when vulnerabilities are detected through a custom workflow (`simpleworkflow.yml`).

### Setup Instructions
- Set up GitHub Actions for the repository.
- Link your Microsoft Azure account.
- Install Bandit and MSDO for security auditing.
- Configure the workflow using `simpleworkflow.yml`.

### Workflow Overview
The workflow monitors inconsistencies in the code and creates alerts using GitHub Actions. It runs on `windows-latest` and integrates Bandit and MSDO.


django.nV is a purposefully vulnerable Django application provided by [nVisium](https://www.nvisium.com/).
