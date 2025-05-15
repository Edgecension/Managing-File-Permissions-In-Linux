# Managing File Permissions In Linux

## Project Description  
Update file permissions for certain files and directories within the projects directory. The permissions do not currently reflect the level of
authorization that should be given. Checking and updating these permissions will help ensure a secure system. Here are the following steps in completing this task:
## File Check and Directory Details
<img width="612" alt="Screenshot 2025-05-15 at 12 58 13 PM" src="https://github.com/user-attachments/assets/dee5c614-239c-49f7-b240-b1ae0ccab411" />

The first line of the screenshot displays the command entered, and the other lines display the output. The code lists all contents of the projects directory. The ls command with the -la option to display a detailed listing of the file contents that also returned hidden files. The output of the command indicates that there is one directory named drafts, one hidden file named .project_x.txt and five other project files. The 10-character string in the first column represents the permissions set on each file or directory.
## Permissions String Description
The 10-character string can be deconstructed to determine who is authorized to access the file and their specific permissions. The characters and what they represent are as follows:
● 1st character: This character is either a d or hyphen (-) and indicates the file type. If it’s a d, it’s a directory. If it’s a hyphen (-), it’s a regular
le.
