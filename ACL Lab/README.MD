# SEE acl.pdf lab manual for specific objective details for the solutions below

This exercise explores the use of Linux ACLs to provide access control over files, with more flexibility
than the access control offered by traditional UNIX file permissions.

To accomplish the objectives of this lab, the getfacl and setfacl commands were used to view and change the ACLs on the lab files.
Full details on the Linux ACL can be viewed here: https://wiki.archlinux.org/index.php/Access_Control_Lists

## 4.2 Task 2: Set an ACL on a single file

The "+" on a file's permissions designates that the file has additional ACL permissions assigned to it alongside the traditional UNIX permissions. 

After logging into the terminals as bob, alice, and harry, the setfacl command was ran to allow alice to read the /shared_data/bob/bobstuff.txt file. Harry should not be able to read bobstuff.txt after the file permission change

![setfacl_alice_bobstuff](https://github.com/user-attachments/assets/e727e0de-398d-4f63-8df1-23ea504c4afa)

![setfacl_alice_bobstuff2](https://github.com/user-attachments/assets/c8e0a8b0-96b0-4253-a123-69598bc294b6)

Alice able to read bobstuff.txt after updating LINUX ACLs

![alice_reads_bobstuff](https://github.com/user-attachments/assets/c08baa99-255e-411e-971e-cd6481669bab)

Harry still not able to read bobstuff.txt

![harry_notable_toread_bobstuff](https://github.com/user-attachments/assets/1e52a0c5-e06c-46d4-9930-40d31d3c9742)


## 4.3 Task 2: Set an default ACL for a directory

Bob needs to have read permissions on alice's folder by default. This will allow bob to view any newly created files in the 'alice' folder. This can be achieved by using the setfacl command:

setfacl command to give bob default permissions

![setfacl_bob_default_alice](https://github.com/user-attachments/assets/a27bae74-fbac-44b4-9c74-3b3c5ac21b89)

default permissions established for bob

![getfacl_bob_default_alice](https://github.com/user-attachments/assets/9af8cd36-01df-4154-bc42-59e2ce9de1ff)


## 4.4 Task 3: Trojan Horses

To accomplish this task, I updated the 'fun' file in bob's folder to copy the accounting.txt file to /shared_data/bob/acctbob1.txt when alice or harry run bob's 'fun' script. 
This is a sneaky attempt to get access to information that bob would not normally be authorized to view. 
