# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
# Exercise 1: Basic Directory and File Operations

# Create a directory named "my-folder"

<img width="398" height="48" alt="Screenshot 2026-05-28 085901" src="https://github.com/user-attachments/assets/74a17fee-c6e9-4443-b85d-e030a6d3d613" />




# Remove the directory "my-folder"

<img width="383" height="25" alt="Screenshot 2026-05-28 085921" src="https://github.com/user-attachments/assets/c50f7d9a-d3ec-48ed-bd6f-75b8eb1b0e6b" />




# Create the file Rose.txt

<img width="627" height="401" alt="Screenshot 2026-05-28 085943" src="https://github.com/user-attachments/assets/2772b92c-0327-479a-a14f-84fb52941484" />




# Create the file hello.txt using echo and redirection

<img width="546" height="97" alt="Screenshot 2026-05-28 090003" src="https://github.com/user-attachments/assets/1a990c70-e2e1-426a-ac8f-095eba9d54db" />





# Copy the file hello.txt into the file hello1.txt

<img width="516" height="195" alt="Screenshot 2026-05-28 090044" src="https://github.com/user-attachments/assets/f50ff1a2-681a-407a-8122-73a326143804" />




# Remove the file hello1.txt

<img width="445" height="234" alt="Screenshot 2026-05-28 090107" src="https://github.com/user-attachments/assets/fdf0015a-9af9-47a4-9581-0cf1f76bf94d" />





# List out all the associated file extensions 

<img width="638" height="1033" alt="Screenshot 2026-05-28 090713" src="https://github.com/user-attachments/assets/1f01b95e-1583-4c2c-a9cd-9d7d8527dfe4" />





# Compare the file hello.txt and rose.txt

<img width="507" height="251" alt="Screenshot 2026-05-28 090730" src="https://github.com/user-attachments/assets/713652f6-5673-4dc8-b5b2-27d0e3412ee2" />




# Exercise 2: Advanced Batch Scripting
## Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".





# PROGRAM AND OUTPUT
```
@echo off
set name=John
echo Hello, %name%!
pause

```

<img width="391" height="82" alt="Screenshot 2026-05-28 090848" src="https://github.com/user-attachments/assets/a3b86471-9eea-4bee-ba3f-5a76912e90cb" />




### Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
### Prompt the user to enter a number.
### Calculate the remainder when the number is divided by 2.
### Display whether the number is odd or not.
### Ask the user if they want to check another number.
### Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
### Handle invalid inputs for the continuation prompt (Y/N) gracefully.




## PROGRAM AND OUTPUT

```
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause


```

<img width="563" height="218" alt="Screenshot 2026-05-28 090831" src="https://github.com/user-attachments/assets/35b68041-2d5d-4967-8636-fef9073d84f8" />





## Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.




## PROGRAM AND OUTPUT
```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause

```
<img width="399" height="184" alt="Screenshot 2026-05-28 090900" src="https://github.com/user-attachments/assets/525d6c53-2587-4746-bd8e-d0b708a2a53c" />






## Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

#### Instructions:
#### Use the IF EXIST conditional statement.
#### Make sure the script works for files located in the same directory as the batch file.
#### Use pause to keep the command window open after displaying the message.
#### Expected Output (if the file exists):

## PROGRAM AND OUTPUT
```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
s
```

<img width="457" height="222" alt="Screenshot 2026-05-28 090933" src="https://github.com/user-attachments/assets/c8a59278-bc08-46e3-b804-b8251b6ceacb" />


### Write a batch script that displays a simple menu with three options:
### ay Hello – Displays the message Hello, World!
### Create a File – Creates a file named newfile.txt with the content This is a new file
### Exit – Exits the script with a goodbye message
### The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.


## PROGRAM AND OUTPUT
```
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 
if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu
:end
echo Goodbye!
pause

```
<img width="560" height="485" alt="Screenshot 2026-05-28 090947" src="https://github.com/user-attachments/assets/b9267383-0f43-41a6-a4d1-db4af1efe3be" />




# RESULT:
The commands/batch files are executed successfully.

