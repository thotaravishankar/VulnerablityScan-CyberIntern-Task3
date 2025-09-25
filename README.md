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
| Severity | Count | Example Vulnerability (CVE)                   | Exploitation                                                                                   | Solution                                                                                                    |
|----------|-------|-----------------------------------------------|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Critical | 1     | Oracle Database Unsupported Version Detection | Unsupported Oracle versions no longer receive security patches. Attackers can exploit known vulnerabilities in these versions. | Upgrade to a version of Oracle Database that is currently supported.                                       |
| High     | 1     | Oracle TNS Listener Remote Poisoning          | The TNS Listener listens on port 1521 (default) and handles incoming Oracle client connections. Remote Poisoning occurs when an attacker sends crafted requests to the listener. | Apply the workaround in Oracle's advisory.                                                                |
| Medium   | 1     | SMB Signing not required                      | An attacker can perform man-in-the-middle attacks.                                             | Enforce message signing in the host's configuration. On Windows, this is found in the policy setting 'Microsoft network server: Digitally sign communications (always)'. On Samba, the setting is called 'server signing'. See the 'see also' links for further details. |
| Low      | 9     | Missing HTTP Security Headers                 | Content type attacks, execution of malicious scripts.                                          | Apply best practice fixes, e.g., add security headers (CSP, X-Frame-Options, X-Content-Type-Options, HSTS). |


Mitigation / Remediation Ideas:

Critical: Disable SMBv1, apply Microsoft security patch.

High: Update OpenSSL, Apache, or other outdated software.

Medium: Reconfigure SSH/HTTP settings to use stronger ciphers/headers.

Low: Apply general system hardening.


