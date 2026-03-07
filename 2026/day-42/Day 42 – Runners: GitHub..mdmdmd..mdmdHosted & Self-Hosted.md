# Day 42 – Runners: GitHub-Hosted & Self-Hosted
## Task 1: GitHub-Hosted Runners
1) Create a workflow with 3 jobs, each on a different OS:

ubuntu-latest

windows-latest

macos-latest

2) In each job, print:

The OS name

The runner's hostname

The current user running the job

Watch all 3 run in parallel

Write in your notes: What is a GitHub-hosted runner? Who manages it?

<img width="1361" height="518" alt="Screenshot (282)" src="https://github.com/user-attachments/assets/79373190-99bc-43f1-bb80-0711ad530846" />

## WHAT ARE GITHUB-HOSTED RUNNERS?
- A runners who provide github action for our workflow are called github hosted runners.They are all pre-installed and managed by github-actions.

  # Task 2: Explore What's Pre-installed

 1)  On the ubuntu-latest runner, run a step that prints:
 
Docker version

Python version

Node version

Git version

4) Look up the GitHub docs for the full list of pre-installed software on ubuntu-latest
   
Write in your notes: Why does it matter that runners come with tools pre-installed?

<img width="1366" height="768" alt="Screenshot (283)" src="https://github.com/user-attachments/assets/099a87e8-4122-4c7a-a78a-9911be3a7df3" />

 ##  Importance of pre-installed tools
 
 - save time
  
 - yaml file clean and easy to maintainable

  
 - faster build and test.
   

 # Task 3: Set Up a Self-Hosted Runner


 <img width="1366" height="768" alt="Screenshot (284)" src="https://github.com/user-attachments/assets/8eb51d53-a4e6-4f37-91fb-9f99821dbaf2" />
 
 - successfully created my selfhosted runner.

   # ask 4: Use Your Self-Hosted Runner

   Create .github/workflows/self-hosted.yml
   
Set runs-on: self-hosted

Add steps that:

Print the hostname of the machine (it should be YOUR machine/VM)

Print the working directory

Create a file and verify it exists on your machine after the run

Trigger it and watch it run on your own hardware

Verify: Check your machine — is the file there?




