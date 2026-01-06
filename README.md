# [GitHub Usage Report Viewer](https://korniychuk.github.io/github-actions-usage-report/)

A web application to visualize GitHub Usage Reports. Supports both the legacy detailed format and the new summarized format.

[![Live Demo](https://img.shields.io/badge/demo-live-green)](https://korniychuk.github.io/github-actions-usage-report/)

## Features

- 📊 Visualize GitHub Actions, Codespaces, Copilot, and Shared Storage usage
- 📈 Interactive charts (daily usage, pie charts by user/SKU, top workflows)
- 📋 Detailed tables with grouping by Runner, Repository, Workflow, or User
- 🔒 100% client-side processing - your data never leaves your browser
- 🌙 Dark/Light theme support
- 📥 Export reports as HTML

## Supported CSV Formats

The tool supports multiple GitHub usage report formats:

| Format | Columns | Features |
|--------|---------|----------|
| Legacy (15 cols) | `usage_at`, `workflow_name`, `workflow_path`, `username` | Full workflow & user details |
| Legacy (14 cols) | `date`, `workflow_path`, `username` | Workflow path & user details |
| Summarized (12 cols) | `date`, `organization`, `repository` | Aggregated data only |

> **Note:** The new summarized format from GitHub doesn't include workflow or username data. Some grouping options will be disabled when using this format.

## Usage

1. Visit [https://korniychuk.github.io/github-actions-usage-report/](https://korniychuk.github.io/github-actions-usage-report/)
2. Download your usage report from GitHub:
   - Go to your [Organization Billing](https://github.com/organizations/YOUR_ORG/settings/billing/summary) or [Enterprise Billing](https://github.com/enterprises/YOUR_ENTERPRISE/settings/billing)
   - Download the usage report CSV
3. Upload the CSV file to the viewer
4. Explore your usage data!

## Development

### Prerequisites

- Node.js 18+
- npm

### Setup

```bash
npm install
npm start
```

Navigate to `http://localhost:4200/`. The app will automatically reload on file changes.

### Build

```bash
npm run build
```

Build artifacts are stored in the `dist/` directory.

### Running Tests

```bash
npm test
```

## Deployment

The app automatically deploys to GitHub Pages on push to `main` branch via GitHub Actions.

To deploy your own fork:
1. Fork this repository
2. Enable GitHub Pages in repository Settings → Pages → Source: "GitHub Actions"
3. Push to `main` branch

## Credits

This project is a fork of the original [GitHub Actions Usage Report Viewer](https://austenstone.github.io/github-actions-usage-report/) created by [@austenstone](https://github.com/austenstone). 

Thanks to the original author for creating this awesome tool! 🙏

**Original Repository:** [austenstone/github-actions-usage-report](https://github.com/austenstone/github-actions-usage-report)

## License

MIT
