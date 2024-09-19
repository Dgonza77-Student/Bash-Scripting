# Bash Scripting

## Objective

The goal of this project is to create a script that generates a specific directory structure within a directory specified by the user. The user can supply the directory as an argument when running the script. If no argument is provided, the script will prompt the user for a directory location.

### Skills Learned

- Improved understanding of Bash script functions.
- Practical experience with the `mkdir` command for creating directories.
- Using conditional statements (`if`, `else`) to handle user input.
- Working with arguments passed to a script and prompting for input when necessary.

### Tools Used

- Oracle VM Virtual Box
- Linux
- Vim
- Bash
  
## Features

- The script allows the user to create a structured set of directories, including subdirectories.
- If the user provides a directory as an argument, the structure will be created in that location.
- If no argument is given, the script prompts the user for input.
  
## Script Breakdown

### **Step 1: Create the Bash Script**
Used vim to create the script via vim (filename).sh. Per usual, the first line of any bash script must be #!/bin/bash to indicate that the program will be interpreting the bash shell.

### **Step 2: Script Content**
The script is written in a manner that will first check to see that an argument for the directory path is supplied. If there is no argument, the script will prompt the user to enter a directory. 


**if [ -z "$1" ]; then  # $1 refers to the first argument passed to the script**

**echo "No directory provided. Please enter the directory where you want to create the structure:"**

  **read dir  # If no argument, ask the user for input**

**else**

  **dir=$1  # If argument is provided, use it as the directory**
    
**fi**

Following the above code, I created a function called "structure_create()" that will create a directory structure for the user

**structure_create() {**

  **mkdir -p "$dir/Data/Image/Cache"  # Create the directory and subdirectories**

  **echo "Structure for directory created at: $dir"**

**}**

**CODE:**

![image](https://github.com/user-attachments/assets/a7eeebdd-4f51-403e-931b-ba780d5d53b4)


### **Step 3: Running the Script**
In order to ensure we have the proper permissions we do chmod 755 (filename).sh

Then we run the command with ./create_structure.sh


### **Output**

![image](https://github.com/user-attachments/assets/ed347581-46bb-4b1a-80d1-8899b5d0fba1)
