```text
                                       Republic of the Philippines
                                      Sorsogon State University
                                COLLEGE OF INFORMATION
                            AND COMMUNICATIONS TECHNOLOGY
                                            Bulan Campus
                                          Zone 8, Bulan, Sorsogon
                         Tel. No.; 056 311-0103; Email Address: cict@sorsu.edu.ph



                            CC 101 – Introduction to Computing
                Laboratory Activity: Programming Foundations

 Name: MART SID D. DE VENECIA                         Section: BSCS 1-1

 Date: November 13, 2026                              Score:          / 100




    Objectives

At the end of this activity, students should be able to:
   1. Create and run Python programs using PyCharm.
   2. Use variables, data types, type conversion, and operators correctly.
   3. Write programs that accept input and display formatted output.
   4. Apply selection (if, if–else, if–elif–else) and iteration (while, for) to solve simple problems.
   5. Test programs with planned test cases and debug syntax, runtime, and logic errors.
   6. Document programs with header comments and record them in the cc101-portfolio
       README.md.


    Materials and Environment

   •   Laboratory computer running Windows 11 (no Internet connection required)
   •   Python 3 and PyCharm Community Edition, installed beforehand on each computer
   •   File Explorer
   •   Your cc101-portfolio folder from the previous activity (or a new one, created in Part A)
Practicing at home: PyCharm needs Python to be installed first. Download Python for free from
https://www.python.org/downloads/. The Windows installer also installs IDLE, a simpler editor that
comes with Python; after installing, click Start, type IDLE, and open IDLE (Python 3.x). You may
use IDLE at home, or download the free version of PyCharm from
https://www.jetbrains.com/pycharm/download/. Every program in this activity works the same in
IDLE and PyCharm.


    General Instructions

   1. Save every program in the folder created in Part A, using the exact file names given.
   2. Start every program with a header comment (file name, your name and section, date,
       and purpose), as shown in the lecture notes.
   3. Before running a program, write your predicted output or expected result in the space
       provided. Then run the program and record the actual result.
   4. Run every program with all the test inputs given. If the result is wrong, debug the
       program, then test again.
   5. Work individually unless your instructor says otherwise. Copying another student's
       program is plagiarism.


    Part A. Set Up Your Workspace

   1. Open File Explorer (press Windows + E) and go to Documents → cc101-portfolio. If the
       folder does not exist, click New → Folder in Documents and name it cc101-portfolio.
   2. Open PyCharm Community Edition from the Start menu. On the Welcome screen, click
       Open (or, if a project is already open, click File → Open). Select Documents\cc101-


--------------------------------------------------------------------------------

                                        Republic of the Philippines
                                       Sorsogon State University
                                 COLLEGE OF INFORMATION
                             AND COMMUNICATIONS TECHNOLOGY
                                              Bulan Campus
                                           Zone 8, Bulan, Sorsogon
                          Tel. No.; 056 311-0103; Email Address: cict@sorsu.edu.ph


       portfolio and click OK. If PyCharm asks whether to trust the project, click Trust Project.
   3. Check the Python interpreter in the status bar at the bottom right of the PyCharm
       window. It should show Python 3.x. If it shows <No interpreter>, click it, choose Add New
       Interpreter → Add Local Interpreter, select the installed Python 3 (python.exe) as an
       existing or system interpreter, and click OK. Ask your instructor if no Python 3 appears in
       the list.
   4. Write down the Python version shown in the status bar:           Python 3.12                and
       the PyCharm version shown in Help → About:                PyCharm 2025.2.4
   5. Open the Project tool window on the left (press Alt + 1 if it is hidden). Right-click the
       cc101-portfolio folder, click New → Directory, type programming-foundations
       (lowercase, with a hyphen), and press Enter.
   6. Click File → Settings (or press Ctrl + Alt + S), go to Editor → Code Style → Python → Tabs
       and Indents, and confirm that Indent is 4. Click OK.
How to create and run each program in PyCharm:
   1. In the Project tool window, right-click the programming-foundations folder and click New
       → Python File.
   2. Type the file name without .py (for example, my_profile) and press Enter. PyCharm adds
       .py and opens the file.
   3. Type the code. PyCharm saves your work automatically; there is no need to click Save.
   4. Right-click anywhere inside the code and click Run 'my_profile' (or press Ctrl + Shift + F10).
       The output appears in the Run window at the bottom.
   5. When the program asks for input, click inside the Run window, type the value, and press
       Enter.
   6. To run the same program again, click the green Run button (▶) at the top right or press
       Shift + F10. To run a different file, right-click inside that file and choose Run again.
   7. To stop a running program (for example, an infinite loop), click the red Stop button (■) in
       the Run window or press Ctrl + F2.


    Part B. Guided Exercises

Exercise 1. My Profile (variables and output)
Type the program below, replacing the values with your own information. Save it as my_profile.py
and run it.
       # my_profile.py
       # Author : (your name), BSCS 1-1
       # Purpose: Displays my profile using variables.

       name = "Juan Dela Cruz"
       program = "BSCS"
       section = "1-1"
       age = 18

       print(f"Name : {name}")
       print(f"Program: {program} {section}")
       print(f"Next year I will be {age + 1} years old.")


--------------------------------------------------------------------------------

                                            Republic of the Philippines
                                           Sorsogon State University
                                    COLLEGE OF INFORMATION
                                AND COMMUNICATIONS TECHNOLOGY
                                                 Bulan Campus
                                               Zone 8, Bulan, Sorsogon
                              Tel. No.; 056 311-0103; Email Address: cict@sorsu.edu.ph


           Expected Output:

           Name : Mart Sid D. De Venecia

           Program: BSCS 1-1

           Next year I will be 19 years old.

Copy the actual output of your program:

 Name : Mart Sid D. De Venecia
 Program: BSCS 1-1
 Next year I will be 19 years old.




Exercise 2. Data Types and Type Conversion (interactive mode)
Open the Python Console by clicking Tools → Python or Debug Console (or the Python Console
button at the bottom left of the PyCharm window). Type each expression after the >>> prompt
and press Enter. Write your prediction first, then the actual result. If Python shows an error, write the
error name.

 Expression                              Predicted Result                     Actual Result

 type(2026)                              int                                  <class 'int'>
 type(3.0)                               float                                <class 'float'>
 type("3.0")                             str                                  <class 'str'>
 type(5 > 3)                             bool                                 <class 'bool'>
 int("42") + 8                           50                                   50
 "42" + "8"                              428                                  ‘428’
 int(7.9)                                8                                    7
 float("2.5") * 2                        5.0                                  5.0
 str(10) + "0"                           100                                  ‘100’
 int("7.5")                              ValueError                           ValueError


Exercise 3. Operators and Precedence (interactive mode)
Evaluate each expression by hand first, then check it in the Python Console.
#Note: the student is familiar with the python operators

 Expression                              Predicted Result                     Actual Result

 7/2                                     3.5                                  3.5
 7 // 2                                  3                                    3
 7%2                                     1                                    1
 2 ** 10                                 1024                                 1024
 10 + 4 * 3 ** 2 / 6                     16                                   16.0
 (10 + 4) * 3                            42                                   42


--------------------------------------------------------------------------------

                                        Republic of the Philippines
                                       Sorsogon State University
                                 COLLEGE OF INFORMATION
                             AND COMMUNICATIONS TECHNOLOGY
                                              Bulan Campus
                                           Zone 8, Bulan, Sorsogon
                          Tel. No.; 056 311-0103; Email Address: cict@sorsu.edu.ph



 Expression                           Predicted Result                    Actual Result

 17 % 5 == 2                          True                                True
 not (3 > 5) and 4 <= 4               True                                True
 3 > 5 or 10 != 10                    False                               False


Exercise 4. Midterm Rating Calculator (input, expressions, formatted output)
The CC 101 midterm rating is 65% of the laboratory grade plus 35% of the lecture grade. Type,
save as grade_calculator.py, and run the program with each test input.
        # grade_calculator.py
        lab = float(input("Laboratory grade: "))
        lecture = float(input("Lecture grade: "))
        rating = lab * 0.65 + lecture * 0.35
        print(f"Midterm rating: {rating:.2f}")



 Test      Laboratory       Lecture           Expected Output                 Actual Output

 1         88               80                Midterm rating: 85.20           Midterm rating: 85.20
 2         90               95                Midterm rating: 91.75           Midterm rating: 91.75
 3         75               70                Midterm rating:                 Midterm rating: 73.25

For Test 3, compute the expected output by hand before running the program.


     Part C. Write Your Own Programs

Write each program on your own. First plan it with short pseudocode, then code, test, and debug
it.

Exercise 5. Even or Odd (selection)
Save as even_odd.py. The program asks for a whole number and displays whether it is even or


--------------------------------------------------------------------------------

                                       Republic of the Philippines
                                      Sorsogon State University
                               COLLEGE OF INFORMATION
                           AND COMMUNICATIONS TECHNOLOGY
                                            Bulan Campus
                                          Zone 8, Bulan, Sorsogon
                         Tel. No.; 056 311-0103; Email Address: cict@sorsu.edu.ph


odd. Hint: use the % operator.
Pseudocode:
START
ENTER Number
IF Number % 2 == 0
   DISPLAY even
ELSE
   DISPLAY odd
END


Code:
# even_odd.py
# Author: Mart Sid D. De Venecia, BSCS 1-1
# Purpose: Check whether the inputted number is even or odd.

n = int(input("Enter a whole number: "))
if n % 2 == 0:
    print(f"{n} is even.")
else:
    print(f"{n} is odd.")



 Input                Expected Output                             Actual Output

 14                   14 is even.                                 14 is even.
 7                    7 is odd.                                   7 is odd.
 0                    0 is even.                                  0 is even.
 -3                   -3 is odd.                                  -3 is odd.


Exercise 6. Jeepney Fare (if–else, expressions)
Save as jeepney_fare.py. For this exercise, assume the fare is PHP 13.00 for the first 4 km, plus PHP
1.80 for every kilometer after the first 4 km. Students, senior citizens, and persons with disability
(PWD) get a 20% discount. The program asks for the distance in whole kilometers and whether the


--------------------------------------------------------------------------------

                                        Republic of the Philippines
                                       Sorsogon State University
                                COLLEGE OF INFORMATION
                            AND COMMUNICATIONS TECHNOLOGY
                                             Bulan Campus
                                           Zone 8, Bulan, Sorsogon
                          Tel. No.; 056 311-0103; Email Address: cict@sorsu.edu.ph


passenger gets the discount (Y or N), then displays the fare with two decimal places.


Pseudocode:
START
ENTER distance
ENTER discount
IF distance >= 4
        distance -= 4
ELSE
DISTANCE = 0
fare = 13 + 1.8*(distance)
IF discount is Y
   20% distount
ELIF discount IS N
        No discount
DISPLAY fare
END

Code:
# jeepney_fare
# Author: Mart Sid D. De Venecia
# Purpose: calculate the total jeepney fare.+

distance = float(input("what is the total distance in kilometers? "))
discount = input("Does the passenger get a discount? ")
if distance >= 4:
   distance -= 4
else:
   distance = 0

fare = 13 + 1.8*(distance)
if discount.upper() == "Y":
   total_fare = fare - 0.2*(13 + 1.8*(distance))
elif discount.upper() == "N":
   total_fare = fare

print(f"Fare: PHP {total_fare:.2f}")


 Test     Distance (km)       Discount?        Expected Output                 Actual Output

 1        3                   N                Fare: PHP 13.00                 Fare: PHP 13.00

 2        4                   N                Fare: PHP 13.00                 Fare: PHP 13.00

 3        5                   N                Fare: PHP 14.80                 Fare: PHP 14.80

 4        10                  N                Fare: PHP 23.80                 Fare: PHP 23.80

 5        10                  Y                Fare: PHP 19.04                 Fare: PHP 19.04

 6        4                   y                Fare: PHP 10.40                 Fare: PHP 10.40


Which tests are boundary test cases? Why?         Test 6 would have been the boundary test case
because of the input being a small y instead of a capital Y, but since I had encountered the same
case before, I managed to solve it by setting the input first into a capital letter with “.upper()”.


--------------------------------------------------------------------------------

                                        Republic of the Philippines
                                       Sorsogon State University
                                 COLLEGE OF INFORMATION
                             AND COMMUNICATIONS TECHNOLOGY
                                              Bulan Campus
                                           Zone 8, Bulan, Sorsogon
                          Tel. No.; 056 311-0103; Email Address: cict@sorsu.edu.ph


Exercise 7. Sum from 1 to n (for loop)
Save as sum_to_n.py. The program asks for a positive whole number n and uses a for loop with
range() to compute 1 + 2 + ... + n.


Pseudocode:
START
INITIALIZE s = 0
ENTER positive whole number
FOR i in range(1, n+1)
         s += i
DISPLAY s
END

Code:
# sum_to_n.py
# Author: Mart Sid D. De Venecia
# Purpose: Sum from 1 tp n (for loop)

s=0
n = int(input("Enter a positive whole number: "))
for i in range(1, n+1):
   s += i
print(f"Sum of 1 to {n} = {s}")


 Input                  Expected Output                            Actual Output

 10                     Sum of 1 to 10 = 55                        Sum of 1 to 10 = 55
 100                    Sum of 1 to 100 = 5050                     Sum of 1 to 100 = 5050
 1                      Sum of 1 to 1 = 1                          Sum of 1 to 1 = 1


Exercise 8. Savings Tracker (sentinel-controlled while loop)
Save as savings_tracker.py. The program keeps asking for the amount saved each day until the
user enters 0. Then it displays the number of days and the total saved, with comma separators
and two decimal places.
         Sample run (user input in bold)
         Savings today (0 to stop): 20
         Savings today (0 to stop): 50
         Savings today (0 to stop): 35.50
         Savings today (0 to stop): 0
         Total saved in 3 days: PHP 105.50


--------------------------------------------------------------------------------

                                       Republic of the Philippines
                                      Sorsogon State University
                                COLLEGE OF INFORMATION
                            AND COMMUNICATIONS TECHNOLOGY
                                             Bulan Campus
                                          Zone 8, Bulan, Sorsogon
                         Tel. No.; 056 311-0103; Email Address: cict@sorsu.edu.ph




Pseudocode:
START
INITIALIZE saved = 1
INITIALIZE total = 0
INITIALIZE days = -1
WHILE s is not equal to 0
ENTER saved
total += saved
days += 1
DISPLAY total and days
END

Code:
# savings_tracker.py
# Author: Mart Sid D. De Venecia, BSCS 1-1
# Purpose: Keep track of total savings each day.

saved = 1
total = 0
days = -1

while s != 0:
   s = float(input("Savings today(0 to stop): "))
   total += saved
   days += 1
print(f"Total Saved in {days} days: PHP {total: .2f}")


What does your program display if the first amount entered is 0?         Total Saved in 0 days: PHP 0.0


     Part D. Debugging

The program below should get three scores, display PASSED (average of 75 or higher) or FAILED,
and display the average. It has six bugs. Type it without the line numbers, save it as
buggy_average.py, and run it. Fix one error at a time, run again, and record each bug in the
table.
       1 count = 1
       2 total = 0
       3 while count <= 3
       4    score = input("Enter score: ")
       5    total = total + score
       6 average = total / 3
       7 if average => 75:
       8    print("PASSED")
       9 else
       10    print("FAILED")
       11 print("Average: " + average)

 Bug    Line     Error Message or Symptom                Error Type         Fix

 1          3               Expected ‘:’                   SyntaxError              while count <= 3:


--------------------------------------------------------------------------------

                                        Republic of the Philippines
                                       Sorsogon State University
                                 COLLEGE OF INFORMATION
                             AND COMMUNICATIONS TECHNOLOGY
                                             Bulan Campus
                                           Zone 8, Bulan, Sorsogon
                          Tel. No.; 056 311-0103; Email Address: cict@sorsu.edu.ph



 Bug     Line     Error Message or Symptom                Error Type         Fix

 2       3        Infinite loop                           LogicalError       count = count + 1
                                                                             score = int(input(“Enter
 3       4        input is set to ‘str’                   TypeError
                                                                             score: “))
 4       7        Invalid syntax ‘=>’                     SyntaxError        if average >= 75:
 5       9        Expected ‘:’                            SyntaxError        else:
                  Can only concatenate str (not                              print(“Average:”,
 6       11                                     TypeError
                  “float”) to str                                            average)

Hint: one bug produces no error message. When you find it, click the red Stop button (■) in the
Run window or press Ctrl + F2 to stop the program. Test your fixed program with the scores 80, 70,
and 81; the expected output is PASSED and Average: 77.00.


     Part E. Documentation and Submission

     1. Make sure every .py file in the programming-foundations folder starts with a header
        comment and runs without errors.
     2. In the PyCharm Project tool window, double-click README.md (in the cc101-portfolio
        folder) to open it. If it does not exist, right-click cc101-portfolio, click New → File, and
        name it README.md.
     3. Add the section below at the end of the file. PyCharm saves it automatically, and the
        preview on the right shows how it will look on GitHub.
        ## Programming Foundations

        | Program | Description |
        | --- | --- |
        | programming-foundations/my_profile.py | Displays my profile using variables |
        | programming-foundations/grade_calculator.py | Computes the midterm rating |
        | programming-foundations/even_odd.py | Tells whether a number is even or odd |
        | programming-foundations/jeepney_fare.py | Computes the jeepney fare with discount |
        | programming-foundations/sum_to_n.py | Sums the numbers from 1 to n |
        | programming-foundations/savings_tracker.py | Totals daily savings until 0 is entered |
        | programming-foundations/buggy_average.py | Debugged quiz-average program |

     4. Submit this worksheet and show your running programs to your instructor.
     5. When you have Internet access, upload the programming-foundations folder and the
        updated README.md to your GitHub repository (Add file → Upload files → Commit
        changes).

Reflection
Answer in 2–3 sentences each.
     1. Which error was the hardest to find in Part D, and how did you find it?
       All errors was not that hard to find, but if I am not allowed to run the program to
     check, the hardest would have been the invalid syntax from line 7 “=>”. Because I
     didn’t notice it when I first scanned the code with my eye.
     2. Why is it important to write the expected output before running a program?
       I think it is important to write the expected output because it checks if the
     programmer really understood the code and doesn’t just rely on the output the
     compilers shows.


--------------------------------------------------------------------------------

                                      Republic of the Philippines
                                     Sorsogon State University
                              COLLEGE OF INFORMATION
                          AND COMMUNICATIONS TECHNOLOGY
                                           Bulan Campus
                                         Zone 8, Bulan, Sorsogon
                        Tel. No.; 056 311-0103; Email Address: cict@sorsu.edu.ph


  3. Give one real problem at home or school that you could solve with a loop and an if
        statement.

   One problem that I would want to solve is the problem that I frequently forget
  things when going to school and it is a real problem because our house is about 6
  kilometers away from the school. It works by asking me the usuall things I forget
  before I leave. This simple unending loop enough to serve as a every day reminder
  for the things that I need to bring.

while True:
 YorN = input(“Did you bring your wallet? )
 YorN = input(“Did you bring your towel? )
 YorN = input(“Did you bring your rubik’s cube? )
 YorN = input(“Did you bring your raincoat? )



   Laboratory Rubric

Criteria                    Description                                              Points

                            Exercises 4–8 run and produce the expected outputs
Program correctness                                                                  40
                            for all test cases

                            Predictions, test tables, and the Part D bug table are
Testing and debugging                                                                25
                            complete and correct

Code style and              Header comments, meaningful variable names, 4-
                                                                                     20
documentation               space indentation, updated README.md

Reflection and work         Thoughtful reflection; works independently and submits
                                                                                     15
habits                      on time

Total                                                                                100


--------------------------------------------------------------------------------
```
