# NOFA AI Evaluator

A browser-based tool that helps staff evaluate grant applications faster and more consistently. Runs entirely on your computer with no external servers, keeping all data secure. AI assists with analysis but staff always make the final decisions.

![NOFA AI Evaluator Demo](demo.gif)

---

## ⬇️ One-Click Install

**No installation required!** Just download and open.

### [📥 Download NOFA AI Evaluator v7.19](https://github.com/bbuxton0823/nofa_ai_analyzer/releases/latest/download/NOFA_AI_Evaluator_v7.19.html)

**How to use:**
1. Click the download link above
2. Open the downloaded `NOFA_AI_Evaluator_v7.19.html` file in your browser (double-click it)
3. That's it! The tool runs entirely in your browser

> 💡 **Tip**: Save the file somewhere easy to find (like your Desktop) for quick access.

> 🔐 **For Teams**: Administrators can pre-configure an API key before distributing. See [Administrator Setup](#administrator-setup) below.

---

## Why This Tool?

- **Increase Capacity**: Review more applications that serve our community
- **Improve Consistency**: Same criteria applied fairly to every application
- **Save Time**: Reduce manual data entry and repetitive analysis
- **Focus on What Matters**: More time for judgment calls, less on paperwork

## Key Benefits

| Benefit | What It Means |
|---------|---------------|
| Faster Reviews | What took hours now takes minutes |
| Fair Scoring | Every application evaluated by the same standards |
| Complete Records | Automatic documentation of all evaluations |
| No Learning Curve | Simple interface anyone can use in minutes |

## Quick Start

1. **Open the Application**: Double-click `NOFA_AI_Evaluator_v7.19.html`
2. **Load a Template**: Upload your Excel scoring template
3. **Enter Application**: Paste or type the application text
4. **Run Evaluation**: Click "Start Evaluation"
5. **Review & Export**: Check scores, make adjustments, export results

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

### Volume Pricing

| Applications | Estimated Cost | Cost per App |
|--------------|----------------|--------------|
| 25 | $12 - $19 | $0.48 - $0.76 |
| 50 | $23 - $38 | $0.46 - $0.76 |
| 100 | $45 - $75 | $0.45 - $0.75 |

### Time Savings Analysis

| Task | Manual Time | With AI Tool | Time Saved |
|------|-------------|--------------|------------|
| Read full application | 15 min | 2 min (AI extracts key info) | 13 min |
| Review linked documents | 20 min | 3 min (auto-fetched & analyzed) | 17 min |
| Score 15 criteria | 25 min | 5 min (review AI suggestions) | 20 min |
| Write justifications | 15 min | 3 min (edit AI reasoning) | 12 min |
| Cross-reference priorities | 10 min | 0 min (automatic) | 10 min |
| **Total per Application** | **85 min** | **13 min** | **72 min (85%)** |

### ROI Calculation

**Assumptions:**
- Staff hourly rate (fully loaded): $75/hour
- Applications per NOFA cycle: 50
- Manual review time: 85 minutes/application
- AI-assisted review time: 13 minutes/application

| Metric | Manual Process | With AI Tool | Savings |
|--------|----------------|--------------|---------|
| Time per application | 85 min | 13 min | 72 min |
| Total time (50 apps) | 70.8 hours | 10.8 hours | 60 hours |
| Staff cost (50 apps) | $5,310 | $810 | $4,500 |
| API cost (50 apps) | $0 | $38 | -$38 |
| **Net Savings (50 apps)** | | | **$4,462** |
| **ROI** | | | **11,600%** |

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

## You Are Always in Control

**Human-in-the-Loop**: The AI assists, but YOU decide.

- **Review Every Score**: All AI-generated scores are visible and can be adjusted
- **Read the Reasoning**: AI explains why it assigned each score
- **Override Anytime**: Change any score with a single click
- **Final Approval**: Nothing is submitted or finalized without your explicit action

## How It Works

The AI is configured to produce consistent, repeatable results:

1. Reads the application text you provide
2. Compares it against the scoring template criteria
3. Assigns scores based on how well the application meets each criterion
4. Writes clear explanations for each score
5. Presents everything for your review

**Deterministic scoring** is achieved by using structured rubrics with defined point values and setting AI parameters to minimize randomness (temperature = 0).

## Security

**No External Servers = No External Attack Vectors**

- **Runs in Your Browser**: Single HTML file that runs locally
- **No Data Storage**: Application data is not saved to any external server
- **Direct API Connection**: Browser connects directly to Anthropic's secure API
- **No Middleware**: No third-party servers process or see your data
- **Your Network**: Works entirely within your organization's network security

## Administrator Setup

To pre-configure a shared API key for your team:

1. Get an API Key at [console.anthropic.com](https://console.anthropic.com)
2. Set spending limits in the Anthropic Console
3. Open `NOFA_AI_Evaluator_v7.19.html` in a text editor
4. Find `SHARED_API_KEY` in the configuration
5. Replace the empty quotes with your API key:

```javascript
const SHARED_API_KEY = 'sk-ant-api03-your-key-here';
```

Distribute the modified file to your team.

## Version History

| Version | Changes |
|---------|---------|
| v7.19 | **Word Document Support**: Added Mammoth.js library to parse .docx files directly in browser; Auto-fetch now extracts text from Word documents for AI analysis; Legacy .doc files show helpful message to convert to .docx or PDF; Better status indicators for unsupported file formats |
| v7.18 | **AI-Powered Document Classification**: Documents are now automatically classified by content analysis, not just filename; AI reads document text and categorizes it (audit, budget, board docs, etc.) even when naming conventions vary; Purple "🤖 AI Classified" badge shows when a document was intelligently categorized; Works globally across different document naming styles and formats |
| v7.17 | **Smart Document Recommendations**: Each evaluation criterion now shows which supporting documents are relevant; Hints like "⭐ Review: Audit/Financial, Budget" guide reviewers to the right documents; Click to see all related documents with explanations of why they matter for scoring; Priority indicators highlight must-review documents |
| v7.16 | **Linked Documents in PDF Viewer**: Added collapsible Linked Documents panel directly in PDF viewer; Reviewers can click any link to open supporting documents in new tabs; Documents grouped by type (Audit, Budget, Exhibit, etc.); Shows fetch status and includes auto-fetch button for one-click analysis |
| v7.15 | **Linked Documents Analysis**: Automatically extracts hyperlinks from uploaded application PDFs; Displays linked documents panel showing all referenced documents (audits, budgets, exhibits); Auto-fetch feature retrieves and analyzes linked PDFs; AI evaluation now includes content from linked supporting documents for more accurate scoring |
| v7.14 | **PDF Zoom Scroll Fix**: Fixed issue where zoomed PDF couldn't scroll to see left edge; PDF now properly scrolls in all directions when zoomed |
| v7.13 | **PDF Viewer Fix**: Fixed bug where Visual PDF viewer displayed pages upside-down on first load; Removed double-rotation issue in PDF rendering |
| v7.12 | **Nonprofit-Appropriate Evaluation**: AI prompts now use nonprofit financial evaluation standards; Fiscal stability scoring updated to assess audit findings, funding diversity, and reserve levels instead of profit metrics; Leveraging criteria recognize multi-year grant relationships and contract renewals; System prompt includes nonprofit context to prevent penalizing organizations for normal grant-seeking behavior |
| v7.11 | **Reference Documents Upload**: Upload Funding Priorities and NOFA Guidelines PDFs; Documents stored locally and persist across sessions; AI cross-references applications against actual County priorities; Cite specific priority names in scoring reasoning |
| v7.10 | AI-powered funding source auto-detection; Analyzes application to suggest HOME, CDBG, or HOME+CDBG with reasoning; One-click "Apply AI Suggestion" button |
| v7.9 | Fixed PDF orientation bug (respects page rotation metadata); Added funding source help tooltip explaining where to find info in applications |
| v7.8 | Added re-upload prompt for restored sessions; Explains PDF files can't be stored in browser and provides easy re-upload button |
| v7.7 | Fixed visual PDF viewer blank pages issue; Better error handling and PDF document reload |
| v7.6 | Fixed scroll behavior - prevents background scrolling when mouse is over modal/PDF viewer |
| v7.5 | Added Escape key and click-outside to close all modals; Shows "Pending analysis" in diagnostics when document loaded but not yet analyzed |
| v7.4 | Added visual PDF viewer with full graphics/charts display; Toggle between Visual and Text views; Zoom controls (50%-300%); All page navigation features work in both modes |
| v7.3 | Performance optimizations: parallel PDF page extraction (5x faster), parallel API batch processing (3 concurrent calls), retry logic with exponential backoff, in-memory caching, debounced rendering |
| v7.2 | Added automatic vision detection - system now scans PDFs for charts/graphs and auto-enables vision analysis when visual content is detected |
| v7.1 | Added Vision Analysis capability for charts, graphs, tables, and visual elements; Updated diagnostics panel to show vision status |
| v7 | Fixed duplicate file upload bug; Fixed "Back to Evidence" navigation; Added page number input for direct navigation; Improved AI analysis to include attachments/exhibits content; Added admin diagnostics panel |
| v6 | Initial public release with full AI-assisted scoring workflow |

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
| Saves you time | |

## Development

| Metric | Value |
|--------|-------|
| Lines of Code | 7,050+ |
| Development Versions | 19 minor releases (v7.x series) |
| Evaluation Criteria | 15+ unique scoring areas |
| Template Support | Flexible (any NOFA format) |
| Supported Documents | PDF, DOCX, TXT, HTML |
| External Libraries | PDF.js, Mammoth.js, SheetJS |

## Demo Video
For a full walkthrough, see the [NOFA AI Analyzer Video](https://github.com/bbuxton0823/nofa_ai_analyzer/releases/download/v7.19/NOFA.AI.Video.mov) in the Releases section.

## License

Internal use only.
