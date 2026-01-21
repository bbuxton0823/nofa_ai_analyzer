# NOFA AI Evaluator v7.20 Release Notes

## 🚩 Red Flags + 📎 Supplemental Docs + 🔄 Auto-Fetch

**CRITICAL FEATURES**: Version 7.20 introduces automatic eligibility validation, supplemental document uploads, AND automatic fetching of linked supporting documents.

---

## 🔄 Auto-Fetch Linked Documents (NEW)

When you upload a PDF application, the system **automatically fetches all linked supporting documents** and notifies you of any that couldn't be retrieved.

### How It Works

1. **PDF Upload** → System detects hyperlinks to supporting documents
2. **Auto-Fetch** → Documents are automatically downloaded in background
3. **AI Classification** → Each document is classified by type (Budget, Audit, Governance, etc.)
4. **Missing Documents Report** → A modal shows which documents couldn't be retrieved

### Missing Documents Notification

If any documents fail to fetch (CORS blocked, broken links, etc.), you'll see:

- **Summary counts**: Retrieved vs. Could Not Fetch vs. Total
- **Detailed list**: Each missing document with name, type, and reason
- **Manual open buttons**: Direct links to open documents that couldn't be auto-fetched
- **Success list**: All documents that were successfully retrieved

### Why Auto-Fetch?

- **No settings to remember** - Works automatically on every upload
- **Immediate context** - AI has supporting documents available for scoring
- **Clear visibility** - You know exactly which documents need manual review
- **Time savings** - No need to manually click "Fetch All Documents"

### CORS-Blocked Documents

Some county servers block direct browser access (CORS). For these documents:
- Use the "View" button in Linked Documents panel (Google Docs viewer)
- Or click the "Open Manually" button in the notification

---

## 📎 Supplemental Documents System (NEW)

When applicants submit corrections, revised budgets, or additional documentation, you can now upload these directly into the evaluation.

### Two Ways to Upload

**1. Attach to Specific Red Flag**
Each red flag shows an "Attach Document" button. For example, if the budget is below minimum, you can attach the applicant's revised budget spreadsheet directly to that flag.

**2. General Supplemental Upload**
A purple "Supplemental Documents" panel allows uploading any additional documents (clarifications, missing exhibits, etc.)

### AI Re-Analysis Options

When uploading, you're asked:
- **YES (Include in AI)** = Document content will be included when AI scores criteria
- **NO (Reference Only)** = Document stored for your reference but not used in AI analysis

### Automatic Budget Extraction

For budget-related red flags, the system can:
1. Parse the uploaded document (Excel, PDF, etc.)
2. Extract the new funding amounts using AI
3. Offer to update the project info automatically
4. Re-validate eligibility to check if the flag is resolved

### Supported File Types
- PDF, Excel (.xlsx/.xls), CSV, Word (.docx), Text (.txt)

---

## 🚩 Red Flags Eligibility Validation

**CRITICAL FEATURE**: Automatic eligibility validation to prevent ineligible applications from being overlooked.

### The Problem This Solves

In a recent evaluation, an application requesting $36,300 was processed without flagging that the NOFA minimum award for CDBG is $50,000. This critical oversight could have resulted in funding an ineligible application.

**This can never happen again.**

### What's New

**Automatic Eligibility Checks**
When project information is extracted (or manually edited), the system now automatically validates:

| Check | Severity | What It Catches |
|-------|----------|-----------------|
| Minimum Award Amount | 🔴 Critical | Request below funding source minimum |
| Maximum Award Amount | 🔴 Critical | Request exceeds funding source maximum |
| Budget Math Error | 🔴 Critical | Amount requested > total project cost |
| High Cost Per Client | 🟡 Warning | > $5,000 per client served |
| High County Share | 🟡 Warning | County funding > 75% of project |
| Missing Amount | 🟡 Warning | Could not extract requested amount |
| Missing Client Count | 🔵 Info | No beneficiary count specified |

**Funding Source Rules**

| Source | Minimum | Maximum |
|--------|---------|---------|
| CDBG | $50,000 | $150,000 |
| HOME | $100,000 | $500,000 |
| ESG | $25,000 | $100,000 |
| PLHA | $50,000 | $200,000 |

### Visual Indicators

**Header Badge**
A prominent red badge appears in the header whenever red flags are detected:
- 🔴 **Red (Pulsing)**: Critical issues detected
- 🟡 **Amber**: Warnings present
- 🔵 **Blue**: Informational notes only

Click the badge to view full details in a modal.

**Project Info Panel**
A color-coded panel displays all red flags directly in the Project Information step, so reviewers see issues immediately after extraction.

**Confirm Dialog**
If you try to proceed with critical red flags, a confirmation dialog blocks the action and requires explicit acknowledgment.

### Example Scenarios

**Scenario 1: Project Sentinel ($36,300 request)**
```
🔴 CRITICAL: Amount Requested Below Minimum
The application requests $36,300, but the CDBG minimum award is $50,000.
This application is INELIGIBLE for funding without a revised budget.
```

**Scenario 2: Excessive Budget Request**
```
🔴 CRITICAL: Amount Requested Exceeds Maximum
The application requests $600,000, but the HOME maximum award is $500,000.
The budget must be reduced to be eligible.
```

**Scenario 3: Math Error**
```
🔴 CRITICAL: Budget Calculation Error
Amount requested ($150,000) exceeds total project cost ($100,000).
This is mathematically impossible.
```

### How It Works

1. **AI extracts project info** → System automatically validates
2. **Red flags detected** → Visual indicators appear immediately
3. **User edits info** → System re-validates on any change
4. **User clicks Continue** → If critical flags exist, confirmation required
5. **User can still proceed** → Flags are warnings, not hard blocks

### Why This Matters

- **Prevents ineligible applications from being processed**
- **Catches budget errors early** before AI scoring begins
- **Saves time** by flagging obvious issues upfront
- **Maintains compliance** with funding source requirements
- **Documents due diligence** in the evaluation process

---

## Previous Version Highlights

**v7.19** - Word Document Support (Mammoth.js)
**v7.18** - AI-Powered Document Classification
**v7.17** - Smart Document Recommendations
**v7.16** - Linked Documents in PDF Viewer
**v7.15** - Linked Documents Analysis
