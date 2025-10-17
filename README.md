# Playwright GitHub Actions CI

Minimal CI setup for running Playwright tests on GitHub Actions.

## Features

- Playwright test configuration
- GitHub Actions workflow for automated testing
- Simple example tests
- HTML test reports

## Setup

1. Install dependencies:
```bash
npm install
```

2. Install Playwright browsers:
```bash
npx playwright install
```

## Running Tests

Run all tests:
```bash
npm test
```

Run tests in headed mode:
```bash
npx playwright test --headed
```

Run tests in UI mode:
```bash
npx playwright test --ui
```

## CI/CD

This project includes a GitHub Actions workflow (`.github/workflows/playwright.yml`) that:

- Runs on push to `main`/`master` branches
- Runs on pull requests
- Installs dependencies and Playwright browsers
- Executes all tests
- Uploads test reports as artifacts

## Project Structure

```
.
├── .github/
│   └── workflows/
│       └── playwright.yml    # GitHub Actions workflow
├── tests/
│   └── example.spec.ts       # Example test file
├── playwright.config.ts      # Playwright configuration
├── package.json
└── README.md
```

## License

MIT
