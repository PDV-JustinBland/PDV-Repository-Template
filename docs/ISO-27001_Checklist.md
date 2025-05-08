# ISO 27001 GitHub Repository Security Checklist

| Control | Area | Description | Status |
|--------|------|-------------|--------|
| A.9.1.2 | Access Control | Repo is private and access is role-based | ✅ / ⬜ |
| A.9.2.3 | Least Privilege | Only essential users have write access | ✅ / ⬜ |
| A.9.4.5 | SSO Enforcement | SSO is enabled for user access (Enterprise only) | ✅ / ⬜ |
| A.12.1.2 | Change Control | Pull requests and code reviews are mandatory | ✅ / ⬜ |
| A.12.4.1 | Logging | GitHub audit log and Actions history are retained | ✅ / ⬜ |
| A.14.2.1 | Secure Dev | CI/CD uses static analysis tools (e.g., CodeQL) | ✅ / ⬜ |
| A.10.1.1 | Secrets Mgmt | All secrets are stored in GitHub Secrets, not code | ✅ / ⬜ |
| A.15.1.1 | Vendor Mgmt | Only approved third-party GitHub apps are allowed | ✅ / ⬜ |
| A.17.1.2 | Backup | Repositories are regularly mirrored or backed up | ✅ / ⬜ |
| A.13.2.1 | Data Handling | No sensitive or customer data stored in code | ✅ / ⬜ |
| A.10.1.4 | Code Signing | Verified commits are required | ✅ / ⬜ |
