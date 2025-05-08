# Repository Security Policy

This repository follows security best practices aligned with ISO/IEC 27001 standards.

## Access Control
- This repository is private and access is restricted by role.
- Only authorized developers may push changes.
- All contributions require Pull Requests.

## Secure Development
- All code changes must pass automated checks (build, lint, SAST).
- Code reviews are mandatory for all PRs into `Production`.
- Secrets must never be committed and must be stored in GitHub Secrets.

## Change Management
- Production branches (e.g. `Production`) are protected.
- Force-push and branch deletion are disabled.
- Only Pull Requests from the `Testing` branch are accepted into production.

## Audit and Monitoring
- GitHub audit logs are reviewed regularly.
- All GitHub Actions logs are retained for traceability.

## Vendor Dependencies
- Dependencies are monitored using Dependabot.
- Only approved GitHub Apps are authorized.

## Reporting Vulnerabilities
If you discover a security issue, please contact [security@example.com] immediately. Do **not** file public issues.
