## linux user & group management
- useradd -m username
  <img width="852" height="552" alt="Screenshot (179)" src="https://github.com/user-attachments/assets/7eded2ee-7750-440a-9862-b4f14890ce20" />

  .users: berlin,professor,tokeyu.
   ## Group created
    - groupadd groupname
 <img width="1366" height="768" alt="Screenshot (181)" src="https://github.com/user-attachments/assets/5f642244-d1d2-4887-baf6-9ee793ffb3a0" />

 .Groups: developrs,admins,project-team.
 ## Group assignment
 <img width="1366" height="768" alt="Screenshot (182)" src="https://github.com/user-attachments/assets/1362d12d-55e7-4c96-a29b-880cfb21568e" />

 # Directories created
<img width="1366" height="768" alt="Screenshot (187)" src="https://github.com/user-attachments/assets/debc38fe-ff50-43b7-a21f-43e0ce74a82b" />

  
 
 ## Shareed dircetories

 
1) Create directory: /opt/dev-project

2) Set group owner to developers


3) Set permissions to 775 (rwxrwxr-x)

5) Test by creating files as tokyo and berlin
   <img width="1366" height="768" alt="Screenshot (189)" src="https://github.com/user-attachments/assets/4d909f2f-e99a-4fff-8d40-36d817f1bbc4" />

   ## Home directories of all users

   <img width="1366" height="768" alt="Sc
    reenshot (185)" src="https://github.com/user-attachments/assets/48cad59d-cce8-472a-983e-93f1c40ab8dd" />

## Task 05 Team workspace 

1)Create user nairobi with home directory

2) Create group project-team

3) dd nairobi and tokyo to project-team

4) Create /opt/team-workspace directory

5) Set group to project-team

6) Test by creating file as nairobi

<img width="1366" height="768" alt="Screenshot (190)" src="https://github.com/user-attachments/assets/aa954eb7-34d1-4aa6-884e-32a616df5d3c" />

### COMMANDS USEDD

- useradd

 useradd username

 - creat group

  groupadd groupname

  - add user in groups

   usermod -aG groupname username

   - Multiple user add in group by single line
   - 
   gpasswd -M user1,user2,user3 groupname

  - change group of dir/file
        
     chown :groupname directoryname
 




\\
 
 

   
