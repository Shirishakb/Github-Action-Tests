# GitHub Actions Tests

## Your Task

As applications scale and develop, developers want to ensure that certain quality checks are met prior to merging to important branches; thus, you'll want to familiarize yourself with Continuous Integration (CI) and Continuous Deployment (CD) that are common practices used to ensure consistency, quality, and deployment of latest code once all checks have been met and merged to `main`.

Your task is to create a CI/CD pipeline using GitHub Actions to run the component tests via Cypress when a Pull Request is made to the `develop` branch, and the application is deployed when code is merged from `develop` to the `main` branch.

## User Story

```md
AS A developer looking to integrate a pipeline in a codebase for continuous integration and deployment, 
I WANT to create a GitHub Action that will follow best practices by running test cases when a Pull Request is made to the develop branch
SO THAT I can ensure that all code integrations are clean and pass the proper requirements.

AS A developer looking to deploy the application automatically to Render when code is merged from develop to main,
I WANT to create a GitHub Action that will run when the code is merged to main and automatically deploys to Render
SO THAT the application is constantly updated when major releases are made to the main branch.
```

## Acceptance Criteria

```md
GIVEN a fullstack application for a web developer,
WHEN I upload new features to the application
THEN I should be making Pull Requests to a develop branch first
WHEN I create a Pull Request to a develop branch
THEN I should be executing a GitHub Action that checks the Cypress component tests
WHEN I see that the tests pass on GitHub Action
THEN I should see those test results on GitHub Action and merge the code
WHEN I push the code from the develop branch to the main branch
THEN I should see that another GitHub Action triggers and should automatically deploy to Render
```

## Mock-Up

Your GitHub Actions for tests should look similar to the image below:

![GitHub Actions Cypress Test.](./Assets/yaml1.png)

Your GitHub Actions for deployments should look similar to the image below:

![GitHub Actions Render Deploy.](./Assets/yaml2.png)

## Getting Started

You'll first upload the content inside the `Develop` folder to a GitHub Repository. 

You'll then deploy the application via [Render and MongoDB](https://coding-boot-camp.github.io/full-stack/mongodb/deploy-with-render-and-mongodb-atlas).

Once you see the application has been deployed, you'll navigate to the Settings option and turn off Auto-Deploy.

![Render image of auto deploy and hook](./Assets/19-Render-Settings.png)

Copy the `Deploy hook` URL as you will need it to properly configure GitHub Actions to deploy to Render.

Next, create a `develop` branch (either on GitHub directly or via command-line) where all feature branches will be merged to.

> **note** Your feature branches should always be merged to the `develop` branch. Only the `develop` branch should be merged to the `main` branch.

You will want to have two separate `YAML` files: one configured to execute GitHub Actions for tests when a Pull Request is made to the `develop` branch and the other configured to execute GitHub Actions to automatically deploy to Render when `develop` is merged to `main` branch.

Use the following resources below:

Resources:

* [Render Deploy Hooks](https://docs.render.com/deploy-hooks)

* [Render API Key](https://docs.render.com/api)

* [GitHub Repo Secrets](https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions)

* [Main and Develop Branches](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)


  * All Cypress component tests must pass.

  * A GitHub Action must trigger when a Pull Request is submitted and merged to the `main` branch and the Action must automatically deploy the application to Render.

  * The application must be deployed to Render.
# Deployed URL Link
https://github-action-tests.onrender.com