# NOFA AI Evaluator v7.21 Release Notes

## New Features

### Sticky Headers with Score Summaries
All major screens now have sticky headers displaying score summaries at a glance:
- Scoring step (Pro & Simple modes)
- Global Review
- Recommendation step
- Summary/Export step

### Sticky Footer Navigation
All screens now have sticky footer navigation for easier workflow.

### Expandable Comment Sections
- Global Review now has expandable/collapsible comment sections
- Works in both Simple and Pro modes
- Reduces visual clutter while keeping details accessible

### Redesigned Summary Page
- Compact 4-column score grid layout (replaces long list)
- Eliminates blank space issue with long recommendation text
- Summary comments are expandable/collapsible
- Questions section uses collapsible details element

### Keyboard Shortcuts
- **0-4 keys**: Quickly assign scores while reviewing criteria
- **Ctrl+Z**: Undo last change

### Undo Functionality
- Undo button available in the header
- Tracks last 50 changes with full history stack
- Works across all score and comment changes

### Compact Pro Mode Header
- Purple header now more compact with all 5 section scores in single row
- Reduced padding and font sizes for better screen utilization
- Notes textarea always visible with min-height 100px

### Notes Export Controls
- Global "Include All" / "Exclude All" toggles for notes
- Individual include/exclude toggle on each criterion
- More compact Notes for Export bar

### Additional Improvements
- Cancel button for Re-Analyze All batch operations
- Persistent "Last saved X ago" indicator in header
- Security warning for API key localStorage storage
- Fixed bottom navigation buttons being cut off in Review Scores

## Technical Changes
- Added `toggleCommentExpand()` function
- Added `toggleSummaryExpand()` function

## Download
Download `NOFA_AI_Evaluator_v7.21.html` and open in your browser to get started.
