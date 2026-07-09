# Automated API Testing Pipeline

This repository contains an automated API testing pipeline built using **Postman**, **Newman**, and **GitHub Actions** to ensure continuous integration and API reliability.

## Tech Stack
* **Testing Tool:** Postman
* **Runner:** Newman
* **Reporter:** newman-reporter-htmlextra
* **CI/CD Platform:** GitHub Actions

## Key Features
* **CI/CD Integration:** Tests trigger automatically on every `push` to the `main` branch to catch breaking changes early.
* **Scheduled Execution:** Configured to run automatically using Cron schedules to monitor API stability daily.
* **Data-Driven Testing:** Driven by external data via a CSV file to validate multiple scenarios and iterations.
* **Advanced Reporting:** Generates detailed, interactive HTML dashboards containing full request/response logs, preserved as GitHub Workflow Artifacts.

## How to Run Locally

To execute these tests on your local machine, follow these steps:

1. **Install Prerequisites:**
   Make sure you have Node.js installed, then run:
   ```bash
   npm install -g newman newman-reporter-htmlextra

2. **Run the Collection:**
   Execute the following command in your terminal:

```bash
newman run "API Testing Practice.postman_collection.json" -e "Beeceptor Practice Environment.postman_environment.json" -d "data.csv" -r htmlextra
