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
# Low-fidelity wireframes for the user interface for this product



![Low-fidelity Wireframes](https://github.com/user-attachments/assets/d3201197-9fe6-4ed3-9d5e-a5281729e685)

This Low-fidelity wireframe shows how users can easily monitor and manage vulnerabilities across thousands of container images. It starts with a clear dashboard that highlights key metrics like total scanned images and severity breakdowns. A table view lets users filter, search, and prioritize images based on risk. Clicking into an image reveals detailed vulnerability info, including CVE IDs, affected packages, and available fixes. The layout is simple and intuitive, using clean boxes and labels to focus on function over design. It guides users from identifying issues to acting—making vulnerability triage fast, understandable, and efficient.

## Identify development action items

### Frontend
- Design dashboard layout using component-based UI (React, Vue, etc.)
- Create reusable components: Filters, Image List Table, Severity Badges
- Add pagination and state management for filters and drill-down views

### Backend
- APIs for:
  - Listing scanned images and vulnerabilities
  - Filtering by severity/timestamp
  - Fetching vulnerability details
  - Export functionality
- Integration with vulnerability scanners (Trivy/Clair)

### DevOps infrastructure requirements
- Container registry → CI/CD pipeline → Vulnerability scan → Results in DB
- DB schema:
  - Images table
  - Vulnerabilities table (linked by image ID)

 Flow Diagram:
 
![Low-fidelity Wireframes (1)](https://github.com/user-attachments/assets/9875b2b5-e963-4708-9307-bcefd1bcd50a)

•	Container Registry Integration  
→ Connects to Docker Hub, ECR, or GCR to automatically fetch your container images.  
•	Vulnerability Scanning (Trivy, Clair, Grype)  
→ Scans each image for known security issues using trusted open-source tools.  
•	Scan Scheduler & History Tracking  
→ Automatically scans images on a schedule and keeps a history of all past scans.  
•	Backend API for Image & Vulnerability Data  
→ Acts as the engine room, powering the UI and integrations with up-to-date scan results.  
•	Role-Based Access Control (RBAC)  
→ Ensures users only see and do what they’re allowed to, based on their role.  
•	Frontend Dashboard  
→ Lets users easily view, search, and understand vulnerabilities in their images.  
•	Slack/Email Notifications  
→ Sends alerts to your team when new critical vulnerabilities are found.  
•	Export Endpoints (JSON/CSV)  
→ Allows teams to download scan reports for audits, sharing, or offline use.  
•	CI/CD Integration  
→ Builds security into your development pipelines by scanning images before they go live.

--------------------------------------------------------------------------------



