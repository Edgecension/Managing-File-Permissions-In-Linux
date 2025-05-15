# Managing File Permissions In Linux

## Project Description  
An organization needs to update file permissions for certain files and directories within the *projects* directory. The permissions do not currently reflect the level of
authorization that should be given. Checking and updating these permissions will help ensure a secure system. Here are the following steps in completing this task:

## File Check and Directory Details
The following code demonstrates how Linux commands are used to determine the existing permissions set for a specific directory in the file system.
<img width="612" alt="Screenshot 2025-05-15 at 12 58 13 PM" src="https://github.com/user-attachments/assets/dee5c614-239c-49f7-b240-b1ae0ccab411" />

The first line of the screenshot displays the command entered, and the other lines display the output. The code lists all contents of the projects directory. The **ls** command with the **-la** option to display a detailed listing of the file contents that also returned hidden files. The output of the command indicates that there is one directory named **drafts**, one hidden file named **.project_x.txt** and five other project files. The 10-character string in the first column represents the permissions set on each file or directory.

## Permissions String Description
The 10-character string can be deconstructed to determine who is authorized to access the file and their specific permissions. The characters and what they represent are as follows:

- **1st Character:** This character is either **a d or hyphen (-)** and indicates the file type. If it’s **a d**, it’s a directory. If it’s a **hyphen (-)**, it’s a regular
file.
- **2nd-4th Characters:** These characters indicate the **read (r), write (w)**, and **execute (x)** permissions for the user. When one of these characters is a **hyphen (-)** instead, it indicates that this permission is not granted to the user.
- **5th-7th Characters:** These characters indicate the **read (r), write (w)**, and **execute (x)** permissions for the group. When one of these characters is a **hyphen (-)** instead, it indicates that this permission is not granted for the group.
- **8th-10th Characters:** These characters indicate the **read (r), write (w)**, and **execute (x)** permissions for other. This owner type consists of all other users on the system apart from the user and the group. When one of these characters is a **hyphen (-)** instead, that indicates that this permission is not granted for other.

For example, the file permissions for **project_t.txt** are **-rw-rw-r--**. Since the first character is a **hyphen (-)**, this indicates that **project_t.txt** is a file, not a directory. The second, fifth, and eighth characters are all **r**, which indicates that user, group, and other all have read permissions. The third and sixth characters are **w**, which indicates that only the user and group have write permissions. No one has execute permissions for **project_t.txt**.

## Change File Permissions
<img width="612" alt="Screenshot 2025-05-15 at 1 14 16 PM" src="https://github.com/user-attachments/assets/c975c914-b593-499b-b5ce-f17b222e8440" />

The first two lines of the screenshot display the commands I've entered, and the other lines display the output of the second command. The **chmod** command changes the permissions on files and directories. The first argument indicates what permissions should be changed, and the second argument specifies the file or directory. In this example, I removed write permissions from other for the **project_k.txt** file. After this, I used **ls -la** to review the updates I made.


## Change File Permissions On Hidden File
<img width="611" alt="Screenshot 2025-05-15 at 1 25 32 PM" src="https://github.com/user-attachments/assets/3a493a7d-9228-4e33-a3c9-c54cfb53217b" />


