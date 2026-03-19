# Australian AI Governance Atlas

Interactive 3D globe visualizing AI governance frameworks across all 8 Australian states and territories.

**[Live Demo](https://vvorotilov-ai-au.github.io/australian-ai-governance-atlas/)**

![Globe Preview](https://img.shields.io/badge/jurisdictions-8-00d4b1) ![Status](https://img.shields.io/badge/status-active-green) ![License](https://img.shields.io/badge/license-MIT-blue)

## What This Is

Every Australian state regulates AI differently. Some have mandatory frameworks with hard compliance deadlines. Others are still advisory. If you're building or deploying AI systems across state borders, you need to know the landscape.

This atlas maps it visually:

- **Green (Mandatory + Mature)**: NSW, QLD, VIC, WA. Hard compliance requirements with enforcement mechanisms.
- **Amber (Mandatory, Narrower)**: NT, ACT. Mandatory but narrower scope or earlier stage.
- **Grey (Advisory / Emerging)**: SA, TAS. Guidance-based, no mandatory requirements yet.

## Features

- 3D interactive globe (Globe.GL + Three.js)
- Click any state for full governance details: framework name, lead agency, mechanism, funding, deadlines
- Search by keywords (e.g., "ISO 38507", "GenAI", "procurement")
- Side-by-side state comparison mode
- Federal/Commonwealth framework timeline
- Color-coded maturity tiers

## Tech

Single HTML file. No build step. No dependencies to install.

- [Globe.GL](https://globe.gl/) for 3D rendering
- Custom point-in-polygon hit detection (bypasses Globe.GL raycasting limitations)
- Vanilla JavaScript, no frameworks

## Disclaimer

**This is a research and educational tool, not legal advice.** All data is sourced from official government publications but may not reflect the latest amendments or interpretations. Always verify against official sources before making compliance decisions. The authors accept no liability for actions taken based on this information.

## Data Sources

All governance data sourced from official state government publications, policy documents, and audit reports as of March 2026. Key sources include:

- NSW Digital: AI Assessment Framework (AIAF)
- QLD QGEA: AI Governance Policy + FAIRA Framework
- VIC DPC: Administrative Guideline for GenAI in VPS
- WA DGov: Artificial Intelligence Policy
- And more (see each state's detail panel for direct links)

## Roadmap

This is v1, covering state-level AI governance frameworks. Planned layers:

- [ ] **Sector regulations**: Healthcare, banking, personal data, government services
- [ ] **Private sector impact**: Which frameworks affect vendors and contractors
- [ ] **International expansion**: Map AI governance globally
- [ ] **Company overlay**: Which organizations operate under which frameworks
- [ ] **Timeline view**: How frameworks have evolved over time

## Contributing

Contributions welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Quick ways to help:**
- Add or correct governance data for a state
- Add a new country's AI governance framework
- Improve polygon accuracy for state borders
- Report bugs or UI issues

## License

MIT License. See [LICENSE](LICENSE).

## Author

Built by [Vladimir Vorotilov](https://linkedin.com/in/vladimir-vorotilov). Research and data compilation from official government sources.

Concept inspired by Josh Tedjasaputra's work at CX Insight.
