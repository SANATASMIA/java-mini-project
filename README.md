## Java-mini-projects&practice
Object Oriented Programming written in java and I would like to share some of practices code.


<img src=https://user-images.githubusercontent.com/20365333/127318808-ec8e206e-a608-45a3-bd58-3e209f8f32e7.png width="300" >
<img src=https://user-images.githubusercontent.com/20365333/127318887-5ddccd73-362b-4fc0-940b-30d21f7da6fb.jpg width="300">

**Objective** : 

The goal of this assignment was to enable GitHub Advanced Security (GHAS) features on a Java project. These features help automatically scan and protect our code from security issues. I had to show the results for:

Code scanning

Dependency scanning

Secret detection

Security alerts

**What I Did** :

1.Created a GitHub repository for my Java application.

2.Used a Personal Access Token (PAT) to push the project code to GitHub.

3.Enabled security features using the GitHub Security tab and repository settings.

4.Allowed GitHub to scan the project automatically for security issues.

5.Collected scan results and provided suggestions to fix any problems found.

**Security Features I Enabled** :

In the repository's Settings > Code security and analysis and the Security tab, I turned on the following features:

**Feature	Status** :

1.Security Policy	Enabled (I added a SECURITY.md file)
2.Security Advisories	Created manually
3.Dependabot Alerts	Enabled to check for vulnerable dependencies
4.Code Scanning Alerts	Enabled using GitHub CodeQL
5.Secret Scanning Alerts	Enabled, including protection when pushing secrets

**What GitHub Found (Scan Results)** : 

1. Code Scanning Alerts (via CodeQL)
Type of Issue	Severity	File	Description
SQL Injection	High	UserController.java	Code is directly using user input in SQL queries
Path Traversal	Medium	FileService.java	File paths are being used without validation

2. Dependency Alerts (via Dependabot) 
Vulnerability	Severity	Library Used	Fix Suggested
jackson-databind 2.9.10	Critical	com.fasterxml.jackson.core	Update to version 2.13.0

3. Secret Scanning Alerts
Type of Secret	Severity	File	Description
AWS Access Key	High	application.properties	A real secret key was found in code

**How to Fix These Issues** :

For each issue, here's what I recommend:

Problem	How to Fix
SQL Injection	Use PreparedStatement to safely handle user input in SQL
Path Traversal	Check and sanitize file paths to avoid letting users access system files
Old Library	Update the vulnerable library to the latest safe version
Secret in Code	Move secrets to GitHub Secrets or environment variables instead of hardcoding them

**Screenshots (Evidence)** :

I’ve included screenshots as proof of each step:

GitHub Security tab - 

Code scanning alerts - 

Dependency alerts - 

Secret detection alerts - 

Workflow logs from GitHub Actions - 

(These are placed in a /screenshots folder in the repo)

**What I Did After Fixing the Issues** : 
After fixing some of the vulnerabilities:

I pushed the changes again to GitHub.

GitHub automatically re-scanned the code.

The alerts that were resolved disappeared or were marked as fixed.

**Conclusion** : 
This assignment helped me learn how to use GitHub’s built-in security tools to scan and improve a Java project. The features like CodeQL, Dependabot, and Secret Scanning make it easier to catch and fix issues early—bringing Shift Left Security into the development process.


