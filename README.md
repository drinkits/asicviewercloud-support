# ASiC Signature Viewer for Jira Cloud — User Guide

## Overview

ASiC Signature Viewer adds a panel to Jira issues that detects supported ASiC-based attachments (e.g., BDOC, ASiC) and shows their digital signature details directly in Jira. The UI is compact, responsive, and accessible, with localized texts and dates.

- Verify signatures without leaving the issue
- See who signed a file and when, with clear status indicators
- Download the file from Jira when needed

---

## Prerequisites

- Jira Cloud
- App installed and licensed on your Jira site (Managed by your Jira administrators)

---

## Licensing

This app requires a valid license. If the app is not licensed, you will see:

> ℹ️ **ASIC Signatures is Not Currently Active**  
>  
> This app requires a valid license to function. Please contact your Jira administrator to enable it for your team.

- Regular users: contact your Jira administrator to enable the app.
- Admins: manage the subscription in site administration (Billing/Manage apps), start a trial, or renew/enable the subscription.

---

## Permissions

The app only needs read access to:
- Issue data (to locate attachments)
- Attachment content/metadata (for analysis)
- User info (for localization and accessibility context)

Attachments are never sent outside Jira unless you choose to download or open an external validator link.

---

## Supported File Types

The panel shows only supported signature container formats:
- `.edoc`
- `.asice`
- `.asics`
- `.sce`
- `.scs`
- `.bdoc`
- `.adoc`
- `.ddoc`

If no supported attachments exist, you’ll see an informative message and the app will remain inactive for that issue.

---

## Using the App

1. Open any Jira issue that contains attachments.
2. Find the "Signatures" panel (usually in the right-side panel or issue content area, depending on your Jira layout).
3. Browse supported attachments in a compact list.

### Filter and Pagination

- Filter: type in the "Filter attachments…" field to quickly find files by name.
- Pagination: use the page controls under the list (20 items per page).

### View Signatures

- Click "View Signatures" next to a supported attachment.
- The signature details appear in a left-docked popup.
- If analysis takes a moment, you’ll see an "Analyzing…" indicator.

The popup shows:
- A status icon (Valid/Warning)
- Signer’s name
- Signing date and time (localized to your language/region)

### Actions Menu (…)
- Download file: direct download from Jira
- Full online validation: marked "Coming soon" (opens an external validator once available)

---

## Localization (Languages and Dates)

- Supported languages: English (default), Estonian (et).
- The app follows your Atlassian account language.
- Signature dates are formatted according to your locale (including parsing common preformatted English date strings).

To change language:
1. Go to `id.atlassian.com` > Profile > Language
2. Choose English or Estonian
3. Reload the Jira issue page

---

## Accessibility (A11y)

- Fully keyboard accessible (Tab/Shift+Tab navigation, Enter/Space to activate, Escape to close popups).
- Screen readers announce:
  - Icon-only controls (e.g., "More actions")
  - Popup titles on open
  - Logical reading order: status icon → signer name → date
- The app uses Atlassian Design System tokens for WCAG-compliant contrast.

---

## Layout and Responsiveness

- Compact list with subtle row dividers for high information density.
- Actions remain adjacent to the filename; popups and menus open to the left to maintain proximity.
- On narrow screens, actions wrap under the filename within the same row.

---

## Troubleshooting

**“ASIC Signatures is Not Currently Active”**  
The app is unlicensed or the trial/subscription expired. Contact your Jira administrator to enable the app.

**“No supported attachments were found”**  
The issue has no attachments in supported formats. Attach a supported file (see supported file types above) and reload the page.

**Popups or menus feel off-screen or misaligned**  
They open to the left by design to stay close to the row that triggered them. Scroll the issue content or widen the browser window as needed.

**Date format looks English in Estonian**  
The app re-parses and localizes common English date strings. If you encounter an unusual format, let support know with an example so we can extend parsing.

**Language didn’t change after updating profile**  
Perform a hard refresh of the page (Ctrl/Cmd + Shift + R). Ensure your Atlassian account language is set and try again.

---

## Privacy and Security

- Runs on Atlassian Forge with Atlassian-hosted execution.
- Reads and analyzes attachments only within Jira; no external transfer unless you choose "Download" or open an external validator link.
- Respects Jira permissions (you only see files you’re allowed to access).

---

## Known Limitations

- "Full online validation" is marked as "Coming soon."
- Supported languages: English and Estonian.
- Some rare/legacy date formats may require additional parsing rules.

---

## FAQs

**Can I validate multiple files at once?**  
The app analyzes one file at a time, on demand, to keep the UI responsive.

**Why can’t I see the app panel?**  
The app might not be installed on your site, or you don’t have the right project/issue permissions. Contact your Jira administrator.

**How do I manage the app license?**  
Jira administrators can manage subscriptions in site administration under Billing/Manage apps.

---

## Support

When contacting support, please include:
- Jira site URL and issue key
- A sample of the file (if possible)
- Your Atlassian account language
- A screenshot of the panel or any error message

We’ll help you resolve the issue and ensure your signatures display clearly and accurately.