# Databricks CI/CD with Asset Bundles & Delta Live Tables

This repository is a hands-on guide to building and managing a full CI/CD (Continuous Integration / Continuous Deployment) workflow on the Databricks platform. The core of this project is using Databricks Asset Bundles (DAB) to package, deploy, and manage data engineering assets like ETL pipelines and notebooks.

It demonstrates a practical, production-style workflow, from initial setup and local development using the Databricks CLI to automated deployment in a multi-environment setup (e.g., DEV to PROD).

Key Concepts & Project Recall
This project covers the complete lifecycle of a Databricks project, allowing you to recall the key steps:

Databricks CLI: The foundation for programmatic interaction. This project uses the CLI to authenticate, validate bundle files, and execute deployment commands from a local terminal.

Databricks Asset Bundles (DAB):

Development: How to define your entire project (notebooks, DLT pipelines, job configurations) in a single databricks.yml file. This is the "source of truth" for your deployment.

Change Tracking: Demonstrates how bundles track local file changes and manage updates to existing jobs or pipelines in the workspace.

Deployment: Using databricks bundle deploy to push the project to different environments (like a "development" workspace for testing and a "production" workspace for release).

Destroy: Using databricks bundle destroy to safely remove all deployed assets, which is crucial for testing and cleanup.

ETL Pipeline Deployment: The primary goal. This shows the end-to-end process of packaging a data transformation workflow (e.g., a notebook that runs a Spark job) and deploying it as a Databricks Job.

Databricks Git Folders: Integrating this workflow with version control. This covers how to sync the project with Databricks Git Folders (formerly Repos) to manage code versions and collaborate with a team.

Deploying Delta Live Tables (DLT): A key modern use case. This part of the project specifically defines and deploys a Delta Live Tables pipeline using the Asset Bundle configuration, showing how to manage DLTs as part of your CI/CD process.
