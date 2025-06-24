# Problem_statement_1

Title: Product Requirement and Low-Fidelity Wireframes
Problem Statement 1: Product Requirement and Low-Fidelity Wireframes
📘 Background / Task
A security product is required to scan container images and present findings to users.
Container images bundle applications with their dependencies, and these components may contain known vulnerabilities.

📄 Product Requirements Document
1. Problem Statement
This product helps users manage thousands of container images that may include known vulnerabilities.
Without a clear view of which images are affected and how severely, prioritizing and fixing issues becomes difficult.

2. Goals & Objectives
✅ Enable users to quickly identify vulnerable container images in their registry.

🧮 Categorize vulnerabilities by severity (e.g., Critical, High, Medium, Low).

🔍 Allow filtering/sorting based on severity, image name, and last scanned date.

🛠️ Provide actionable remediation suggestions.

🔄 Support bulk actions or integrations for fixing vulnerabilities.

## 🔑 Key Features

### A. Dashboard View

- Total number of container images scanned
- Number of vulnerable images
- Breakdown of vulnerabilities by severity:
  - Critical
  - High
  - Medium
  - Low

### B. Image Vulnerability Table

A paginated table that includes:

- **Image name and tag**
- **Last scanned date**
- **Number of vulnerabilities** (grouped by severity)
- **Fix availability status**

#### Filters

- Severity
- Fixable only
- Scan date
- Image name/tag

#### Sorting Options

- By image name
- By number of vulnerabilities
- By most vulnerable

### C. Image Detail View
- Image metadata (name, tag, digest, last scanned).
- List of vulnerabilities with:
  - CVE ID
  - Severity
  - Affected package/version
  - Fixed in version
  - Fix available (Yes/No)
  - Links to CVE advisories
- Option to export report (PDF/CSV)
- Suggested remediation steps

### D. Search and Filter
- Full-text search on image name, CVEs, tags.
- Filter by severity, fixable vulnerabilities, image status.

### E. Notifications/Alerts 
- Trigger alerts for new Critical/High vulnerabilities.
- Integrations with Slack, email, Jira.

### 4. User Personas:
- DevSecOps Engineer – triages vulnerabilities and enforces compliance.
- Security Analyst – monitors and reports on security posture.
- Platform Engineer – remediates issues by rebuilding or patching images.

### 5. Key Impacts and Benefit:
- You'll catch security issues early before they become real threats.
- Secure container images mean fewer vulnerabilities in deployed systems
- Centralized dashboard gives a clear view of vulnerabilities across the entire image repository.
- Integrates with CI/CD pipelines and issue trackers for faster DevSecOps adoption.
- Developers, DevOps, and Security can coordinate using shared data and tools.

# Low-fidelity wireframes for the user interface for this product:

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


