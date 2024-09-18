# Bash Scripting

## Objective

The goal of this project is to gain familiarity with Bash scripting by creating a simple command line calculator

### Skills Learned


- Improved understanding of Bash scripting.
- Enhanced problem-solving through script automation.
- Development of basic command-line tools.y.

### Tools Used


- Oracle VM Virtual Box
- Linux
- Vim
- Bash
  
## Features
This calculator performs basic arithmetic operations such as:
- Addition
- Subtraction
- Multiplication
- Division
  
## Script Breakdown

**Step 1.) Create the Bash script**
In order to create the script, I used Vim to create the file by running the command "vim calc_test.sh". Like all scripts the first line must be #!/bin/bash

**Step 2.) Script content**

![image](https://github.com/user-attachments/assets/d0b66e40-40e0-44b2-9c38-ad90af56c7d8)

The script (posted above) prompts the user for two numbers, assigns the responses as num1 and num2 and then performs basic mathematical operations on them

**Step 3.) Running the script**
After saving my script by pressing esc followed by "w:" and "x:", I had to make sure that I had the proper permissions to run the script.
To do so I used chmod 755 (script name) to gain the proper permissions needed. 7 means the owner of the file can read,write and execute, 5 means group members can read and execute but NOT write and the other 5 means that other users can also read and execute but not modify.
To execute the script I used the command "./calc_test.sh"

**Example output**

![image](https://github.com/user-attachments/assets/5938517a-1c73-4f77-b3be-295a57d3bae3)


**Permissions breakdown**
### Visual Representation

You can visualize `755` like this:

|         | Read (4) | Write (2) | Execute (1) |
|---------|----------|-----------|-------------|
| **Owner**  | Yes      | Yes       | Yes         |
| **Group**  | Yes      | No        | Yes         |
| **Others** | Yes      | No        | Yes         |
