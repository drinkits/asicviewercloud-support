# Data Security and Privacy Statement

**ASiC Viewer Cloud for Jira Cloud**

*Last Updated: September 16, 2025*

## 1. Overview

The ASiC Viewer Cloud for Jira Cloud app ("the App") is built on the Atlassian Forge platform, which is designed with security and privacy as a first principle. The App adheres to strict security standards by ensuring that your data is processed securely and is never stored or transmitted outside of the Atlassian ecosystem.

## 2. Data Processing

*   **Attachment Analysis:** The App accesses Jira attachment content **only when a user initiates an action** (e.g., clicking "View Signatures"). This processing occurs in-memory within the secure Atlassian Forge runtime environment.
*   **No External Processing:** No attachment data, user data, signature details, or validation results are ever sent to any external service or third party. All operations are self-contained within the App's Forge environment.

## 3. Data Storage

*   **No Persistent Data Storage:** The App does **not** store any of your data. It does not use any databases (internal or external) or the Forge Storage API to persist user data, attachment content, or analysis results. All information is discarded after the operation is complete.

## 4. Data Transmission

*   **Internal Communication Only:** The App does **not** transmit any data outside of the Atlassian Cloud infrastructure.
*   **API Calls:** All communication with the Jira Cloud REST API is performed through the secure, authenticated Forge Bridge (`@forge/bridge`). API calls are made on behalf of the current user (`asUser`), respecting all of their existing Jira permissions.

## 5. Permissions and Access

*   **Principle of Least Privilege:** The App requests the minimum set of permissions required for it to function:
    *   `read:issue:jira`: To get basic information about the issue the user is viewing.
    *   `read:attachment:jira`: To access the content of attachments for analysis.
    *   `read:jira-user`: To perform actions on behalf of the user.
*   **Respect for Jira Permissions:** The App fully respects Jira's native permission schemes. A user can only view and analyze attachments on issues that they already have permission to access.

## 6. Security & Privacy by Design

*   **Atlassian Forge Platform:** The App's code is hosted and executed by Atlassian on their secure Forge serverless platform. This provides a sandboxed environment and removes the need for us, the vendor, to manage servers or infrastructure that could otherwise access your data.
*   **No Personally Identifiable Information (PII):** The App does not collect, store, or share any PII.
*   **No Analytics or Tracking:** The App does not include any third-party analytics, user tracking, or telemetry.

## 7. Upcoming Features

*   **"Full online validation" feature:** This future feature will offer an option to send a file's hash or content to an external, trusted validation service (such as the official European Commission DSS validator). This will be an **explicit, user-initiated action**, and the app will never send any data automatically. This policy will be updated with more details before the feature is released.

## 8. Contact

For any questions or concerns regarding data security and privacy, please contact the app vendor at:
**support@drinkits.lv**