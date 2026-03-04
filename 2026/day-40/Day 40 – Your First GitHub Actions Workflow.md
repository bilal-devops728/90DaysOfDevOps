# Day 40 – Your First GitHub Actions Workflow
## Task 1: Set Up
Create a new public GitHub repository called github-actions-practice

Clone it locally

Create the folder structure: .github/workflows/

<img width="1366" height="768" alt="Screenshot (281)" src="https://github.com/user-attachments/assets/a462f842-e930-4371-9f0a-d156f62c5c4c" />

# Task 2: Hello Workflow

Create .github/workflows/hello.yml with a workflow that:

Triggers on every push

Has one job called greet

Runs on ubuntu-latest

Has two steps:

Step 1: Check out the code using actions/checkout

Step 2: Print Hello from GitHub Actions!

Push it. Go to the Actions tab on GitHub and watch it run.

Verify: Is it green? Click into the job and read every step.
