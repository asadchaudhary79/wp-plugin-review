# WordPress Plugin Review Tool

A comprehensive automated and manual review tool for WordPress plugins, focusing on security, coding standards, repository compliance, unit testing, and accessibility.

## Features

- **Automated Analysis**:
  - PHPCS with WordPress Coding Standards (WPCS)
  - PHPStan for static analysis
  - PHPUnit for unit test execution
- **Manual Review Framework**:
  - Comprehensive Security Checklist (Sanitization, Escaping, SQLi, Nonce, Capabilities, etc.)
  - WordPress Coding Standards compliance (Naming, Hook usage, i18n, etc.)
  - WordPress.org Repository Guidelines verification
  - Unit Test coverage and quality assessment
  - Accessibility (WCAG 2.1 AA) evaluation
- **Structured Reporting**:
  - Detailed Markdown report with severity ratings (Critical, High, Medium, Low)
  - Actionable code fixes with before/after snippets
  - Category-based scoring and overall readiness verdict

## Installation & Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/asadchaudhary79/wp-plugin-review.git
   cd wp-plugin-review
   ```

2. Run the setup script to install necessary tools (PHPCS, PHPStan, PHPUnit):
   ```bash
   bash scripts/setup_tools.sh
   ```

## Usage

Currently, this tool is designed to be used as a skill by an AI agent. To trigger a review, provide the plugin folder or zip file and ask for a "plugin review".

The workflow follows these phases:
1. **Setup**: Ensures all environment tools are ready.
2. **Automated Scan**: Runs PHPCS, PHPStan, and PHPUnit.
3. **Manual Audit**: Deep dive into the source code guided by checklists in `references/`.
4. **Report Generation**: Produces a comprehensive report based on `references/report-template.md`.

## Directory Structure

- `scripts/`: Contains environment setup and tool configuration scripts.
- `references/`: Essential checklists and templates:
  - `security-checklist.md`: Deep dive into security patterns.
  - `repo-guidelines-checklist.md`: Repository submission manual.
  - `report-template.md`: Structure for the final review report.
- `SKILL.md`: Detailed instructions for the AI reviewer.

## License

GPL-2.0-or-later
