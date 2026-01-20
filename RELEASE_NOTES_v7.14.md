# NOFA AI Evaluator v7.14 Release Notes

## 🎉 What's New

### 🐛 Bug Fix: PDF Zoom Scrolling (v7.14)
Fixed an issue where the PDF viewer couldn't scroll to see the left edge of the document when zoomed in. The PDF now properly scrolls in all directions when zoomed, allowing you to view the entire document at any zoom level.

### 🐛 Bug Fix: PDF Visual Viewer (v7.13)
Fixed an issue where the Visual PDF viewer displayed pages upside-down when first opening a document. The fix removes a double-rotation problem that occurred with certain PDF files.

### Nonprofit-Appropriate Evaluation (v7.12)
This release significantly improves how the AI evaluates nonprofit organizations by using standards appropriate for the nonprofit sector.

**Key Changes:**
- **Fiscal Stability Scoring**: Now evaluates audit findings, funding diversity, and reserve levels instead of for-profit metrics like "income exceeding expenses"
- **Leveraging Criteria**: Recognizes multi-year grant relationships and contract renewals as valid leveraging
- **System Prompt Updates**: AI now understands that nonprofits secure grants/contracts (not "income") and that budgets showing expenses equal to revenue is normal and healthy

### Reference Documents Upload (from v7.11)
- Upload Funding Priorities and NOFA Guidelines PDFs
- Documents stored locally and persist across sessions
- AI cross-references applications against actual County priorities
- Scoring reasoning now cites specific priority names

---

## 🔒 Security - Your Data Stays Private

**This tool prioritizes your security:**

| Security Feature | What It Means |
|------------------|---------------|
| **Runs 100% in Your Browser** | Single HTML file - no software to install |
| **No External Servers** | Your application data never touches our servers |
| **No Data Storage** | Nothing is saved or stored externally |
| **Direct API Connection** | Your browser connects directly to Anthropic's secure API |
| **No Middleware** | No third-party services see or process your data |
| **Works Offline** | Once loaded, works within your organization's network |

> ✅ **Bottom Line**: Application data stays on YOUR computer. The only external connection is to Anthropic's API for AI analysis, and that connection is encrypted.

---

## 📥 One-Click Installation

**No installation required!** Just download and open.

1. Download `NOFA_AI_Evaluator_v7.14.html` from the **Assets** section below
2. Save it somewhere easy to find (like your Desktop)
3. Double-click the file to open it in your browser
4. You're ready to start evaluating!

---

## 🔑 Getting Your API Key (Required)

You need an Anthropic API key to use the AI features. Here's how to get one:

### Step 1: Create an Anthropic Account
1. Go to **[console.anthropic.com](https://console.anthropic.com)**
2. Click **"Sign Up"** and create your account
3. Verify your email address

### Step 2: Get Your API Key
1. Log in to **[console.anthropic.com](https://console.anthropic.com)**
2. Click on **"API Keys"** in the left sidebar
3. Click **"Create Key"**
4. Give it a name (e.g., "NOFA Evaluator")
5. **Copy the key immediately** - you won't be able to see it again!

### Step 3: Set Up Billing
1. In the Anthropic Console, go to **"Billing"**
2. Add a payment method
3. **Recommended**: Set a monthly spending limit (e.g., $50-100) to control costs

### Step 4: Enter Your Key in the Evaluator
1. Open the NOFA AI Evaluator
2. Click the **⚙️ Settings** button (top right)
3. Paste your API key in the **"API Key"** field
4. The key is saved locally in your browser

> 💡 **Tip**: Your API key is stored only in your browser's local storage. It is never sent anywhere except directly to Anthropic's API.

---

## 📋 How to Use the Evaluator

### Step 1: Upload Your Scoring Template
1. Click **"Upload Scoring Template"** (or the Excel icon)
2. Select your Excel scoring template file (.xlsx)
3. The template defines what criteria will be evaluated

### Step 2: Upload the Grant Application
1. Click **"Upload Application"** (or the PDF icon)
2. Select the applicant's PDF application
3. The AI will extract and analyze the text

### Step 3: Upload Reference Documents (Recommended)
1. Click **"Reference Docs"** button in the toolbar
2. Upload your **Funding Priorities** PDF - helps AI understand County priorities
3. Upload your **NOFA Guidelines** PDF - helps AI apply correct standards
4. These documents persist across sessions (saved locally)

### Step 4: Run the Evaluation
1. Select the **Funding Source** (CDBG, HOME, or both)
2. Click **"Start Evaluation"**
3. The AI will score each criterion and provide reasoning

### Step 5: Review and Adjust
1. Review each AI-generated score and reasoning
2. **You can change any score** - click on it to adjust
3. Add your own notes or comments
4. Export the completed evaluation to Excel

---

## 🔐 For Administrators: Pre-Configure API Key for Your Team

If you want to distribute the evaluator with an API key already set up:

1. Open `NOFA_AI_Evaluator_v7.14.html` in a **text editor** (like Notepad or VS Code)
2. Search for `SHARED_API_KEY` (around line 50)
3. Replace the empty quotes with your API key:
   ```javascript
   const SHARED_API_KEY = 'sk-ant-api03-your-key-here';
   ```
4. Save the file
5. Distribute this modified file to your team

> ⚠️ **Important**: Set spending limits in the Anthropic Console to control costs across your team.

---

## 💰 Cost Estimate

| Usage | Estimated Cost |
|-------|----------------|
| Per Application | $0.50 - $1.50 |
| 50 Applications | $25 - $75 |
| 100 Applications | $50 - $150 |

**ROI Example**: If reviewing one application manually takes 30 minutes and AI reduces that to 10 minutes, you save 20 minutes per application. At 100 applications, that's over 33 hours saved.

---

## ⚠️ Requirements

- **Browser**: Chrome, Firefox, Edge, or Safari (modern versions)
- **API Key**: Anthropic API key (see instructions above)
- **Files**: Excel scoring template + PDF application to evaluate

---

## 🆘 Troubleshooting

| Issue | Solution |
|-------|----------|
| "API Key Invalid" | Double-check you copied the full key; make sure billing is set up |
| PDF not loading | Try a different browser; ensure PDF isn't password-protected |
| Slow evaluation | Large PDFs take longer; try enabling "Vision" only when needed |
| Scores seem off | Upload Reference Documents to give AI more context |

---

## 📞 Support

For questions or issues, contact your system administrator or open an issue on the GitHub repository.
