# NOFA AI Evaluator v7.19 Release Notes

## Word Document (.docx) Support

Version 7.19 adds the ability to automatically extract and analyze Word documents that are linked in application PDFs.

### What's New

**Word Document Parsing**
The auto-fetch feature now supports .docx files using the Mammoth.js library. When you click "Auto-Fetch Documents", Word documents are now:
- Downloaded and parsed directly in your browser
- Text extracted and included in AI evaluation
- Shown with "✓ Analyzed" status just like PDFs

**Supported File Types**
| Format | Support | Notes |
|--------|---------|-------|
| .pdf | ✅ Full | Text extraction from all pages |
| .docx | ✅ Full | Text extraction via Mammoth.js |
| .doc | ⚠️ Limited | Legacy format - shows conversion message |

**Legacy .doc Files**
The older .doc format (pre-2007 Word) uses a proprietary binary format that cannot be parsed in a browser. For these files:
- An amber "⚠ Legacy .doc" badge is shown
- A helpful message suggests converting to .docx or PDF
- The document link still works for manual review

### How It Works

1. **Automatic Detection**: When auto-fetch encounters a .docx file, it automatically uses Mammoth.js to extract the text
2. **Full Text Extraction**: All text content is extracted, up to 50,000 characters per document
3. **AI Analysis**: Extracted Word document content is included in the AI evaluation alongside PDF content

### Example Documents Now Supported

Based on your sample files:
- ✅ `Conflict_of_Interest.docx` - Will be parsed and analyzed
- ✅ `IRS_non_profit_status_certificate.pdf` - Already supported
- ⚠️ `reasonable_accommodation_statement.doc` - Legacy format, needs conversion

### Technical Details

- Uses Mammoth.js 1.6.0 from CDN
- No server-side processing required
- All parsing happens in your browser
- Same 50,000 character limit as PDFs

### What About Other Formats?

| Format | Status | Recommendation |
|--------|--------|----------------|
| .xlsx | Not supported | Save as PDF for analysis |
| .pptx | Not supported | Save as PDF for analysis |
| .txt | ✅ Works | Fetched as plain text |
| .html | ✅ Works | Fetched as text |

---

## Bug Fixes & Improvements

### PDF Visual Render Error Fix
Fixed the "Cannot use the same canvas during multiple render() operations" error that occurred when rapidly zooming or navigating pages in the Visual PDF view. The fix:
- Tracks the current render task
- Cancels any in-progress render before starting a new one
- Gracefully handles cancellation without showing error messages

### Text View Highlighting Improvements
Improved the accuracy and reliability of text highlighting in the PDF Text View:
- **Removed 100-character limit** - Long AI excerpts now get highlighted properly
- **Added clause-level matching** - Splits evidence by commas/semicolons for better partial matches
- **Progressive substring matching** - Creates 80, 60, and 40 character fragments for very long excerpts
- **Console logging** - Added debug logs to help diagnose highlighting issues

### CORS Proxy Fallback for Linked Documents
Added automatic CORS proxy fallback when fetching linked documents from external servers:
- Tries direct fetch first
- Falls back to multiple CORS proxies if blocked
- Shows 🔒 lock icon and "View" button for documents that can't be auto-fetched
- Informative toast messages about CORS issues

### API Error Feedback
Added user-facing feedback for API/vision failures:
- Header indicator shows when analysis errors occur
- Click for detailed error summary
- Track network issues vs vision-specific failures

---

## Previous Version Highlights

**v7.18** - AI-Powered Document Classification
**v7.17** - Smart Document Recommendations
**v7.16** - Linked Documents in PDF Viewer
**v7.15** - Linked Documents Analysis
