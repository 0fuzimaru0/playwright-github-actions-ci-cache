# Playwright GitHub Actions CI with Cache

Optimized CI setup for running Playwright tests on GitHub Actions using Docker image and npm cache.

## Features

- Playwright test configuration
- Optimized GitHub Actions workflow with Docker container
- npm cache for faster dependency installation
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
- Caches npm dependencies for improved build times
- Executes all tests
- Uploads test reports as artifacts on failure

### Performance Improvements

- **Docker Image**: Pre-installed browsers eliminate the need for `npx playwright install --with-deps`
- **npm Cache**: Fixed Node.js version (20) enables efficient dependency caching
- **Faster Execution**: 2nd run onwards significantly faster due to caching

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
