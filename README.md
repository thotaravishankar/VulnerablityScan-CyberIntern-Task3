# VulnerablityScan-CyberIntern-Task3
 

##  Objective  
The goal of this task was to perform a **basic vulnerability scan** on my personal computer using a free vulnerability scanning tool (OpenVAS Community Edition or Nessus Essentials).  
This exercise helps in:  
- Understanding **common security risks** in personal systems.  
- Learning how vulnerability scanners work.  
- Exploring **CVSS scores**, severity ratings, and prioritization.  
- Practicing documentation of a basic vulnerability assessment.  

---

##  Tools Used  
- **Operating System:** <Windows 10>  
- **Vulnerability Scanner:**  
    Nessus Essentials  
---

##  Step-by-Step Process  

### 1. Installation:  
- Downloaded and installed the vulnerability scanner nessus from browser.  
- Completed setup and allowed required dependencies ( Plugins update for Nessus).  

### 2. Target Configuration:  
- I did a advanced scan on a localhost 127.0.0.1

 3. Running the Scan:

Created a advanced scan in nessus.

Launched the scan against my PC.

Waited ~30–60 minutes for results.

4. Reviewing Results:

Opened the vulnerability report.

Checked vulnerabilities categorized by Critical, High, Medium, and Low severity.

Focused on Critical & High vulnerabilities for documentation.

5. Researching Fixes:

Looked up vulnerabilities in CVE database / security blogs.

Documented simple fixes (patching, updating software, disabling unnecessary services).

6. Documentation

Collected evidence with screenshots.

Scan findings:
| Severity   | Count | Example Vulnerability (CVE)                   | Solution                       |
|------------|-------|-----------------------------------------------|--------------------------------|
| Critical   | 1     | Oracle Database Unsupported Version Detection | Upgrade to a version of Oracle Database that is currently supported. |
| High       | 3     | Outdated OpenSSL Version                      | Upgrade required               |
| Medium     | 5     | Weak SSH Cipher Suites                        | Disable weak ciphers           |
| Low        | 8     | Missing HTTP Security Headers                 | Best practice fix              |



Mitigation / Remediation Ideas:

Critical: Disable SMBv1, apply Microsoft security patch.

High: Update OpenSSL, Apache, or other outdated software.

Medium: Reconfigure SSH/HTTP settings to use stronger ciphers/headers.

Low: Apply general system hardening.


