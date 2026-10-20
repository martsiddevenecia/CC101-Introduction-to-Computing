# CC 101 Laboratory Activity: Exploring the Windows Command Line

**Republic of the Philippines**  
**Sorsogon State University**  
**College of Information and Communications Technology — Bulan Campus**  
Zone 8, Bulan, Sorsogon  
Tel. No.: 056 311-0103 | Email Address: cict@sorsu.edu.ph  

---

## Student & Course Information

| Field | Details |
| :--- | :--- |
| **Student Name** | Mart Sid Dorado De Venecia |
| **Student ID** | 26117109 |
| **Program & Section** | BSCS 1-1 |
| **Date Performed** | September 23, 2026 |
| **Professor** | John Mark D. Gabrentina |
| **Course** | CC 101 Introduction to Computing (BSCS 1st Year) |
| **Course Outcome** | CO2: Identify the functions and relationships of major hardware and software components |
| **Output** | Command Line Exploration Documentation |
| **Estimated Time** | 2 to $2\frac{1}{2}$ hours |
| **Reference** | CC 101 Lecture Notes: Exploring the Windows Command Line |

---

## Introduction

The command line is a text-based interface that allows the users to configure the computer's operating system by typing specific commands instead of clicking visual icons. The purpose of this activity was for us to experience first-hand both the Windows Command Prompt and PowerShell to perform basic file management tasks. By completing these exercises, we were able to learn a little on how to manipulate files, view system configurations, and understand the core differences between command-line operations and the traditional graphical user interface.

---

## Instructions

Follow every step in order, take the screenshots marked **[Screenshot]**, and answer the questions marked **[Answer]** in your documentation.

### Before You Start
* You need a Windows 10 or 11 computer. No administrator rights are needed.
* To take a screenshot, press `Windows + Shift + S`, drag over the terminal window, then paste it (`Ctrl + V`) into your documentation.
* Replace the sample values (`Juan Dela Cruz, BSCS 1-1`) with your own details.
* Type every command yourself. Do not copy and paste; typing is how you learn.

---

## Part A: Open the Two Shells

1. Press `Windows + R`, type `cmd`, and press **Enter**. Type `cls` and press **Enter**.
2. Type `echo Juan Dela Cruz, BSCS 1-1` (your own name and section) and press **Enter**.

### [Screenshot] Figure A1: Command Prompt `echo` Output
*Optional image path for repository:* `![Figure A1](screenshots/Figure_A1.png)`

~~~cmd
C:\Users\Mhax>echo Mart Sid De Venecia, BSCS 1-1
Mart Sid De Venecia, BSCS 1-1

C:\Users\Mhax>
~~~

3. Press `Windows + R`, type `powershell`, and press **Enter**. Type the same `echo` command, but put the text in quotation marks: `echo "Juan Dela Cruz, BSCS 1-1"`. PowerShell treats the comma as a list separator without them.

### [Screenshot] Figure A2: PowerShell `echo` Output
*Optional image path for repository:* `![Figure A2](screenshots/Figure_A2.png)`

~~~powershell
Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

PS C:\Users\Mhax> echo "Mart Sid De Venecia, BSCS 1-1"
Mart Sid De Venecia, BSCS 1-1
PS C:\Users\Mhax>
~~~

### [Answer] A-Q1
**Compare the two prompts. What is different, and what does each part of the Command Prompt prompt mean?**

> Just by looking at the two prompts, the `cmd` prompt starts with drive `C`, while the PowerShell prompt starts with `PS` which stands for PowerShell. We can also notice that after the greater-than symbol (`>`) on each prompt, the PowerShell gives a single "space" before the input, while the `cmd` doesn't. For me, having a space before the input makes it cleaner and easier to understand.

---

## Part B: Inspect Your System (Command Prompt)

*Use the Command Prompt window for Parts B to D.*

1. Run these commands one at a time: `whoami`, then `hostname`, then `ver`.

### [Screenshot] Figure B1: `whoami`, `hostname`, and `ver` Output
*Optional image path for repository:* `![Figure B1](screenshots/Figure_B1.png)`

~~~cmd
C:\Users\Mhax>whoami
atomic\hizashi mhast

C:\Users\Mhax>hostname
ATOMIC

C:\Users\Mhax>ver

Microsoft Windows [Version 10.0.26200.9457]

C:\Users\Mhax>
~~~

2. Run the command below. It may take 10 to 30 seconds.

~~~cmd
systeminfo | findstr /B /C:"OS Name" /C:"OS Version" /C:"System Type" /C:"Total Physical Memory"
~~~

### [Screenshot] Figure B2: Filtered `systeminfo` Output
*Optional image path for repository:* `![Figure B2](screenshots/Figure_B2.png)`

~~~cmd
C:\Users\Mhax>systeminfo | findstr /B /C:"OS Name" /C:"OS Version" /C:"System Type" /C:"Total Physical Memory"
OS Name:                   Microsoft Windows 11 Home Single Language
OS Version:                10.0.26200 N/A Build 26200
System Type:               x64-based PC
Total Physical Memory:     7,916 MB

C:\Users\Mhax>
~~~

3. Run `ipconfig`. Find the adapter that shows an IPv4 Address.

### [Screenshot] Figure B3: `ipconfig` Output
*Optional image path for repository:* `![Figure B3](screenshots/Figure_B3.png)`

~~~cmd
C:\Users\Mhax>ipconfig

Windows IP Configuration


Wireless LAN adapter Local Area Connection* 1:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Wireless LAN adapter Local Area Connection* 2:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Wireless LAN adapter Wi-Fi:

   Connection-specific DNS Suffix  . :
   IPv6 Address. . . . . . . . . . . : 2405:8d40:4888:8b7a:29fb:7746:4d31:1d1b
   Temporary IPv6 Address. . . . . . : 2405:8d40:4888:8b7a:c90a:40f6:78c:43b5
   Link-local IPv6 Address . . . . . : fe80::83f:47d:d167:3d3f%16
   IPv4 Address. . . . . . . . . . . : 10.120.184.201
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Default Gateway . . . . . . . . . : fe80::acc6:4fff:fe4a:ea1d%16
                                       10.120.184.96

C:\Users\Mhax>
~~~

### [Answer] B-Q1
**Complete this table in your documentation using your results:**

| Item | Your Result |
| :--- | :--- |
| **Logged-in account (`whoami`)** | `atomic\hizashi mhast` |
| **Computer name (`hostname`)** | `ATOMIC` |
| **OS name** | Microsoft Windows 11 Home Single Language |
| **OS version** | 10.0.26200 N/A Build 26200 |
| **System type (x64 or ARM)** | x64-based PC |
| **Total physical memory (RAM)** | 7,916 MB |
| **IPv4 address** | 10.120.184.201 |

### [Answer] B-Q2
**The `|` symbol in step 2 is called a pipe. Run `systeminfo` alone and compare. In your own words, what did `| findstr` do?**

> When I ran `systeminfo` alone, it showed all information about the device's system. `| findstr` helped users to find specific information that he/she needed. In other words, we use `| findstr` to find only what we need, reducing the data that are shown, thus removing irrelevant or unneeded information.

---

## Part C: Build a Folder Structure

1. Go to your user folder and create the lab folders:

~~~cmd
cd %USERPROFILE%
mkdir CC101-Lab
cd CC101-Lab
mkdir Notes Projects Screenshots
~~~

2. Create a text file about yourself (use your own details):

~~~cmd
echo Name: Mart Sid De Venecia > profile.txt
echo Section: BSCS 1-1 >> profile.txt
echo Favorite app: Calculator >> profile.txt
type profile.txt
~~~

### [Screenshot] Figure C1: Folder Creation and `type profile.txt` Output
*Optional image path for repository:* `![Figure C1](screenshots/Figure_C1.png)`

~~~cmd
C:\Users\Mhax>cd %USERPROFILE%

C:\Users\Mhax>mkdir CC101-Lab

C:\Users\Mhax>cd CC101-Lab

C:\Users\Mhax\CC101-Lab>mkdir Notes Projects Screenshots

C:\Users\Mhax\CC101-Lab>echo Name: Mart Sid De Venecia > profile.txt

C:\Users\Mhax\CC101-Lab>echo Section: BSCS 1-1 >> profile.txt

C:\Users\Mhax\CC101-Lab>echo Favorite app: Calculator >> profile.txt

C:\Users\Mhax\CC101-Lab>type profile.txt
Name: Mart Sid De Venecia
Section: BSCS 1-1
Favorite app: Calculator

C:\Users\Mhax\CC101-Lab>
~~~

3. Run `tree /F` to display your folder structure.

### [Screenshot] Figure C2: `tree /F` Output
*Optional image path for repository:* `![Figure C2](screenshots/Figure_C2.png)`

~~~cmd
C:\Users\Mhax\CC101-Lab>tree /F
Folder PATH listing for volume Windows-SSD
Volume serial number is 08F9-ADBD
C:.
│   profile.txt
│
├───Notes
├───Projects
└───Screenshots

C:\Users\Mhax\CC101-Lab>
~~~

4. Open File Explorer, go to `C:\Users\(your account)\CC101-Lab`, and open `profile.txt` in Notepad.

### [Screenshot] Figure C3: File Explorer and Notepad Side by Side
*Optional image path for repository:* `![Figure C3](screenshots/Figure_C3.png)`

* **File Explorer (`C:\Users\Mhax\CC101-Lab`):** Shows folders `Notes`, `Projects`, `Screenshots`, and text document `profile.txt`.
* **Notepad (`profile.txt`):**
~~~text
Name: Mart Sid De Venecia
Section: BSCS 1-1
Favorite app: Calculator
~~~

### [Answer] C-Q1
**What would happen if you used `>` instead of `>>` in the second `echo` line? Test it on a new file (`test.txt`) and explain.**

> When I used `>` instead of `>>`, the first `echo` line was overwritten. It is because `>` clears or replaces the old text, resulting in the clearance of the first `echo` line while leaving only the second or the latest `echo` line that used `>`. On the other hand, `>>` keeps the old text and adds new text below it. It doesn't remove the old text; instead, it appends the new text to the older text, keeping both the first, second, and other lines if there are any.

---

## Part D: Copy, Rename, and Delete Files

Commands executed:

~~~cmd
copy profile.txt Notes\profile-copy.txt
cd Notes
ren profile-copy.txt about-me.txt
echo This file will be deleted > temp.txt
dir
del temp.txt
dir
cd ..
tree /F
~~~

### [Screenshot] Figure D1: From `copy` to the First `dir`
*Optional image path for repository:* `![Figure D1](screenshots/Figure_D1.png)`

~~~cmd
C:\Users\Mhax\CC101-Lab>copy profile.txt Notes\profile-copy.txt
        1 file(s) copied.

C:\Users\Mhax\CC101-Lab>cd Notes

C:\Users\Mhax\CC101-Lab\Notes>ren profile-copy.txt about-me.txt

C:\Users\Mhax\CC101-Lab\Notes>echo This file will be deleted > temp.txt

C:\Users\Mhax\CC101-Lab\Notes>dir
 Volume in drive C is Windows-SSD
 Volume Serial Number is 08F9-ADBD

 Directory of C:\Users\Mhax\CC101-Lab\Notes

23/09/2026  07:41 pm    <DIR>          .
23/09/2026  07:13 pm    <DIR>          ..
23/09/2026  07:14 pm                75 about-me.txt
23/09/2026  07:41 pm                28 temp.txt
               2 File(s)            103 bytes
               2 Dir(s)  138,159,624,192 bytes free

C:\Users\Mhax\CC101-Lab\Notes>
~~~

### [Screenshot] Figure D2: From `del` to `tree /F`
*Optional image path for repository:* `![Figure D2](screenshots/Figure_D2.png)`

~~~cmd
C:\Users\Mhax\CC101-Lab\Notes>del temp.txt

C:\Users\Mhax\CC101-Lab\Notes>dir
 Volume in drive C is Windows-SSD
 Volume Serial Number is 08F9-ADBD

 Directory of C:\Users\Mhax\CC101-Lab\Notes

23/09/2026  07:43 pm    <DIR>          .
23/09/2026  07:13 pm    <DIR>          ..
23/09/2026  07:14 pm                75 about-me.txt
               1 File(s)             75 bytes
               2 Dir(s)  138,164,359,168 bytes free

C:\Users\Mhax\CC101-Lab\Notes>cd ..

C:\Users\Mhax\CC101-Lab>tree /F
Folder PATH listing for volume Windows-SSD
Volume serial number is 08F9-ADBD
C:.
│   profile.txt
│
├───Notes
│       about-me.txt
│
├───Projects
└───Screenshots

C:\Users\Mhax\CC101-Lab>
~~~

### [Answer] D-Q1
**After `del temp.txt`, check your Recycle Bin. Is `temp.txt` there? What does this tell you about deleting files from the command line?**

> When I checked the Recycle Bin, `temp.txt` was not there. I can conclude that deleting a file from the `cmd` permanently deletes it, bypassing the Recycle Bin.

---

## Part E: Explore PowerShell

*Switch to the PowerShell window.*

1. Go to your lab folder and list and read its files:

~~~powershell
cd $HOME\CC101-Lab
Get-ChildItem
Get-Content profile.txt
$PSVersionTable
~~~

### [Screenshot] Figure E1: PowerShell Directory Listing, Content, and Version Table
*Optional image path for repository:* `![Figure E1](screenshots/Figure_E1.png)`

~~~powershell
PS C:\Users\Mhax> cd $HOME\CC101-Lab
PS C:\Users\Mhax\CC101-Lab> Get-ChildItem


    Directory: C:\Users\Mhax\CC101-Lab


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        23/09/2026   7:43 pm                Notes
d-----        23/09/2026   7:12 pm                Projects
d-----        23/09/2026   7:12 pm                Screenshots
-a----        23/09/2026   7:14 pm             75 profile.txt


PS C:\Users\Mhax\CC101-Lab> Get-Content profile.txt
Name: Mart Sid De Venecia
Section: BSCS 1-1
Favorite app: Calculator
PS C:\Users\Mhax\CC101-Lab> $PSVersionTable

Name                           Value
----                           -----
PSVersion                      5.1.26100.9444
PSEdition                      Desktop
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0...}
BuildVersion                   10.0.26100.9444
CLRVersion                     4.0.30319.42000
WSManStackVersion              3.0
PSRemotingProtocolVersion      2.3
SerializationVersion           1.1.0.1
~~~

2. Run `Get-Help Get-ChildItem`. If PowerShell asks whether to run `Update-Help`, type `N` and press **Enter**.

### [Screenshot] Figure E2: `Get-Help Get-ChildItem` Output
*Optional image path for repository:* `![Figure E2](screenshots/Figure_E2.png)`

~~~powershell
PS C:\Users\Mhax\CC101-Lab> Get-Help Get-ChildItem

NAME
    Get-ChildItem

SYNTAX
    Get-ChildItem [[-Path] <string[]>] [[-Filter] <string>] [-Include <string[]>]
    [-Exclude <string[]>] [-Recurse] [-Depth <uint32>] [-Force] [-Name]
    [-UseTransaction] [-Attributes {ReadOnly | Hidden | System | Directory |
    Archive | Device | Normal | Temporary | SparseFile | ReparsePoint |
    Compressed | Offline | NotContentIndexed | Encrypted | IntegrityStream |
    NoScrubData}] [-FollowSymlink] [-Directory] [-File] [-Hidden] [-ReadOnly]
    [-System] [<CommonParameters>]

ALIASES
    gci
    ls
    dir

REMARKS
    Get-Help cannot find the Help files for this cmdlet on this computer. It is
    displaying only partial help.
        -- To download and install Help files for the module that includes this
        cmdlet, use Update-Help.
        -- To view the Help topic for this cmdlet online, type: "Get-Help
        Get-ChildItem -Online" or go to https://go.microsoft.com/fwlink/?LinkID=113308.
~~~

3. Take the last three digits of your student ID number (`26117109` $\rightarrow$ `109`). Convert it with PowerShell:

~~~powershell
[Convert]::ToString(109, 2)
[Convert]::ToString(109, 8)
'{0:X}' -f 109
~~~

### [Screenshot] Figure E3: Number Base Conversions in PowerShell
*Optional image path for repository:* `![Figure E3](screenshots/Figure_E3.png)`

~~~powershell
PS C:\Users\Mhax\CC101-Lab> [Convert]::ToString(109, 2)
1101101
PS C:\Users\Mhax\CC101-Lab> [Convert]::ToString(109, 8)
155
PS C:\Users\Mhax\CC101-Lab> '{0:X}' -f 109
6D
~~~

### [Answer] E-Q1
**Write your number in decimal, binary, octal, and hexadecimal. Keep this; you will verify it by hand in Week 5.**

* **Decimal:** $109_{10}$
* **Binary:** $1101101_2$
* **Octal:** $155_8$
* **Hexadecimal:** $\text{6D}_{16}$

---

## Part F: Discover a New Command

1. In Command Prompt, type `help` to see a list of commands.
2. Choose one command that was not taught in this lesson and is safe to run (e.g., `DATE`).
3. Read its help with `command /?` (`DATE /?`), then run it.

### [Screenshot] Figure F1: `help` Command Output
*Optional image path for repository:* `![Figure F1](screenshots/Figure_F1.png)`

~~~cmd
C:\Users\Mhax\CC101-Lab>help
For more information on a specific command, type HELP command-name
ASSOC          Displays or modifies file extension associations.
ATTRIB         Displays or changes file attributes.
BREAK          Sets or clears extended CTRL+C checking.
BCDEDIT        Sets properties in boot database to control boot loading.
CACLS          Displays or modifies access control lists (ACLs) of files.
CALL           Calls one batch program from another.
CD             Displays the name of or changes the current directory.
...
DATE           Displays or sets the date.
DEL            Deletes one or more files.
DIR            Displays a list of files and subdirectories in a directory.
...
VER            Displays the Windows version.
VERIFY         Tells Windows whether to verify that your files are written
               correctly to a disk.
VOL            Displays a disk volume label and serial number.
XCOPY          Copies files and directory trees.
WMIC           Displays WMI information inside interactive command shell.

For more information on tools see the command-line reference in the online help.
~~~

### [Screenshot] Figure F2: `DATE /?` Command Output
*Optional image path for repository:* `![Figure F2](screenshots/Figure_F2.png)`

~~~cmd
C:\Users\Mhax\CC101-Lab>DATE /?
Displays or sets the date.

DATE [/T | date]

Type DATE without parameters to display the current date setting and
a prompt for a new one.  Press ENTER to keep the same date.

If Command Extensions are enabled the DATE command supports
the /T switch which tells the command to just output the
current date, without prompting for a new date.

C:\Users\Mhax\CC101-Lab>
~~~

### [Answer] F-Q1
**What does your chosen command do, and when would it be useful?**

> First, my chosen command is the `DATE` command. It is used to display the current date setting and a prompt for a new one. It is useful for troubleshooting system time sync errors and automatically adding timestamps to automated backup scripts.

---

## Part G: Reflection

### 1. G-Q1: Which task in this activity was faster in the CLI than in the GUI? Which was easier in the GUI? Explain why.
> Creating and writing text to files was faster in the CLI because a single `echo` command does it instantly without opening separate programs. However, managing deleted files was easier in the GUI because you can visually see and browse the Recycle Bin with a mouse, whereas the CLI permanently deletes files immediately without trace.

### 2. G-Q2: What error did you encounter (if any), what caused it, and how did you fix it?
> I encountered an error at E2 where the command must be `Get-Help Get-ChildItem`; it showed `"Get-Help cannot find the Help files for this cmdlet on this computer. It is displaying only partial help."` I was not able to find a solution to fix it, so I just took a screenshot of it and pasted it into the document.

### 3. G-Q3: Give one real-world job or situation in computing where knowing the command line would be important.
> I think a real-world job example would be a Software Developer. A Software Developer needs to know the command line to efficiently manage their project files using version control tools like Git and to quickly install coding libraries. It also allows them to run, test, and debug their code directly through the terminal without relying on heavy graphical interfaces.

---

## Commands Learned Table

| Command | Shell | What It Does |
| :--- | :--- | :--- |
| `mkdir` | Command Prompt | Creates a folder. |
| `cd` | Command Prompt | Opens a folder / changes the current directory. |
| `echo Mart Sid De Venecia, BSCS 1-1` | Command Prompt | Displays `Mart Sid De Venecia, BSCS 1-1` to the screen in the terminal. |
| `echo "Mart Sid De Venecia, BSCS 1-1"` | PowerShell | Displays `Mart Sid De Venecia, BSCS 1-1` to the screen in the terminal. |
| `whoami` | Command Prompt | Displays the current logged-in username and domain of the person operating the computer. |
| `hostname` | Command Prompt | Prints the specific network name of your computer hardware on the screen. |
| `ipconfig` | Command Prompt | Displays your computer's network interface details. |
| `ver` | Command Prompt | Displays the exact version number of the Windows operating system. |
| `systeminfo` | Command Prompt | Displays a list of detailed information about the computer's hardware and operating system configuration. |
| `findstr` | Command Prompt | Used to search for specific text patterns or words inside files or command outputs. |
| `tree /F` | Command Prompt | Used to graphically display the folder structure of a specific drive or path, including all the files inside each folder. |
| `del` | Command Prompt | Used to permanently remove one or more files from the computer's disk storage. |
| `cd ..` | Command Prompt | Moves you backward or up one level in the folder hierarchy. |
| `dir` | Command Prompt | Displays a complete list of all files and subfolders contained inside the current directory. |
| `Get-ChildItem` | PowerShell | Similar to `dir`, the difference is that it is for PowerShell. It retrieves the files and folders inside your current location, displaying them in a cleaner, structured format. |
| `help` | Command Prompt & PowerShell | Displays a complete list of available system commands or provides the instruction manual for a specific command. |
| `DATE` | Command Prompt | Displays the current system calendar date and immediately drops down to a prompt asking you to type a new date. |
| `DATE /?` | Command Prompt | Opens the instruction manual for the `DATE` command. |

---

## Grading Rubric

| Criterion | Points | Full Marks | Partial Marks | Low Marks |
| :--- | :---: | :--- | :--- | :--- |
| **Completeness of procedure** | 30 | All 16 labeled, readable screenshots; every part A to F documented | 1 to 4 screenshots missing or unreadable | 5 or more screenshots missing |
| **Accuracy of results** | 20 | System-information table complete; commands and conversions correct and personalized | Minor errors or 1 to 2 missing values | Many errors, or results not the student's own |
| **Answers to guide questions (A to F)** | 20 | Correct, clear, in the student's own words | Mostly correct but brief or vague | Missing, incorrect, or copied |
| **Reflection (G-Q1 to G-Q3)** | 15 | Specific, honest, and linked to the activity | General statements with few specifics | Missing or off-topic |
| **Organization and formatting** | 15 | Follows the required order, naming, and formatting rules; commands learned table complete | Some rules not followed | Disorganized; wrong file type or name |
| **Total** | **100** | | | |