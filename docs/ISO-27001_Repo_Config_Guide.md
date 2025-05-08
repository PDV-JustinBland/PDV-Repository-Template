# Repository Configuration Guide

## 📘 New Repository Setup

### 🏷 Naming Convention

Use the format:  
**`{Org}-{Name}-{SubName1}-{SubName2}`**

**Examples:**
```
Productiv-MSAReporting-DataCollection
CTM-OutletOctopus-DataSubmission
```


This ensures consistency and makes repositories easily identifiable across projects and teams.

---

### 🛠 Steps to Create a Repository

1. Go to your GitHub organization.
2. Click **"New Repository"**.
3. Fill in the following:
   - **Repository Name**: Use the naming convention above.
   - **Description**: Provide a clear, concise summary.
   - **Visibility**: Select **Internal**.  
     > 🔒 *Do not choose Private. Public is disabled by default.*
4. Check ✅ **“Initialize this repository with a README”**.
5. Click **"Create repository"**.

---

## 🌿 Configure the Branches

1. Go to your repository’s **"Branches"** page (Settings > Branches).
2. Rename the default `main` branch to `Development`.
   - Click the pencil ✏️ icon next to `main`, enter `Development`, and confirm.
3. Create two new branches:
   - `Testing`
   - `Production`
   > You can do this from the repository’s main page:
   > - Click the branch dropdown.
   > - Type the new branch name.
   > - Select “Create branch: [Name] from Development”.

4. You should now have:
   - `Development` (default)
   - `Testing`
   - `Production`

---

## 🔐 Configure Branch Protection Rulesets

Set up rulesets to enforce access control, review processes, and safe merging workflows aligned with your branching strategy.

### 📦 Ruleset: `Production PR Isolation`

**Purpose:** Ensure that only controlled and reviewed changes reach the `Production` branch.

**Configuration:**

- **Name:** `Production PR Isolation`
- **Enforcement Status:** Enabled
- **Target Branches:** Include by pattern `Production`
- **Rules:**
  - ✅ Restrict deletions
  - ✅ Require linear history
  - ✅ Require a pull request before merging
    - Required approvals: **1**
    - ✅ Require approval of the most recent reviewable push
    - ✅ Dismiss stale pull request approvals when new commits are pushed

**⚠ Limitation:**
GitHub does not natively restrict pull request sources (e.g. allow only `Testing → Production`).  
To enforce this, configure a GitHub Actions workflow that **fails any PR into `Production` not coming from `Testing`** (see `enforce-branch-origin.yml`).

---

### 🔁 Ruleset: `Testing Branch Ruleset`

**Purpose:** Prevent deletion of the `Testing` branch and preserve integrity.

**Configuration:**

- **Name:** `Testing Branch Ruleset`
- **Enforcement Status:** Enabled
- **Target Branches:** Include by pattern `Testing`
- **Rules:**
  - ✅ Restrict deletions


