---
name: Deprecation
about: For the Octopus team to make customers aware of upcoming deprecations.
---

**_Are you a customer of Octopus Deploy? Please contact [our support team](https://octopus.com/support) if you have any questions regarding an upcoming deprecation.**

# Prerequisites

- [ ] I have updated the [public deprecation schedule](https://octopus.com/docs/deprecations)
- [ ] I have written a descriptive issue title

# Description

<!-- Take the time to describe the deprecation and link to the public deprecation schedule if necessary -->

# Process
- The functionality will be marked as deprecated in code, causing any usages to be logged for monitoring purposes
- After the notification period of at least 6 months the functionality will be toggled off, resulting in an error when attempting to use it. Customers can toggle this back on if they still require it.
- After another 12 months the functionality will be completely removed

# Migration Guide

<!-- If necessary, provide a guide for customers who may need to migrate away from the deprecated feature -->
