# Contributing to the AI Governance Atlas

Thanks for your interest in contributing. This project maps AI governance frameworks globally, starting with Australia. Community contributions make it better.

## How to Contribute

### 1. Report Issues

Found incorrect data, broken links, or UI bugs? [Open an issue](https://github.com/VVorotilov-AI-AU/australian-ai-governance-atlas/issues/new).

Include:
- What you expected vs. what happened
- Browser and OS
- Screenshot if it's a visual issue

### 2. Correct or Update Governance Data

AI governance moves fast. If a framework has been updated, a new policy published, or a deadline changed:

1. Fork this repository
2. Edit `index.html` and find the `STATES` object (around line 660)
3. Update the relevant state's data
4. Include the official source URL in your PR description
5. Submit a pull request

**Data quality rules:**
- All data must cite an official government source (no news articles as primary source)
- Include the publication date of the source document
- If a framework has been superseded, note both the old and new versions

### 3. Add a New Country

To add a new country's AI governance data:

1. Fork the repository
2. Add the country's GeoJSON polygon coordinates to the `GEO` object
3. Add governance data to the `STATES` object following the existing format
4. Add capital city markers to `CAPITALS`
5. Add state/region labels to `STATE_LABELS`
6. Test that clicking and hovering work correctly
7. Submit a pull request with sources

### 4. Improve the UI

For visual improvements, new features, or bug fixes:

1. Fork and clone
2. Open `index.html` in a browser (it's a single file, no build step)
3. Make your changes
4. Test in Chrome, Firefox, and Safari
5. Submit a pull request

## Data Format

Each jurisdiction entry in the `STATES` object follows this structure:

```javascript
STATE_CODE: {
  name: 'Full Name',
  framework: 'Official framework name and version',
  date: 'Publication date',
  lead: 'Responsible agency or body',
  status: 'mandatory' | 'advisory',
  maturity: 'high' | 'medium' | 'low',
  tier: 'green' | 'amber' | 'grey',
  scope: 'Who the framework applies to',
  distinction: 'What makes this jurisdiction unique',
  mechanism: ['How the framework works (array of strings)'],
  privateSector: 'Impact on private sector',
  funding: 'Funding allocations if known',
  deadlines: [{ label: 'Date', text: 'Description' }],
  links: [{ label: 'Link text', url: 'https://...' }],
  keywords: ['searchable', 'terms']
}
```

## Pull Request Guidelines

- One PR per change (don't bundle unrelated fixes)
- Describe what you changed and why
- Include source URLs for any data changes
- Keep the single-file architecture (no build tools, no npm, no frameworks)
- Test that the globe loads and all interactions work

## Code of Conduct

Be respectful. This is a factual reference tool. Keep contributions objective and well-sourced.

## Questions?

Open an issue or reach out on [LinkedIn](https://linkedin.com/in/vladimir-vorotilov).
