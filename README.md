# Playwright GitHub Actions CI with Docker

Optimized CI setup for running Playwright tests on GitHub Actions using Docker image.

## Features

- Playwright test configuration
- Optimized GitHub Actions workflow with Docker container
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

This project includes an optimized GitHub Actions workflow (`.github/workflows/playwright.yml`) that:

- Runs on push to `main`/`master` branches
- Runs on pull requests
- Uses Playwright Docker image (mcr.microsoft.com/playwright:v1.49.0-jammy) for faster execution
- Executes all tests
- Uploads test reports as artifacts on failure

### Performance Improvements

- **Docker Image**: Pre-installed browsers eliminate the need for `npx playwright install --with-deps`
- **Faster Execution**: 2nd run onwards significantly faster due to Docker image caching

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
