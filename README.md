Practical 01: Writing a Batch Script to Create Directory Structure

Objective:
This exercise aims to develop a batch script that automatically creates a structured set of folders based on specific criteria and standards.

Requirements:
     -A text editor (such as Notepad++, Visual Studio Code, or Notepad).
     -Basic knowledge of Windows batch scripting and file organization.
     -A Windows operating system.

Instructions to Create the Batch Script
1. Launch a Text Editor
Open any text editor of your choice. (We used Notepad++.)
3. Enter the Script
    Type the following code:
     mkdir criteria_1
cd criteria_1
mkdir standard_1
mkdir standard_2
cd..
mkdir criteria_2
cd criteria_2
mkdir standard_1
mkdir standard_2
cd..
mkdir criteria_3
cd criteria_3
mkdir standard_1
mkdir standard_2
mkdir standard_3
cd..
mkdir criteria_4
cd criteria_4
mkdir standard_1
mkdir standard_2
mkdir standard_3
cd..
mkdir criteria_5
cd criteria_5
mkdir standard_1
mkdir standard_2
mkdir standard_3
cd..
mkdir criteria_6
cd criteria_6
mkdir standard_1
mkdir standard_2
mkdir standard_3

How to Run the Batch Script
  1. Save the File
      Save the document with a .bat extension, for example, create_folders.bat.
  2. Execute the File
       -Find the .bat file in File Explorer.
       -Double-click to run it.
       -The folder structure will be created where the file is located

Commands Explained
      mkdir – Makes new folders.
      cd – Changes the working directory.
      @echo off – Hides command lines from displaying during execution.

Summary
     In this task, we learned to automate the setup of a well-organized folder structure. This method ensures consistent directory arrangements, saving time and improving project organization.

..........................................................................................................................................................................................................................................

Practical 02: Writing a Batch Script to Calculate Age

Objective
The goal is to create a batch script that asks for the user’s birth year and calculates their current age using the system’s date.
    
Steps to Create the Script
1. Open a Text Editor
 Use any simple text editor (e.g., Notepad++, VS Code).
2. Write the Following Script
Type the code below:
               @echo off
                  for /f "tokens=2 delims==" %%i in ('wmic os get localdatetime /value') do set datetime=%%i
                  set current_year=%datetime:~0,4%
                  set /p birth_year=Please enter your birth year:
                  set /a age=%current_year% - %birth_year%
                  echo You are %age% years old.
                  pause

                  
      
![1](https://github.com/user-attachments/assets/e19fd5c3-ad50-45fb-87cf-c4e6de241c4a)

 Running the Script
1. Save the File
            Save the document with a .bat extension, for example, calculate_age.bat.
2. Execute the Script
            Locate the file through File Explorer.
            Double-click to open and run it.
            Enter your birth year when prompted to see your age displayed.

            
Script Explanation
echo off – Suppresses command echoing for a cleaner look.
set /p birth_year=... – Prompts the user to input their birth year.
%date:~10,4% – Extracts the current year from the system date.
set /a age=... – Calculates the difference between the current year and birth year.
echo – Prints the output.
pause – Waits for user input before closing the window.

Summary
In this activity, we created a basic batch script to interact with the user, perform a simple calculation, and display the result. We practiced using essential commands like set, echo, and pause in Windows batch scripting.

