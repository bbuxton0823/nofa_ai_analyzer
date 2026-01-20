# NOFA AI Evaluator v7.15 Release Notes

## 🎉 What's New

### Linked Documents Analysis
This release adds automatic extraction and analysis of hyperlinked supporting documents from application PDFs.

**Key Features:**
- **Automatic Link Extraction**: When you upload an application PDF, the system automatically extracts all hyperlinks to supporting documents
- **Document Categorization**: Links are categorized by type (Audited Financial Statements, Budget, Board Resolution, Exhibits, IRS Status, etc.)
- **Linked Documents Panel**: New UI panel displays all linked documents with their types, page numbers, and fetch status
- **Auto-Fetch Feature**: Click "Fetch All Documents" to automatically retrieve and extract text from all linked PDFs
- **AI Integration**: Fetched document content is included in AI evaluation prompts, enabling more comprehensive scoring

**How It Works:**
1. Upload an application PDF as usual
2. Click "Linked Docs" in the settings panel to see extracted links
3. Click "Fetch All Documents" to retrieve linked PDFs
4. Run evaluation - AI now has access to linked supporting documents

**Supported Document Types:**
- Audited Financial Statements
- Budget Documents
- Board Resolutions
- IRS 501(c)(3) Determination Letters
- Exhibits (5, 6, 7, etc.)
- Organization Charts
- Governance Documents
- Compliance Documentation

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

> ✅ **Bottom Line**: Application data stays on YOUR computer. The only external connections are to Anthropic's API and to fetch linked documents from their source URLs.

---

## 📥 One-Click Installation

**No installation required!** Just download and open.

1. Download `NOFA_AI_Evaluator_v7.15.html` from the **Assets** section below
2. Save it somewhere easy to find (like your Desktop)
3. Double-click the file to open it in your browser
4. You're ready to start evaluating!

---

## 📋 Using Linked Documents

### Viewing Linked Documents
1. Upload an application PDF
2. Click the "Linked Docs" button in the settings panel
3. View all hyperlinks found in the application with their document types

### Fetching Linked Documents
1. Click "Fetch All Documents" in the Linked Documents panel
2. The system will attempt to retrieve each PDF link
3. Progress is shown as documents are fetched
4. Successfully fetched documents show a green checkmark

### AI Evaluation with Linked Documents
- After fetching, run your evaluation as normal
- AI will automatically reference linked document content
- Scores may be more accurate with access to audits, budgets, and exhibits

### Troubleshooting
- **CORS Errors**: Some linked documents may not be fetchable due to server restrictions. These are marked as "fetch failed"
- **Non-PDF Links**: Links to websites or non-PDF files are marked as "not fetchable" but can be manually reviewed

---

## 💰 Cost Estimate

| Usage | Estimated Cost |
|-------|----------------|
| Per Application | $0.50 - $2.00* |
| 50 Applications | $25 - $100 |
| 100 Applications | $50 - $200 |

*Cost may be slightly higher when linked documents are fetched, as more content is analyzed.

---

## ⚠️ Requirements

- **Browser**: Chrome, Firefox, Edge, or Safari (modern versions)
- **API Key**: Anthropic API key
- **Files**: Excel scoring template + PDF application to evaluate

---

## 🆘 Troubleshooting

| Issue | Solution |
|-------|----------|
| "API Key Invalid" | Double-check you copied the full key; make sure billing is set up |
| PDF not loading | Try a different browser; ensure PDF isn't password-protected |
| Linked docs not fetching | Server may block external requests (CORS); manually review these documents |
| Scores seem off | Enable linked documents fetch to provide AI with more context |

---

## 📞 Support

For questions or issues, contact your system administrator or open an issue on the GitHub repository.
