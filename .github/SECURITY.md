# Security Policy

## Supported Versions

We are committed to maintaining the security of the `UdemyCourseVault-Offline-Video-Downloader-CLI-Tool`. At this time, we are only actively supporting and patching the latest stable version. If you are using an older version, we strongly recommend upgrading.

| Version | Supported |
| ------- | --------- |
| Latest  | ✅        |
| < Previous | ❌        |

## Reporting a Vulnerability

We take security vulnerabilities very seriously. If you discover a security issue, please report it to us using one of the following methods:

1.  **GitHub Security Advisory:** [https://github.com/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool/security/advisories](https://github.com/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool/security/advisories)
2.  **Email:** Please send an email to `security@example.com` (replace with a real security contact if available). Please encrypt your findings using our [PGP key](link-to-pgp-key) if possible.

We will acknowledge your report within **48 hours** and provide an estimate for a fix.

Please do **NOT** disclose the vulnerability publicly until it has been addressed. We will work with you to coordinate a responsible disclosure timeline.

## Vulnerability Disclosure Policy

When you submit a vulnerability report, we will:

*   Acknowledge receipt of your report.
*   Provide a timeline for investigation and remediation.
*   Provide updates on our progress.
*   Grant a **$100 bounty** for valid, previously undisclosed vulnerabilities that lead to a security fix (subject to severity and impact).
*   Publicly acknowledge your contribution (with your permission).

## Dependency Scanning

We regularly scan our dependencies for known vulnerabilities using automated tools integrated into our CI/CD pipeline. The `uv` package manager, in conjunction with our CI, helps ensure that our Python dependencies are up-to-date and secure.

## Architecture & Design Principles

Our development follows established security best practices, including:

*   **Principle of Least Privilege:** Components operate with the minimum permissions necessary.
*   **Input Validation:** All user inputs and external data are rigorously validated.
*   **Secure Defaults:** The tool is configured with secure settings out-of-the-box.
*   **Regular Audits:** Code undergoes regular security reviews and audits.

Thank you for helping to keep this project secure!