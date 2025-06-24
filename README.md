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

3. Key Features
A. 📊 Dashboard View
Total container images scanned

Number of vulnerable images

Breakdown of vulnerabilities by severity:

Critical

High

Medium

Low

B. 🗃️ Image Vulnerability Table
A paginated table that includes:

Image name and tag

Last scanned date

Number of vulnerabilities (grouped by severity)

Fix availability status

Filters:

Severity

Fixable only

Scan date

Image name/tag

Sorting Options:

Image name

Most vulnerable

Others as needed
