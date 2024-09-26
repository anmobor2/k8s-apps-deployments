This document tracks the versions of Helm charts used in this project. Please update this file whenever a chart version is changed or a new chart is added.

## Table of Contents

- [Jenkins](#jenkins)
- [Other Applications](#other-applications)
- [How to Update Chart Versions](#how-to-update-chart-versions)

---

## Jenkins

### Chart Information

- **Chart Name:** Jenkins
- **Repository:** [https://charts.jenkins.io](https://charts.jenkins.io)
- **Current Version:** 4.0.0
- **Helm Repository Version:** 3.5.2
- **Environment-Specific Values Files:**
  - **Development:** `jenkins/values/values-dev.yaml`
  - **Staging:** `jenkins/values/values-staging.yaml`
  - **Production:** `jenkins/values/values-prod.yaml`

### Change History

| Date       | Version | Change Description                                         | Author          |
|------------|---------|------------------------------------------------------------|-----------------|
| 2024-09-25 | 4.0.0   | Initial setup of Jenkins chart with custom values          | Antonio Moreno  |
| 2024-10-05 | 4.1.0   | Updated Jenkins to version 4.1.0 to address security fixes | Antonio Moreno  |

---

## Other Applications

### ExampleApp

- **Chart Name:** ExampleApp
- **Repository:** [https://charts.example.com](https://charts.example.com)
- **Current Version:** 2.3.0
- **Helm Repository Version:** 2.1.0
- **Environment-Specific Values Files:**
  - **Development:** `exampleapp/values/values-dev.yaml`
  - **Staging:** `exampleapp/values/values-staging.yaml`
  - **Production:** `exampleapp/values/values-prod.yaml`

### Change History

| Date       | Version | Change Description                                     | Author          |
|------------|---------|--------------------------------------------------------|-----------------|
| 2024-09-25 | 2.3.0   | Initial deployment of ExampleApp                       | Antonio Moreno  |

---

## How to Update Chart Versions

1. **Identify the New Version:**
   - Check the chart repository for the latest version.
   - Update the `Chart.yaml` or `requirements.yaml` file with the new version.

2. **Run Helm Dependency Update:**
   - Execute `helm dependency update` in the appropriate directory to download the updated chart.

3. **Test the New Version:**
   - Deploy the chart in a non-production environment and verify its functionality.

4. **Document the Change:**
   - Update this `chart-versions.md` file with the new version and details.
   - Add a new entry in the **Change History** section for the relevant chart.

5. **Commit and Push:**
   - Commit your changes to the repository and push them to the remote.

---

*Note:* Always ensure that the versions documented here match the versions specified in the Helm values files or dependencies.
