---
applyTo: "**" 
---

# PCI-SSC best practices

- All access attempts and usage of critical assets are tracked and traceable to a unique user. Please use a logging framework to log access to critical assets. <!-- Specific logger ? -->

- This is a list of information that should never be logged:
  - PII (Personally Identifiable Information)
  - passwords
  - unique user identifiers

- Create a change log at the root of the project in a file named "CHANGELOG.md" for any changes to the software architecture, source code, or components that handle or interact with sensitive data, sensitive functions, or sensitive resources