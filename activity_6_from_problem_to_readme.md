# CC 101 — Introduction to Computing
## "From Problem to README": Designing a Number-System Converter and Documenting It in Markdown

**Republic of the Philippines**  
**Sorsogon State University**  
**College of Information and Communications Technology — Bulan Campus**  
Zone 8, Bulan, Sorsogon  
Tel. No.: 056 311-0103 | Email Address: cict@sorsu.edu.ph  

---

| Field | Details |
| :--- | :--- |
| **Name** | Mart Sid D. De Venecia |
| **Block** | BSCS 1-1 |
| **Computer Unit Used** | Laptop, Lenovo |
| **Date** | October 18, 2026 |

---

## I. Objectives

At the end of this activity, you should be able to:
* Analyze a number-system conversion problem by identifying its inputs, processes, loop condition, and outputs.
* Write pseudocode using sequence, selection, and iteration.
* Draw flowcharts using standard symbols and check them by tracing and testing with sample data.
* Create a properly formatted `README.md` file in Markdown using Notepad, without an Internet connection.
* Upload the `README.md` to your CC 101 GitHub Computing Portfolio repository (take-home part).

---

## II. Materials Needed

* A computer running Windows 11 with Notepad (no network or Internet connection is needed in the laboratory)
* This worksheet, a pencil, and a ruler (or a flowchart template) for drawing flowcharts
* A USB flash drive, to bring your `README.md` home for uploading
* For Part G only (outside the laboratory): any device with Internet access and a free GitHub account
* Week 7 lecture notes, for reference on pseudocode, flowchart symbols, and Markdown syntax

---

## III. Background

Programmers do not start by typing code. They first analyze the problem, plan the solution as pseudocode and a flowchart, and check it by hand. In this activity, you will design a program that converts numbers between the decimal and binary number systems you learned in Week 5. An algorithm can be written as pseudocode (English-like steps) or drawn as a flowchart (standard symbols connected by arrows). Good work is also documented. On GitHub, the standard way to introduce a project is a `README.md` file written in Markdown, a plain-text format that uses symbols such as `#`, `*`, and `-` for headings, emphasis, and lists. Because Markdown is plain text, you can write it in Notepad with no Internet connection and upload it to GitHub later.

---

## IV. Data and Findings

### Table 1. Problem Analysis for Problem 1: Decimal-to-Binary Converter (Part A)

| Item | Your Answer |
| :--- | :--- |
| **Restated problem (your own words)** | Create a program that asks the user to enter a whole number in decimal (base 10) that is greater than or equal to $0$, then converts it to binary (base 2), and displays the result. |
| **Input** | A whole number in decimal (base 10) that is $0$ or greater ($n$) |
| **Output** | The binary (base 2) representation of the input number (`binary`) |
| **Processes (operations)** | 1. Check if $n = 0$ (if true, set `binary = "0"`).<br>2. Find the remainder of dividing by $2$ using `remainder = n MOD 2`.<br>3. Place each new remainder to the left of the existing binary digits: `binary = remainder + binary`.<br>4. Divide the number by $2$ using whole-number division: `n = n DIV 2`. |
| **Loop condition (when the loop stops)** | The loop continues while $n > 0$ and stops when $n = 0$. |
| **Variables needed** | `n` (whole-number decimal input), `remainder` (remainder from `n MOD 2`), `binary` (string storing the binary result). |
| **13 and 25 in binary (computed by hand)** | **13:** $13 \div 2 = 6\text{ r }1$; $6 \div 2 = 3\text{ r }0$; $3 \div 2 = 1\text{ r }1$; $1 \div 2 = 0\text{ r }1 \rightarrow \mathbf{1101_2}$<br>**25:** $25 \div 2 = 12\text{ r }1$; $12 \div 2 = 6\text{ r }0$; $6 \div 2 = 3\text{ r }0$; $3 \div 2 = 1\text{ r }1$; $1 \div 2 = 0\text{ r }1 \rightarrow \mathbf{11001_2}$ |

---

### Box 1. Pseudocode for Problem 1: Decimal-to-Binary Converter (Part B)

~~~text
START
    INPUT n
    IF n = 0 THEN
        SET binary = "0"
    ELSE
        SET binary = ""
        WHILE n > 0 DO
            SET remainder = n MOD 2
            SET binary = remainder + binary
            SET n = n DIV 2
        ENDWHILE
    ENDIF
    DISPLAY binary
END
~~~

---

### Figure 1. Flowchart for Problem 1 (Part C)

*Optional image path for repository:* `![Flowchart for Problem 1](images/flowchart_problem1.png)`

~~~mermaid
flowchart TD
    START(["START"]) --> INPUT[/"INPUT n"/]
    INPUT --> COND_ZERO{"n = 0?"}
    COND_ZERO -- Yes --> SET_ZERO["SET binary = '0'"]
    COND_ZERO -- No --> SET_EMPTY["SET binary = ''"]
    SET_EMPTY --> LOOP_COND{"n > 0?"}
    LOOP_COND -- Yes --> REM["SET remainder = n MOD 2"]
    REM --> PREPEND["SET binary = remainder + binary"]
    PREPEND --> DIV["SET n = n DIV 2"]
    DIV --> LOOP_COND
    SET_ZERO --> DISPLAY[/"DISPLAY binary"/]
    LOOP_COND -- No --> DISPLAY
    DISPLAY --> END_NODE(["END"])
~~~

---

### Table 2. Trace of Problem 1 with Input 13 (Part C)

| Pass | `n` (before) | `n MOD 2` (remainder) | `n DIV 2` (new `n`) | `binary` (so far) |
| :---: | :---: | :---: | :---: | :--- |
| **1** | $13$ | $1$ | $6$ | `"1"` |
| **2** | $6$ | $0$ | $3$ | `"01"` |
| **3** | $3$ | $1$ | $1$ | `"101"` |
| **4** | $1$ | $1$ | $0$ | `"1101"` |
| **5** | *Loop stops because $0$ is not greater than $0$* | — | — | **Value displayed at the end:** `1101` |

---

### Table 3. Test Cases for Problem 1 (Part C)

| Case | Decimal Input | Binary (by hand) | Binary From Your Pseudocode | Match? (Y/N) |
| :---: | :---: | :---: | :---: | :---: |
| **1** | $0$ | `0` | `0` | Y |
| **2** | $5$ | `101` | `101` | Y |
| **3** | $13$ | `1101` | `1101` | Y |
| **4** | $25$ | `11001` | `11001` | Y |
| **5** | $255$ | `11111111` | `11111111` | Y |

---

### Box 2. Pseudocode for Problem 2: Binary-to-Decimal Converter (Part D)

~~~text
START
    INPUT binary
    SET decimal = 0
    SET place = 1
    WHILE binary > 0 DO
        SET digit = binary MOD 10
        SET decimal = decimal + (digit * place)
        SET binary = binary DIV 10
        SET place = place * 2
    ENDWHILE
    DISPLAY decimal
END
~~~

---

### Figure 2. Flowchart for Problem 2 (Part D)

*Optional image path for repository:* `![Flowchart for Problem 2](images/flowchart_problem2.png)`

~~~mermaid
flowchart TD
    START(["START"]) --> INPUT[/"INPUT binary"/]
    INPUT --> INIT["SET decimal = 0<br/>SET place = 1"]
    INIT --> LOOP_COND{"binary > 0?"}
    LOOP_COND -- Yes --> DIGIT["SET digit = binary MOD 10"]
    DIGIT --> ADD_DEC["SET decimal = decimal + (digit * place)"]
    ADD_DEC --> DIV_BIN["SET binary = binary DIV 10"]
    DIV_BIN --> MULT_PLACE["SET place = place * 2"]
    MULT_PLACE --> LOOP_COND
    LOOP_COND -- No --> DISPLAY[/"DISPLAY decimal"/]
    DISPLAY --> END_NODE(["END"])
~~~

---

### Table 4. Test Cases for Problem 2 (Part D)

| Case | Binary Input | Decimal (by hand) | Decimal From Your Pseudocode | Match? (Y/N) |
| :---: | :---: | :---: | :---: | :---: |
| **1** | `1101` | $13$ | $13$ | Y |
| **2** | `101010` | $42$ | $42$ | Y |
| **3** | `11111111` | $255$ | $255$ | Y |
| **4** | `10000000` | $128$ | $128$ | Y |

---

### Table 5. `README.md` File Check (Part E)

| Item | Your Findings |
| :--- | :--- |
| **Full folder path of `cc101-portfolio`** | `C:\Users\Mhax\OneDrive\Documents\cc101-portfolio` |
| **File name shown in File Explorer** | `README.md` |
| **Type shown in File Explorer (Details view)** | `Markdown Source File` |
| **Size of `README.md` shown by `dir` (bytes)** | `1,177` |
| **Does `type README.md` show your Markdown text? (Y/N)** | `Y` |
| **Notepad formatted view available? (Y/N)** | `Y` |
| **Elements that appeared formatted in Notepad (if available)** | Headings (`#`, `##`), bold (`**`), italic (`*`), bulleted list, numbered list, links, and horizontal rule (`---`) appear formatted; the table, image, and code block appear as plain text. |

---

### Table 6. Peer Review Checklist (Part F)

* **Reviewer's Name:** Carl Nathaniel B. Fundano
* **Owner of the README:** Mart Sid D. De Venecia

| Element | Markdown Used | Present and Correct? (Y/N) |
| :--- | :--- | :---: |
| **Level-1 heading** | `#` | Y |
| **Level-2 headings** | `##` | Y |
| **Paragraph** | Text with a blank line before and after | Y |
| **Bold and italic text** | `**bold**` `*italic*` | Y |
| **Bulleted list** | `- item` | Y |
| **Numbered list** | `1. item` | Y |
| **Table** | `\| header \|` and `\| --- \|` separator | Y |
| **Link** | `[text](url)` | Y |
| **Image** | `![alt](path)` | Y |
| **Code block** | Lines between two lines of three backticks | Y |
| **Horizontal rule** | `---` | Y |
| **File saved as `README.md` (not `.txt`)** | `README.md` | Y |

---

### Table 7. GitHub Submission (Part G, Take-Home)

| Item | Your Answer |
| :--- | :--- |
| **GitHub username** | `martsiddevenecia` |
| **Repository URL** | [https://github.com/martsiddevenecia/cc101-portfolio](https://github.com/martsiddevenecia/cc101-portfolio) |
| **Date uploaded (YYYY-MM-DD)** | `2026-10-18` |
| **Does the README display formatted on GitHub? (Y/N)** | `Y` |
| **Elements that did not display as expected, and why** | `None` |

---

## V. Realization (Reflection)

### 1. Which was easier for you to create, the pseudocode or the flowchart? Why?
> For me, the flowchart is easier to create. Because one of our professors taught us how to do flowcharting, which means flowcharting is not new to me anymore.

### 2. Did tracing and testing reveal any errors in your pseudocode or flowcharts? Describe what you found and how you corrected it.
> Yes, testing helped me find what went wrong in my operations when solving by hand, especially the reverse conversion.

### 3. How is writing a README in Markdown different from typing a document in Microsoft Word?
> Microsoft Word uses visual toolbar buttons to style text, while Markdown uses plain-text symbols like `#`, `*`, and `-` for headings, emphasis, and lists. Because Markdown is plain text, you can write it offline in Notepad and upload it to GitHub to display formatted project documentation.

### 4. How can a GitHub portfolio help you as a future computing professional?
> A GitHub portfolio serves as a public showcase of your programming projects, algorithms, and technical documentation as your skills grow. It allows future employers or clients to view real examples of your work and see how clearly you organize and explain your code.

---

## VI. Scoring Guide

| Criteria | Description | Points |
| :--- | :--- | :---: |
| **Problem Analysis & Pseudocode** | Table 1 is complete; the pseudocode for both conversions is correct (correct use of `MOD`, `DIV`, and the loop), uses proper keywords, and is indented. | 25 |
| **Flowcharts & Testing** | Both flowcharts use the correct symbols with labeled decisions and a clear loop; the trace (Table 2) and test cases (Tables 3 and 4) are correct. | 25 |
| **`README.md`** | The file is saved correctly as `README.md`, uses all required Markdown elements, and passes the peer review in Table 6. | 25 |
| **GitHub Upload** | The README is uploaded to a public `cc101-portfolio` repository and the URL is submitted (Table 7). | 10 |
| **Realization / Reflection** | Answers are thoughtful, specific to the student's own work, and well written. | 10 |
| **Neatness & Timeliness** | Worksheet is legible/well-formatted and submitted on time. | 5 |
| **Total** | | **100** |