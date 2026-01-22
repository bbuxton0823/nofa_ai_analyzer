# NOFA AI Evaluator

A browser-based tool that helps staff evaluate grant applications faster and more consistently. Runs entirely on your computer with no external servers, keeping all data secure.

![NOFA AI Evaluator Demo](demo.gif)

---

## ⬇️ One-Click Install

**No installation required!** Just download and open.

### [📥 Download NOFA AI Evaluator v7.21](https://github.com/bbuxton0823/nofa_ai_analyzer/releases/latest/download/NOFA_AI_Evaluator_v7.21.html)

**How to use:**
1. Click the download link above
2. Open the downloaded `NOFA_AI_Evaluator_v7.21.html` file in your browser (double-click it)
3. Enter your Anthropic API key (see [Getting Your API Key](#getting-your-anthropic-api-key) below)
4. That's it! The tool runs entirely in your browser

> 💡 **Tip**: Save the file somewhere easy to find (like your Desktop) for quick access.

---

## Why This Tool?

| Benefit | What It Means |
|---------|---------------|
| **Increase Capacity** | Review more applications that serve our community |
| **Improve Consistency** | Same criteria applied fairly to every application |
| **Save Time** | Reduce manual data entry and repetitive analysis |
| **Focus on What Matters** | More time for judgment calls, less on paperwork |

---

## Quick Start

1. **Open the Application**: Double-click `NOFA_AI_Evaluator_v7.21.html`
2. **Load a Template**: Upload your Excel scoring template
3. **Enter Application**: Paste or type the application text
4. **Run Evaluation**: Click "Start Evaluation"
5. **Review & Export**: Check scores, make adjustments, export results

---

## Getting Your Anthropic API Key

This tool uses Claude AI from Anthropic to analyze grant applications. You'll need an API key to get started. Your API key is stored locally in your browser and is only sent directly to Anthropic's servers.

### 🏢 For Agency/Team Use

If your organization (e.g., San Mateo County Housing and Community Development) has already set up an Anthropic account, your administrator will provide you with a shared API key. Simply skip to Step 4 below and enter the key provided by your admin. All usage will be billed to your agency's account.

### For Individual Setup or Administrators:

1. **Create an Anthropic Account**: Go to [console.anthropic.com](https://console.anthropic.com/) and sign up. You'll need to verify your phone number.
2. **Set Up Billing**: Navigate to [Billing Settings](https://console.anthropic.com/settings/billing) to add a payment method and purchase credits. We recommend starting with $5-10 for testing, or more for team usage.
3. **Create an API Key**: Go to [API Keys](https://console.anthropic.com/settings/keys), click "Create Key", give it a name (e.g., "NOFA Evaluator - County Team"), and copy the key.
4. **Enter in the Tool**: Open the NOFA AI Evaluator, click "Settings", and paste your API key in the "Anthropic API Key" field.

> 💡 **Important**: Your API key starts with "sk-ant-" and should be kept private within your organization. The API will not work until the account has credits — billing must be set up first!

---

## Administrator Setup

To pre-configure a shared API key for your team (so staff don't need to configure anything):

1. Download the `NOFA_AI_Evaluator_v7.21.html` file
2. Open it in a text editor (Notepad, VS Code, etc.)
3. Search for `SHARED_API_KEY`
4. Replace the empty quotes with your API key:
   ```javascript
   const SHARED_API_KEY = 'sk-ant-api03-your-key-here';
   ```
5. Save the file and distribute to your team via shared drive, email, or intranet

> **Note**: Users can still override this key in Settings if needed. Keep the pre-configured file internal to your organization.

---

## Security & Privacy

Your data security is our top priority. This tool was designed from the ground up with privacy in mind.

| Feature | Description |
|---------|-------------|
| **🔒 100% Local Processing** | The entire application runs in your browser. No data is ever sent to our servers because we don't have any servers. Your files never leave your computer. |
| **🔐 Secure API Communication** | Your API key and application data are sent directly to Anthropic's secure servers using encrypted HTTPS connections. We never see or store this information. |
| **💾 Local Storage Only** | Your API key is stored in your browser's local storage on your device. It never travels through any third-party servers or cloud services. |
| **👁️ Full Transparency** | This is open-source software. You can inspect every line of code on GitHub to verify exactly how your data is handled. |

### What This Means For You

- **Grant applications stay private** — Sensitive applicant information never touches external servers except Anthropic's AI
- **No data collection** — We don't track usage, collect analytics, or store any information about you or your work
- **You control your API key** — Clear it anytime from Settings, and you can revoke it from your Anthropic console
- **Offline capable** — The application itself works offline; only AI evaluation requires an internet connection

### Best Practices

- Never share your API key or commit it to version control
- Regularly rotate your API key from the Anthropic console
- Set spending limits in your Anthropic account to control costs
- Use a dedicated API key for this tool (don't reuse keys across applications)

---

## You Are Always in Control

**Human-in-the-Loop**: The AI assists, but YOU decide.

- **Review Every Score**: All AI-generated scores are visible and can be adjusted
- **Read the Reasoning**: AI explains why it assigned each score
- **Override Anytime**: Change any score with a single click
- **Final Approval**: Nothing is submitted or finalized without your explicit action

---

## What AI Does vs. Does NOT Do

| What AI Does | What AI Does NOT Do |
|--------------|---------------------|
| Reads and analyzes text | Make final funding decisions |
| Analyzes charts, graphs, and tables (with Vision enabled) | Override your judgment |
| Extracts and analyzes linked supporting documents | Store or share your data |
| Detects and suggests appropriate funding source | Submit anything automatically |
| Applies consistent criteria | Replace human expertise |
| Explains its reasoning | |
| Suggests scores for review | |

---

## Cost & ROI Analysis

The tool itself is free. The only cost is AI API usage (Claude Sonnet 4).

### API Cost Breakdown

| Component | Tokens (est.) | Cost per App |
|-----------|---------------|--------------|
| Main PDF Analysis | ~15,000 input | ~$0.045 |
| 15 Criteria Evaluations | ~60,000 input + ~15,000 output | ~$0.27 |
| Linked Documents (avg 3) | ~30,000 input | ~$0.09 |
| Vision Analysis (if enabled) | ~5,000 input | ~$0.015 |
| Document Classification | ~10,000 input | ~$0.03 |
| **Total per Application** | | **$0.45 - $0.75** |

*Based on Claude Sonnet 4 pricing: $3/M input tokens, $15/M output tokens*

### Time Savings

| Task | Manual Time | With AI Tool | Time Saved |
|------|-------------|--------------|------------|
| Read full application | 15 min | 2 min | 13 min |
| Review linked documents | 20 min | 3 min | 17 min |
| Score 15 criteria | 25 min | 5 min | 20 min |
| Write justifications | 15 min | 3 min | 12 min |
| Cross-reference priorities | 10 min | 0 min | 10 min |
| **Total per Application** | **85 min** | **13 min** | **72 min (85%)** |

### What You Get for $0.50-$0.75 per Application

- ✅ Full PDF text extraction and analysis
- ✅ Automatic linked document retrieval (PDFs, Word docs)
- ✅ AI-powered document classification
- ✅ 15 criteria scored with detailed reasoning
- ✅ Counter-arguments for each score
- ✅ Evidence excerpts with page references
- ✅ Smart document recommendations per criterion
- ✅ Vision analysis of charts/graphs (when detected)
- ✅ Cross-reference against County funding priorities
- ✅ Funding source recommendation (HOME/CDBG)
- ✅ Export-ready Excel output

---

## Version History

| Version | Changes |
|---------|---------|
| v7.21 | Keyboard shortcuts (0-4 keys), Ctrl+Z undo, 50-change history, Analyze button for individual criteria, sticky headers, compact Pro Mode |
| v7.20 | Counter-arguments for each score |
| v7.19 | Word document (.docx) support |
| v7.18 | AI-powered document classification |
| v7.17 | Smart document recommendations per criterion |
| v7.16 | Linked documents panel in PDF viewer |
| v7.15 | Automatic linked document extraction and analysis |
| v7.14 | PDF zoom scroll fix |
| v7.13 | PDF viewer orientation fix |
| v7.12 | Nonprofit-appropriate evaluation standards |
| v7.11 | Reference documents upload (Funding Priorities, NOFA Guidelines) |
| v7.10 | AI-powered funding source auto-detection |

---

## Demo Video

For a full walkthrough, see the [NOFA AI Analyzer Video](https://github.com/bbuxton0823/nofa_ai_analyzer/releases/download/v7.21/NOFA.AI.Video.mov) in the Releases section.

---

## License

Internal use only.
