---
name: general-ticket.yml
about: Describe this issue template's purpose here.
title: ''
labels: ''
assignees: ''

---

name: General Ticket Submission
description: Submit a new issue related to processing, QC, files, or general queries.
title: "[Category] - Short Description"
labels: ["Status: New"]
assignees: 

body:
  - type: markdown
    attributes:
      value: |
        Thank you for submitting your request! Please provide as much detail as possible.

  - type: dropdown
    id: category
    attributes:
      label: Select Issue Category
      options:
        - Reprocess Request
        - QC Queries
        - Phy File Queries
        - Hex File Queries
        - Meta Files Queries
        - Traj File Queries
        - GDAC Queries
        - GTS Queries
        - NCEI Queries
        - General Queries
        - PI Queries
        - Core Queries
        - Deep Queries
        - BGC Queries
        - Polar Queries

  - type: input
    id: request_title
    attributes:
      label: Brief Title
      placeholder: e.g., "QC Issue in Float Data"

  - type: textarea
    id: issue_description
    attributes:
      label: Detailed Description
      description: Provide all relevant details, error messages, or file names.

  - type: input
    id: submitter_email
    attributes:
      label: Your Email (optional)
      description: Provide your email if you want status updates.

  - type: textarea
    id: additional_info
    attributes:
      label: Additional Comments or Attachments
      description: You may include any extra details, relevant links, or attach logs/screenshots.
