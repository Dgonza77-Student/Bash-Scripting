# Bash Scripting

## Objective

The goal of this project is to practice Bash scripting by creating a script that generates a specified number of empty files in a given directory. Each file is named sequentially following a naming format specified by the user (e.g., `myfile1`, `myfile2`, etc.).


### Skills Learned

- Improved understanding of Bash scripting.
- Enhanced ability to work with loops and user input.
- Practical use of the `touch` command to create files.
- Improved understanding of file permissions using `chmod`.
  
### Tools Used

- Oracle VM Virtual Box
- Linux
- Vim
- Bash

## Features

- Prompts the user for input to specify the file prefix and the number of files to create.
- Automatically generates files using the specified prefix and a sequential number.
- Utilizes loops to create multiple files efficiently.
  
## Script Breakdown

**Step 1.) Create the Bash script**

I created the file using Vim by running the command vim (Filename).sh


**Step 2.) Script content**

The file automation script is designed to run by prompting the user to provide the first part of the file name (a prefix) and the number of files to create. 
This is done with the lines
**echo "Enter the first part of the file name:"**

**read prefix**   - this sets prefix as the variable to hold whatever input is listed in the above prompt. We could also have done **read -p "Enter the first part of the file name" prefix**

and 

**echo "Enter the number of files you want to create: "**

**read num_files**

Next we utilize a for loop to iterate and create the files using the "touch" command.
This is done with the lines

**for ((i=1; i<=num_files; i++))**  - Iterates until a set limit input by the user

**do**

   **touch "${prefix}${i}"**  -  Creates file with prefix and sequential number**
   
**done**


Lastly to display a completion of the automated task, we have bash output the following
**echo "$num_files files created with prefix '$prefix'"** with $num_files and $prefix calling from variables


**CODE:**

![image](https://github.com/user-attachments/assets/0fa39ba3-37b6-4fbc-af14-903a863eff3e)



**Step 3.) Running the script**

To run the script we ensure we change the permissions to 755 via chmod 755 (filename)

**Example output**

![image](https://github.com/user-attachments/assets/7aeb1543-dadb-4b11-becb-38987cb37ce1)

