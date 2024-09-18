# Bash Scripting

## Objective

Practice and gain familiarity with the concept of iteration in Bash.

### Skills Learned
- Improved understanding of user input handling in Bash.
- Enhanced ability to implement control flow structures (loops and conditions) in scripts.
- Handling default values in user input scenarios.

### Tools Used
- Oracle VM Virtual Box
- Linux
- Vim
- Bash

## Features
- Prompts the user to input an integer value.
- If no input is provided, it defaults to 10.
- Uses a loop to display numbers from 1 to the user-inputted number.
  
## Script Breakdown

**Step 1.) Create the Bash script**

I created the file much the same to any other, "vim (filename).sh"

**Step 2.) Script content**

The content of the script, as seen below, was to practice the concept of Iteration. Iteration is a concept we see universally throughout every programming language.
First off I started with #!/bin/bash which all bash scripts demand as the first line, following by a simple explanation of what the script is in order to follow basic programming ettiquette 

The first chunk recieves the users input and sets a variable. This is done with the line

**read -p "Enter a number(Default is 10): " num**

In bash the read command is used to take input from the user and the -p command it tacked ontop to display a prompt message before a value is inputed

The next chunk of code practices a simple if statement in bash

**if [ -z "$num" ]; then
          num=10 
fi**

in other programming languages, like java, operators such as != and == would mean not equal to or equal to. In bash these operators also exist but additional specific test operators such as -z can be used.
In the above code -z is used to see is a string is empty/no input. Above its simply saying "If there is no input for the variable num, then num will equal 10."



Moving forward we have the main chunk of the script, the iteration.
The code reads as follows

**for (( i=1; i<=num; i++ ))
do 
        echo $i
done**

The above line of code reads as a simple iteration statement that essentially has the code add a value to whatever input is given. If the user inputs nothing then the program will continue to iterate until it reaches 10 (assuming no input is given). It knows to stop at 10 because of the i<=num 
which reads as if i is less than or equal to num (10) then add. But if i no longer meets the criteria of being <= to 10 then stop.

**Step 3.) Running the script**

To run the script I saved the file and changed the permission to 755 following by the command "./(filename).sh"

**Example output**

![image](https://github.com/user-attachments/assets/c810f650-06b4-4024-b185-8b16dda724d7)




**Permissions breakdown**
### Visual Representation of Iteration
| Step   | i Value | Condition (`i <= num`) | Action           | Output (if num=3) |
|--------|---------|------------------------|------------------|-------------------|
| Step 1 | 1       | True                   | Run the command  | 1                 |
| Step 2 | 2       | True                   | Run the command  | 2                 |
| Step 3 | 3       | True                   | Run the command  | 3                 |
| Step 4 | 4       | False (end loop)        | Exit the loop    | (none)            |
