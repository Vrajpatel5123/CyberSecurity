# Lab 1

## General System Tasks:

1.  Open the terminal in your Virtual Machine (VM). Enter the command to retrieve
    available updates.

        sudo apt update
        Basically showing things that can be updated

    <img width="937" height="776" alt="CyberSecurity_lab1_p1" src="https://github.com/user-attachments/assets/e5f9b866-7b50-45b0-b488-9c9b3ff38214" />

2.  Upgrade your system.
    Already did that once I using the command line for update. Upgrading the system that it will upgrade after entering the command line.
    <img width="971" height="867" alt="CyberSecurity_lab1_upgrade" src="https://github.com/user-attachments/assets/f7ddef5d-9dee-4281-9a0c-4cc7d553485f" />

3.  Reboot your system.
    It says it as its asked. Reboot!
    Reboots the system like a restart.
    AKA sudo reboot

## User Tasks:

1. The prompt went away from bash (originally in Linux). Now, it's in shell terminal. (I Believe)
   <img width="987" height="98" alt="CyberSecurity_lab1_root" src="https://github.com/user-attachments/assets/7c8cf948-bf11-42df-bc10-0b2595aa8000" />

2. The "Useradd" is just user which it doesn't create a password for the user. Unlike adduser is different
   due to having the ability to create a password for the user.
   <img width="952" height="422" alt="CyberSecurity_lab1_add_useradd" src="https://github.com/user-attachments/assets/26d3eecd-c98b-419b-b560-642053d74e5e" />

3. When I changed to user sally, it changed from shell terminal to bash terminal as the user sally.
   <img width="968" height="47" alt="CyberSecurity_lab1_change_user" src="https://github.com/user-attachments/assets/4dc94fac-5754-4be6-a061-a4f63996d51b" />

4. I wasn't able to create a user name earl due to sally not like user with an ability like root would have. You can fix it by making this change: "usermod -aG sudo sally" to give her the ability to create user.

<img width="972" height="71" alt="CyberSecurity_lab1_add_userEarl" src="https://github.com/user-attachments/assets/6579450c-54fa-436a-a16a-2ebf3c0be9a7" />

5. The command for delete user is sudo userdel -r "username". Basically delete the user in short.
   <img width="955" height="67" alt="CyberSecurity_lab1_remove_user" src="https://github.com/user-attachments/assets/c7ef7c72-4866-44ff-855b-53434f178b6b" />

6. It just as in the beginning when adding a user with a password and now adding a new password.
   <img width="992" height="77" alt="CyberSecurity_lab1_newpasswd_sally" src="https://github.com/user-attachments/assets/d0024501-ecc4-4b4b-a4ca-737175845c4c" />

7. It's a bad practice to stay logged in as a root due to have the ability to changed any files or worse execute it without a records left behind who changed who. It would be seen as just root not the actually person that made the changes.

8. User id is showing what id number the root is aka patelvraj-007 and others like group and etc.
   <img width="1012" height="56" alt="CyberSecurity_lab1_id" src="https://github.com/user-attachments/assets/eca32c7e-82b2-4361-a11b-f77c3174cea6" />

## Group tasks:

1. I don't quite get what its specifically asking. I believe as of now nothing but the group I created is cybersec.

2. I use chmod due to giving the ability for sally that doesn't have the sudo privillege. After I made the change, now she has the sudo privillege to create user.
   <img width="962" height="263" alt="CyberSecurity_lab1_changeMod" src="https://github.com/user-attachments/assets/e57dc745-5e23-4b69-bd4e-d71a8d27ea03" />

3. Its basically creating a group for everyone to be in after adding them. It make it more smoother than manually showing who is doing what in main.
   <img width="958" height="23" alt="CyberSecurity_lab1_createGroup" src="https://github.com/user-attachments/assets/38c3dba0-0396-4cc3-a105-451518fe6923" />

4. Using the code usermod -a -G to add sally to groupsec. Of course it has to be by the root aka patelvraj-007.
   <img width="976" height="20" alt="CyberSecurity_lab1_addSally_group" src="https://github.com/user-attachments/assets/9c19cb77-e78a-4c26-a257-2071046fe0b3" />

5. Many ways, main is typing in groups under the user it shows in the terminal. Another is by id. And last is by grep seed /etc/group
   <img width="996" height="202" alt="CyberSecurity_lab1_manywaytocheckgroup" src="https://github.com/user-attachments/assets/7e142608-8e81-4609-b71a-dba78bc44c1d" />

## Permission and Access Control Lists:

1. The owner of directory of lab1 is patelvraj-007 and group is also patelvraj-007. The permission the owner has write, execute,& read and the group has same as the owner in this case.
   <img width="966" height="382" alt="CyberSecurity_lab1_makedir" src="https://github.com/user-attachments/assets/1d8df2ee-3e64-490c-988c-dece54ab5816" />

2. Create a file is command called touch and to type in the file is nano. Then to execute have to change it to having execute permission aka chmod. To print out"Hello World!". It is echo instead of print.
   <img width="953" height="162" alt="CyberSecurity_lab1_createfilebash" src="https://github.com/user-attachments/assets/3e254ced-c2a9-416b-be1b-bde65a5f2e89" />

   <img width="956" height="93" alt="CyberSecurity_lab1_change_groupPermission" src="https://github.com/user-attachments/assets/8fb75ab4-4481-4151-8fd4-fc50f6f01f8b" />

3. The owner has read, write and execute permissions. The group has read and write permissions.
   a. I wrote chmod 770 helloWorld. That was able to change the permission for the group to now being able to read, write and execute. Also, getfacl means get file access control lists.

    <img width="950" height="127" alt="CyberSecurity_lab1_setfacl" src="https://github.com/user-attachments/assets/d0dbbedb-8932-4db9-beff-b2503933f3e6" />

4. setfacl is set file access control lists. In order to do that have to made "-m" then u (user) : name of the user: (the three permission like rwx) file name.  
   <img width="946" height="195" alt="CyberSecurity_lab1_setfacl_sally_rw" src="https://github.com/user-attachments/assets/71290fc6-e098-485e-beac-78bdaac7ffae" />
