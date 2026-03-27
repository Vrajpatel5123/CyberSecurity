# Lab 2

## Task 1

1. Printenv is basically printing the env of the user.
   <img width="883" height="737" alt="Cyber_HW3_printenv" src="https://github.com/user-attachments/assets/0ce8eb6a-89ce-4124-a4fb-8f2aaed324b4" />

2. export is the same thing as echo but it can only be shared in root aka shell unlike echo (which literally just prints of whats written after it.)
   <img width="873" height="56" alt="Cyber_HW3_export_using!" src="https://github.com/user-attachments/assets/77ff6d0c-1051-40af-adb5-3d0cb5fe4255" />

## Task 2

1. gcc is another way to complie only c code.
   <img width="1191" height="547" alt="Cyber_HW3_export_using_part1" src="https://github.com/user-attachments/assets/0e3c3763-c605-4146-99de-9bc2459c56bb" />
2. Instead of using the parent fork. Now, it will be using the children fork to basically do the same thing aka give the same output just like the parent fork did.
   <img width="1180" height="401" alt="Cyber_HW3_export_using_part2" src="https://github.com/user-attachments/assets/8799f067-a295-4f36-b246-492c7c65bcaa" />

3. There is no difference because it's using the parent fork into the children fork (if that makes sense). Therefore, there isn't any difference found besides the files location that I made.
   <img width="872" height="490" alt="Cyber_HW3_envfile_difference" src="https://github.com/user-attachments/assets/438bbd84-913b-4da6-a580-85fa119ac6a0" />

## Task 3

1. From the code, it launches with /usr/bin/env with no environment variable due to the argument being null. Basically prints nothing.<img width="791" height="73" alt="Cyber_HW3_myenv1" src="https://github.com/user-attachments/assets/8d1b7430-dc30-4772-ad40-ffd00ec16306" />

2. As well as step 3: Before, it was receiving no environment variables. But now with environ, it will able to get the environment variable. <img width="787" height="576" alt="Cyber_HW3_myenv2" src="https://github.com/user-attachments/assets/c9ef0ff1-381f-41ae-a750-3bd3567c9e47" />

3. The new code basically "execve()" in the third argument adding environ. It gave the ability to initial environment for the program. The old code, it had NULL in the third argument. Therefore, nothing was returning in short no environment. Same picture as in step #2. <img width="787" height="576" alt="Cyber_HW3_myenv2" src="https://github.com/user-attachments/assets/c9ef0ff1-381f-41ae-a750-3bd3567c9e47" />

## Task 4

1. <img width="730" height="431" alt="Cyber_HW3_envexample_task4_2 4" src="https://github.com/user-attachments/assets/0a9faaee-b537-4021-8293-4de72c84558e" />
   Basically, its the same thing as printenv but little difference. It's using environment variable to give the same out after running the code.

## Task 5

1. All of the steps are in two picture:

1) <img width="1320" height="861" alt="Cyber_HW3_setuidex_all of it!" src="https://github.com/user-attachments/assets/05182b4b-d0d9-45b6-81ed-fa68286a3609" />
2) <img width="1056" height="76" alt="Cyber_HW3_setuidex_changing to chown and chmod 4755" src="https://github.com/user-attachments/assets/17a13282-9b17-4990-b768-e299b2c14fe5" />

   As I was doing this section, I thought when I was running the export for LB_LIBRARY_PATH was returning empty. I thought it was missing something but later on I found out that it was doing it correctly after I ran the file call setuidex. If you can see, when I initialized ANY_NAME as "James Bond". It also showed up when I ran setuidex.

## Task 6

1. <img width="1317" height="233" alt="Cyber_HW3_lsexample" src="https://github.com/user-attachments/assets/21673a74-7ccc-49c2-a21b-b38fe3b44178" />
   It's in fact running with root privilege. As I ran, its basically doing the same command line when we want to see whats in the current directory like a list of files. Its the exact same functionality used when I ran the code.

## Task 7

1. All of task 1 to 2 are in two pictures:

1)  <img width="1237" height="582" alt="Cyber_HW3_2 7mylibPart1" src="https://github.com/user-attachments/assets/76936f1b-e3ae-481e-a41a-3b442be6ca96" />
2)  <img width="1333" height="776" alt="Cyber_HW3_2 7mylibPart2" src="https://github.com/user-attachments/assets/bf1464d1-2beb-4c96-8c3c-3879eba8cb92" />

- Make myprog a regular program, and run it as a normal user.

* Its stating that "I am not sleeping" is printed (the fake "sleep()" runs)

- Make myprog a Set-UID root program, and run it as a normal user.

* Normal sleep(1) occurs and no output (fake sleep() is ignored)

- Make myprog a Set-UID root program, export the LD PRELOAD environment variable again in the root account and run it.

* The same occurs as it happened on the first one!

- Make myprog a Set-UID user1 program (i.e., the owner is user1, which is another user account), export the LD PRELOAD environment variable again in a different user’s account (not-root user) and run it.

* The same is supposed to happen as the second example!

The Differences is the dynamic linker ignore LD_PRELOAD for SET-UID program unless the user running it owns the program. Therefore, prevents library hacking. (It worked on all of them because I was the owner)

## Task 8

1. <img width="1321" height="272" alt="Cyber_HW3_2 8part1" src="https://github.com/user-attachments/assets/a09e2b1f-93dd-403d-845e-cff63e715188" />
   <img width="952" height="237" alt="Cyber_HW3_2 8part2" src="https://github.com/user-attachments/assets/2cd81e85-8ed8-478c-b7b8-ae79064357d4" />
   If I was Bob, Yes I can compromise the integrity of the system. The code basically is using the same functionality of cat command in linux.

2. <img width="1326" height="277" alt="Cyber_HW3_2 8part1step2" src="https://github.com/user-attachments/assets/a686fad9-bd6b-4860-8916-2e275a0326c8" />
   The attack won't work. Why its because execve() doesn't invoke shell. It executes /bin/cat exactly with argv[1] passed as argument.

## Task 9

<img width="1311" height="543" alt="Cyber_HW3_2 9" src="https://github.com/user-attachments/assets/1e76073c-52d4-46ac-968d-a0463d19eeaa" />
Created a tmp for the code to find the find when ran and then printed out “I am under the water!” then use the cat command to print out what is being printed as I initialized before it was read in the /etc/zzz file.
