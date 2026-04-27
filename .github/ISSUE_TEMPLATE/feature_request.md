name: Feature Request
description: Suggest an idea for JBAutomate
title: "[FEATURE] "
labels: ["enhancement"]
assignees: []

body:
  - type: markdown
    attributes:
      value: |
        Thanks for your interest in improving JBAutomate! Please describe your feature request.

  - type: dropdown
    id: module
    attributes:
      label: Module
      description: Which module does this feature relate to?
      options:
        - Finance (Bank statements, Budget tracking)
        - Meals (Meal planning, Recipes)
        - Travel (Itineraries, Trip planning)
        - Core (General improvements)
        - Other
    validations:
      required: true

  - type: textarea
    id: description
    attributes:
      label: Description
      description: Describe the feature you'd like to see
      placeholder: |
        I would like JBAutomate to [feature description]
    validations:
      required: true

  - type: textarea
    id: use_case
    attributes:
      label: Use Case
      description: Explain the problem this solves or the benefit it provides
      placeholder: |
        This would help me [problem/benefit]
    validations:
      required: true

  - type: textarea
    id: alternatives
    attributes:
      label: Alternative Solutions
      description: Have you considered other approaches?
      placeholder: |
        Other potential solutions...

  - type: textarea
    id: additional
    attributes:
      label: Additional Context
      description: Any other relevant information?

  - type: checkboxes
    id: checklist
    attributes:
      label: Checklist
      options:
        - label: I have checked if this feature already exists
          required: true
        - label: I have searched for similar feature requests
          required: true
