
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
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT
<img width="677" height="87" alt="image1" src="https://github.com/user-attachments/assets/359c6c2c-d57e-4b0f-9c83-b259a98dca74" />

Remove the directory "my-folder"

## COMMAND AND OUTPUT
<img width="717" height="75" alt="image2" src="https://github.com/user-attachments/assets/14bda17d-a0c3-4a24-94a4-3204505d9104" />



Create the file Rose.txt

## COMMAND AND OUTPUT

<img width="766" height="67" alt="image3" src="https://github.com/user-attachments/assets/8bdfb841-dc02-4529-8652-6d04190dee78" />




Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT

<img width="638" height="77" alt="image4" src="https://github.com/user-attachments/assets/e5e9a077-be95-405d-910a-b89944c4e78a" />

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT

<img width="622" height="95" alt="image5" src="https://github.com/user-attachments/assets/72b548d2-aa79-4947-9481-864cbb50b211" />

Remove the file hello1.txt

## COMMAND AND OUTPUT

<img width="418" height="67" alt="image6" src="https://github.com/user-attachments/assets/2f0bc644-a473-4e7d-b622-6a6d865aa6e0" />


List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT


<img width="606" height="172" alt="image7" src="https://github.com/user-attachments/assets/3f7313a8-c64c-45a5-90ab-b02d226c2115" />

List out all the associated file extensions 

## COMMAND AND OUTPUT


<img width="717" height="906" alt="image8" src="https://github.com/user-attachments/assets/f358bfc0-95dd-4f94-9daf-65fe08962146" />

<img width="886" height="137" alt="image9" src="https://github.com/user-attachments/assets/aaf00e97-b6bf-4b58-94c0-a39e91a271fd" />

<img width="861" height="1087" alt="image10" src="https://github.com/user-attachments/assets/844091b7-395e-4834-97f0-af9f6da41b80" />

<img width="912" height="1086" alt="image11" src="https://github.com/user-attachments/assets/3e864d82-4653-4a9d-a1d3-f27fdaf3b2b0" />

<img width="777" height="1088" alt="image12" src="https://github.com/user-attachments/assets/c9a6f254-4422-48e2-aae3-5fcb3b2a984f" />

<img width="743" height="1089" alt="image13" src="https://github.com/user-attachments/assets/fcb188bd-1899-4a44-b88e-459f4a805a5d" />

<img width="962" height="1084" alt="image14" src="https://github.com/user-attachments/assets/f91909b8-2cb7-487e-96d4-4affb7c68277" />

<img width="1028" height="1098" alt="image15" src="https://github.com/user-attachments/assets/bc5dbcea-a24f-47e5-8a8a-91e7323cc9bc" />


<img width="758" height="1087" alt="image16" src="https://github.com/user-attachments/assets/17ec7e0d-a2ed-4f30-b1af-1bcbb7238c57" />



Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT

<img width="562" height="153" alt="image17" src="https://github.com/user-attachments/assets/ee779e91-5fd9-4134-b760-7376503f5a9c" />

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

## BATCH PROGRAM
```c
@echo off
set name=John
echo Hello, %name%
pause

```



## OUTPUT

<img width="471" height="131" alt="image18" src="https://github.com/user-attachments/assets/f6b197e1-94d0-4c9c-ae84-6b34cb322ddb" />


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

## BATCH PROGRAM
```c
@echo off
:loop
set /p num=Enter a number: 
set /a rem=%num% %% 2

if %rem%==0 (
    echo %num% is Even
) else (
    echo %num% is Odd
)

:ask
set /p ans=Do you want to check another number? (Y/N): 
if /I "%ans%"=="Y" goto loop
if /I "%ans%"=="N" goto end
echo Invalid input. Please enter Y or N.
goto ask

:end
echo Thank you!
pause

```

## OUTPUT

<img width="688" height="241" alt="image19" src="https://github.com/user-attachments/assets/4c809dd8-0564-4b66-9c04-47b2457b35eb" />



Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

## BATCH PROGRAM
```^c
@echo off
for /L %%i in (1,1,5) do (
    echo Number: %%i
)
pause
```





## OUTPUT
<img width="831" height="261" alt="image20" src="https://github.com/user-attachments/assets/2ff049d5-cf83-41aa-bc8b-3c0e3e58ae95" />




Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

## BATCH PROGRAM
```c
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause

```

## OUTPUT
<img width="599" height="93" alt="image21" src="https://github.com/user-attachments/assets/0912ebb5-4d61-4afa-858d-a4c164fdfd47" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

## BATCH PROGRAM
```c
@echo off
:menu
cls
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option (1-3): 

if "%choice%"=="1" goto hello
if "%choice%"=="2" goto create
if "%choice%"=="3" goto exit
echo Invalid choice.
pause
goto menu

:hello
echo Hello, World!
pause
goto menu

:create
echo This is a new file > newfile.txt
echo File newfile.txt created.
pause
goto menu

:exit
echo Goodbye!
pause
exit


```

## OUTPUT
<img width="411" height="147" alt="image22" src="https://github.com/user-attachments/assets/04f453a2-65f4-4b59-acf1-3667c468a17b" />

<img width="742" height="242" alt="image23" src="https://github.com/user-attachments/assets/92faa7f9-dfc6-4bf1-a43c-05f52a255c74" />

<img width="643" height="171" alt="image24" src="https://github.com/user-attachments/assets/9ed12f8c-2312-4c24-913f-ff458a97b940" />

# RESULT:
The commands/batch files are executed successfully.

