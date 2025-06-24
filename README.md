# Problem_statement_1

# Title: Product Requirement and Low-Fidelity Wireframes

## Background/Task:
•	A security product requires scanning container images and showing users the findings.  
•	Container images contain applications with their dependencies and all these components might have known vulnerabilities.

## Product Requirements document:

### 1. Problem Statement:
This product helps users manage thousands of container images that may include known vulnerabilities. Without a clear view of which images are affected and how severely, prioritizing and fixing issues becomes difficult.

### 2. Goals & Objectives:
•	Enable users to quickly identify vulnerable container images in their registry.  
•	Categorize vulnerabilities by severity (e.g., Critical, High, Medium, Low).  
•	Allow filtering/sorting based on severity, image name, and last scanned date.  
•	Provide actionable remediation suggestions.  
•	Support bulk actions or integrations for fixing vulnerabilities.

### 3. Key Features:

#### A. Dashboard View
•	Total container images scanned.  
•	Number of vulnerable images.  
•	Breakdown of vulnerabilities by severity (Critical, High, Medium, Low).

#### B. Image Vulnerability Table
•	Paginated table with:  
•	Image name and tag  
•	Last scanned date  
•	Number of vulnerabilities (grouped by severity)  
•	Fix availability status  
•	Filters: severity, fixable only, scan date, image name/tag  
•	Sorting by image name, most vulnerable, etc.

#### C. Image Detail View
•	Image metadata (name, tag, digest, last scanned).  
•	List of vulnerabilities with:  
	o	CVE ID  
	o	Severity  
	o	Affected package/version  
	o	Fixed in version  
	o	Fix available (Yes/No)  
	o	Links to CVE advisories  
•	Option to export report (PDF/CSV)  
•	Suggested remediation steps

#### D. Search and Filter
•	Full-text search on image name, CVEs, tags.  
•	Filter by severity, fixable vulnerabilities, image status.

#### E. Notifications/Alerts 
•	Trigger alerts for new Critical/High vulnerabilities.  
•	Integrations with Slack, email, Jira.

### 4. User Personas:
•	DevSecOps Engineer – triages vulnerabilities and enforces compliance.  
•	Security Analyst – monitors and reports on security posture.  
•	Platform Engineer – remediates issues by rebuilding or patching images.

### 5. key impacts and benefit:
•	You'll catch security issues early before they become real threats.  
•	Secure container images mean fewer vulnerabilities in deployed systems  
•	Centralized dashboard gives a clear view of vulnerabilities across the entire image repository.  
•	Integrates with CI/CD pipelines and issue trackers for faster DevSecOps adoption.  
•	Developers, DevOps, and Security can coordinate using shared data and tools.


