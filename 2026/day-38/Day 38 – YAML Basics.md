# Day 38 – YAML Basics
Create person.yaml that describes yourself with:

name

role

experience_years

learning (a boolean)

Verify: Run cat person.yaml — does it look clean? No tabs

<img width="1366" height="270" alt="Screenshot (270)" src="https://github.com/user-attachments/assets/16497bea-8fbc-46ce-b746-52c99c4e8323" />

# Task 2: Lists

tools — a list of 5 DevOps tools you know or are learning

hobbies — a list using the inline format [item1, item2]

<img width="722" height="236" alt="Screenshot (271)" src="https://github.com/user-attachments/assets/7d5db79c-4141-4980-a29b-4755b786664f" />

<img width="336" height="92" alt="Screenshot (273)" src="https://github.com/user-attachments/assets/bdbb3b09-2c9e-405f-a213-82dc40e56df7" />


<img width="1366" height="52" alt="Screenshot (272)" src="https://github.com/user-attachments/assets/5a49a78d-4bb0-4951-b3ea-cc1e190142c3" />
- There are 2 methods to write yaml
 
  1) using [1,2,3,4] comma seperated
  
   2) using  each items should have  -
 
      # Task 3: Nested Objects

      Create server.yaml that describes a server:

server with nested keys: name, ip, port

database with nested keys: host, name, credentials (nested further: user, password)

Verify: Try adding a tab instead of spaces — what happens when you validate it?

<img width="502" height="289" alt="Screenshot (277)" src="https://github.com/user-attachments/assets/dbb23f0b-7e2a-46dc-8331-0c3597bfa75f" />
<img width="870" height="434" alt="Screenshot (275)" src="https://github.com/user-attachments/assets/e3df9132-4f9e-43fd-8cff-0d40a269fc0e" />

- every level 2 spaces
- yaml doesnot allow tabs.

- # Task 4: Multi-line Strings
- In server.yaml, add a startup_script field using:

The | block style (preserves newlines)

The > fold style (folds into one line)

Write in your notes: When would you use | vs >?

<img width="681" height="238" alt="Screenshot (278)" src="https://github.com/user-attachments/assets/aa56497f-9b79-44e7-b094-725cd631f8b8" />

- when used |    for scripts,config files 
- when used >    for long paragraphe text

 # Task 5: Validate Your YAML
Install yamllint or use an online validator

Validate both your YAML files

Intentionally break the indentation — what error do you get?

Fix it and validate again

<img width="870" height="412" alt="Screenshot (279)" src="https://github.com/user-attachments/assets/b24b6d2d-db45-487c-8446-283559d9ce72" />
### problem:All mapping items must start at the same column at line 13, column 1

### valid:
<img width="868" height="418" alt="Screenshot (280)" src="https://github.com/user-attachments/assets/ab913696-39f6-4c5d-993c-28fab5873395" />

# Task 6 : Spot the Difference


# Block 1 - correct
name: devops
tools:
  - docker
  - kubernetes
# Block 2 - broken
name: devops
tools:
- docker
  - kubernetes

- RESULT: block 1 is valid coz both child have same level. tools is parent and docker and kuberntes is child.
- WHAT THE PROBLEMS IN BLOCK 2
- IN YAML both list have same level.
