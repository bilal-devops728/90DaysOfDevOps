# Day 39 – What is CI/CD?
- CICD pipeline is an automated process that build,test,and deploy code whenever developrs make changend to project.
- CI-------- Continuous intergration
- CD-------- Continuous devlivery/continuous deployment.
  # Task 1: The Problem.


Think about a team of 5 developers all pushing code to the same repo manually deploying to production.

Write in your notes:

What can go wrong?

What does "it works on my machine" mean and why is it a real problem?

How many times a day can a team safely deploy manually?

- when 5 developrs push code manually and deploy in production then

- ### WHAT CAN GO WRONG
- code conflict
- bugs problems
- one developrs overwrite anothers change
- no automated testing
- deployment mistake 
What does "it works on my machine" mean and why is it a real problem.
-it means the code runs correctly on my machine or local computer.but fails in client oranother enviroments
## WHY THE PROBLEMS:
- different os
- Dependencies
- different enviroments
- different configrations
   CICD solve this by creating consistant automated enviroments.

  ## How many times a day can a team safely deploy manually?
  - usually 1-2 times per day suitable
  Manual deployment:
- slow
- risky
- stressfull

  # Task 2: CI vs CD:
  CI------Continuously intergration
  Developrs frequently push code to a shared reop each push automatically triggers to build and test processses.
  CI include :
  - Bulid code
  - test
  - integration
  - ## CD--------Continuously Delivery/deployment:
    after ci code passes the application is code is automatically prepared for release .it is ready to deploy at any time ,but deployment requires manual approval.
    e.g= after build code passes tests. now ready for stagging manual clicks deploy.

    # Task 3: Pipeline Anatomy

  A pipeline has these parts — write what each one does:

Trigger — what starts the pipeline

Stage — a logical phase (build, test, deploy)

Job — a unit of work inside a stage

Step — a single command or action inside a job

Runner — the machine that executes the job

Artifact — output produced by a job
### TRIGGER:
- when start the pipeline
 ### STAGES
- a majoer phase in pipeline (build,test,deploy)
  ### JOB:
-  A unit of work inside a stage. e.g= run test on ubuntu
  ### STEPS:
-  inside the job single or multiple steps in step unit
   ### RUNNER:
-  the system wherer jobs execure
 e.g= cloud vm or selfhosted server
### ARTIFACT:
output produced by pipelines
- docker images
- test report

- # Task 4: Draw a Pipeline

- # Task 5: Explore in the Wild
Open any popular open-source repo on GitHub (Kubernetes, React, FastAPI — pick one you know)

Find their .github/workflows/ folder

Open one workflow YAML file

Write in your notes:

What triggers it?

How many jobs does it have?

What does it do? (best guess)


https://github.com/frappe/frappe/blob/develop/.github/workflows/create-release.yml


        name: Generate Semantic Release
        
on:
  push:
    branches:
      - version-14-beta
permissions:
  contents: read

jobs:

  release:
  
    name: Release
    
    runs-on: ubuntu-latest
    
    steps:
      - name: Checkout Entire Repository
        uses: actions/checkout@v6
        
        with:
          fetch-depth: 0
          persist-credentials: false
          
      - name: Setup Node.js
        uses: actions/setup-node@v6
        with:
          node-version: 24
      - name: Setup dependencies
      
        run: |
          npm install @semantic-release/git @semantic-release/exec --no-save
      - name: Create Release
        env:
          GH_TOKEN: ${{ secrets.RELEASE_TOKEN }}
          GITHUB_TOKEN: ${{ secrets.RELEASE_TOKEN }}
          GIT_AUTHOR_NAME: "Frappe PR Bot"
          GIT_AUTHOR_EMAIL: "developers@frappe.io"
          GIT_COMMITTER_NAME: "Frappe PR Bot"
          GIT_COMMITTER_EMAIL: "developers@frappe.io"
        run: npx semantic-release

        ### BREAKDOWN:
        trigger: runs on push to specfic branch version-14-beta
        - jobs:  1 job
        -  steps:    checkout repo gets full git history
      
        -  setup Node.js:  install Node 24
        -  install dependiences
        -  Run semantic -release
