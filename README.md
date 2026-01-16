# NOFA AI Evaluator

A browser-based tool that helps staff evaluate grant applications faster and more consistently. Runs entirely on your computer with no external servers, keeping all data secure. AI assists with analysis but staff always make the final decisions.

![NOFA AI Evaluator Demo](demo.gif)

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

1. **Open the Application**: Double-click `NOFA_AI_Evaluator_v7.html`
2. **Load a Template**: Upload your Excel scoring template
3. **Enter Application**: Paste or type the application text
4. **Run Evaluation**: Click "Start Evaluation"
5. **Review & Export**: Check scores, make adjustments, export results

## Cost

The tool itself is free. The only cost is AI API usage:

| Usage | Estimated Cost |
|-------|----------------|
| Per Application | $0.50 - $1.50 |
| 50 Applications | $25 - $75 |
| 100 Applications | $50 - $150 |

**ROI Example**: If reviewing one application manually takes 30 minutes and AI reduces that to 10 minutes, you save 20 minutes per application. At 100 applications, that's over 33 hours saved.

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
3. Open `NOFA_AI_Evaluator_v7.html` in a text editor
4. Find `SHARED_API_KEY` in the configuration
5. Replace the empty quotes with your API key:

```javascript
const SHARED_API_KEY = 'sk-ant-api03-your-key-here';
```

Distribute the modified file to your team.

## Version History

| Version | Changes |
|---------|---------|
| v7 | Fixed duplicate file upload bug; Fixed "Back to Evidence" navigation; Added page number input for direct navigation; Improved AI analysis to include attachments/exhibits content; Added admin diagnostics panel |
| v6 | Initial public release with full AI-assisted scoring workflow |

## What AI Does vs. Does NOT Do

| What AI Does | What AI Does NOT Do |
|--------------|---------------------|
| Reads and analyzes text | Make final funding decisions |
| Applies consistent criteria | Override your judgment |
| Explains its reasoning | Store or share your data |
| Suggests scores for review | Submit anything automatically |
| Saves you time | Replace human expertise |

## Development

| Metric | Value |
|--------|-------|
| Lines of Code | 4,132 |
| Development Versions | 7 major iterations |
| Evaluation Criteria | 15+ unique scoring areas |
| Template Support | Flexible (any NOFA format) |

## Demo Video
For a full walkthrough, see the [NOFA AI Analyzer Video](https://github.com/bbuxton0823/nofa_ai_analyzer/releases/download/NOFA_AI/NOFA.AI.Video.mov) in the Releases section.

## License

Internal use only.
