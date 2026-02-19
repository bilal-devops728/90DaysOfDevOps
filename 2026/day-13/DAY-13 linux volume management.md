# Task 1: Task 1: Check Current Storage

## Task 2: Create Physical Volume
- we create three physical volume
1) 3GB
2)  9GB
3)  10GB

 <img width="1366" height="768" alt="Screenshot (217)" src="https://github.com/user-attachments/assets/4243f795-e1ad-4750-90b9-fe011e35ace8" />

 Task 3: Create Volume Group
 - we create voulme group by name developrs_vg

 <img width="1366" height="768" alt="Screenshot (218)" src="https://github.com/user-attachments/assets/661c2421-b275-43d7-95c3-682a09adcc03" />

# Task 4: Create Logical Volume
- we create logical volume of 2 logical volume
- 1) developrs_lv  6GB
  2) developrs2_lv 11GB

<img width="1366" height="768" alt="Screenshot (220)" src="https://github.com/user-attachments/assets/a3036194-6b66-4e3e-9bcb-3f172baf57dc" />

# Task 5: Format and Mount
- now we formating and mount our LV developrs2_lv

 <img width="1366" height="768" alt="Screenshot (221)" src="https://github.com/user-attachments/assets/c71c9d82-6d5c-4ee4-9a1b-ca4cdd800291" />

<img width="1366" height="768" alt="Screenshot (222)" src="https://github.com/user-attachments/assets/95875ba4-6f0b-4b13-a34e-09ec788eca8b" />

# Task 6: Extend the Volume

- logical volume is:   1st_logiclvolume
- gropupname:           my_volumegroup
- then we extend our logival volume
- after extended now its dont show df -h so, we need resize the filesystem

- <img width="1366" height="768" alt="Screenshot (224)" src="https://github.com/user-attachments/assets/37b78661-130c-47db-86a6-eb16b66126e2" />




