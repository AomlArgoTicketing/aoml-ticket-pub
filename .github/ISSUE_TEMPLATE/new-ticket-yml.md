---
name: new-ticket.yml
about: Describe this issue template's purpose here.
title: ''
labels: ''
assignees: ''

---

name: New Issue
description: Submit a new issue with predefined categories
title: "[New Issue] <Add Title Here>"
labels: ["triage"]
assignees: []

body:
  - type: markdown
    attributes:
      value: "### 📝 Please select the type of issue"

  - type: dropdown
    id: category
    attributes:
      label: "Select Issue Category"
      description: "Choose the most relevant category for this issue"
      options:
        - Reprocess request
        - QC queries
        - Phy file queries
        - Hex file queries
        - Meta files queries
        - Traj file queries
        - GDAC queries
        - GTS queries
        - NCEI queries
        - General queries
        - PI queries
        - Core queries
        - Deep queries
        - BGC queries
        - Polar queries
    validations:
      required: true

  - type: textarea
    id: description
    attributes:
      label: "Detailed Description"
      description: "Provide additional details about this issue"
      placeholder: "Explain the issue here..."
    validations:
      required: true

  - type: dropdown
    id: priority
    attributes:
      label: "Set Priority"
      description: "Select the priority level for this issue"
      options:
        - Low
        - Medium
        - High
        - Critical
    validations:
      required: true

  - type: checkboxes
    id: confirm
    attributes:
      label: "Confirmation"
      description: "Check the box to confirm before submission"
      options:
        - label: "I have reviewed all details before submitting."
          required: true
