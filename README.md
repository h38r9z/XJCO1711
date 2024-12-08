java cUNIVERSITY OF LEEDS | SCHOOL OF COMPUTING 
 
Assessment Brief 
 
Module title Procedural Programming 
Module code XJCO1711 
Assignment title Collaborating with HealthMate CIC on a Step Tracker Data Analysis Tool 
Assignment type and 
description 
This is a programming assignment. You will design and create a number of 
programs to solve a problem from your client. 
Rationale You are doing this assessment to develop your skills in software design and 
development. 
Word limit and guidance You will create a number of tested and working C programs 
Weighting 100%: This is the only assessment for this module 
Submission deadline Part 1: Friday November 8
th
 2024 (by 2pm) 
Part 2: Wednesday December 16
th 2024 (by 2pm) 
Submission method Online through Minerva. 
Feedback provision You will get automated feedback through Minerva and Gradescope 
Learning outcomes 
assessed 
LO1: select appropriate data types to represent data. 
LO2: apply problem solving techniques to develop a programming solution to 
real world problems. 
LO3: design, implement, debug and test procedural programs. 
Module leader Bo Peng 
Other Staff contact - 
 
  
UNIVERSITY OF LEEDS | SCHOOL OF COMPUTING 
1. Assignment guidance 
HealthMate CIC, a Community Interest Company based in the UK, is embarking on an ambitious project to 
support healthy lifestyles and enhance digital literacy among high achieving secondary school students. 
 
Their intention is to create a proof of concept that combines health consciousness with the teaching of 
digital proficiency. 
 
As intern software developers, you have been signed up to work on the development of a step tracker data 
analysis tool, the first step in this large project. 
 
Your mission is to develop a console application in C capable of analysing step data derived from a data file. 
 
This tool should offer a large range of analyses to give users with detailed insights into their daily physical 
activity, so supporting HealthMate CIC’s vision of a digitally literate and health-conscious younger 
generation. 
 
Although you will be expected to submit files to Gradescope for marking, you should continue to use Git and 
Codespaces to develop your code. 
 
If ever there are doubts whether work is completely your own, we will be able to look at your commit history 
to confirm when you have been working. 
 
We can give you general guidance and remind you where to find relevant supporting material in the notes, 
but coursework is individual and by submitting you are confirming that it is your own individual effort. 
 
You must attempt the part 1 task. All the part 2 tasks are optional but remember that the passing grade for 
the module is 40%.  
UNIVERSITY OF LEEDS | SCHOOL OF COMPUTING 
2. Assessment tasks 
Part 1: Submission deadline Friday November 8th 2024 (by 2pm) 
 
You can submit the task as many times as you like up to and including the deadline 
 
Total marks available: 15 
 
Task 1: Understanding our data files 
Difficulty level: BRONZE 
 
Task 1 marks: 15 
 
You are given a data file called FitnessData_2024.csv and a code template file StepsTask1.c 
 
Each row in the csv file looks like this: 
 
2024-09-01,08:15,150 
 
• The first column represents the date (in YYYY-MM-DD format). 
• The second column is a time (8.15am in our example) 
• The third column represents the steps counted in the 15 minutes immediately before the time stamp. 
Here, it means that the step counter has counted 150 steps between 8.00am and 8.15am. 
 
 
Your client wants you to write a single C program (called file_import.c) that will: 
• Read in this csv file 
• Store it in a suitably sized and structured array and typedef data structure 
• Write to the screen the first three rows of the file (corresponding to the times 07:30, 07:45, 08:00). 
This should be in the format: 
 
2024-09-01/08:15/150 
 
Note that there are NO SPACES here. We will test for this format EXACTLY. 
 
The output will be automatically marked so if you get the format wrong it’s likely you will get no 
marks. 
 
We will test it with multiple different files - so don’t “hard code” the output. 
 
This will involve you using an appropriate typedef (custom data structure). We suggest you use something 
like this and define it at the start of your program: 
 
typedef struct { 
 char date[11]; 
 char time[6]; 
 int steps; 
} FITNESS_DATA;  
UNIVERSITY OF LEEDS | SCHOOL OF COMPUTING 
The template program we supply (see Minerva) has this typedef already in it. Feel free to use this or to come 
up with something better yourself. 
 
Also in the template, you will see that we have already written a helper function called tokeniseRecord that 
you can use to split the string representing each line from the file into a number of individual token strings. 
 
You do not need to understand how this function works and should not change it in any way. This is the 
same function that we have used before in our teaching sessions. 
 
When you submit the file it should have the exact filename: 
 
StepsTask1.c 
 
How it will be marked: 
 
 1. The ability to read in the file we give you without any errors: 5 marks 
2. The ability to read in another data file that you have not seen: 5 marks 
3. Printing out the requested rows: 5 marks 
 
 
 
  
UNIVERSITY OF LEEDS | SCHOOL OF COMPUTING 
Part 2: Submission deadline Wednesday December 16th 2024 (by 2pm) 
Total marks available: 85 
 
You can submit the tasks as many times as you like up to and including the deadline 
 
Task 2: Analysing our data 
Difficulty level: SILVER 
 
Task 2 marks: 30 
 
Following on from your initial program, you now need to expand your initial program to add some features 
to analyse the data and help us understand what the data means. 
 
Following good programming practice, you should split your program functionality into two files: 
 
FitnessDataStruct.h – a header file containing the struct typedef and any helper functions you want 
 
StepCounter.c – a program that contains the code and functions to solve the requested tasks 
 
The program should provide a simple menu system and ask the user to select from the following options and 
an option to quit. 
 
A: Specify the filename to be imported (we will give you some additional files to test with). This should have 
some error checking so that the program can cope with an incorrect filename and a file that is of an 
unexpected format. 
B: Display the total number of records in the file 
C: Find the date and time of the timeslot with the fewest steps 
D: Find the data and time of the timeslot with the largest number of steps 
E: Find the mean step count of all the records in the file 
F: Find the longest continuous period where the step count is above 500 steps 
 
These should be printed out exactly as below: 
 
Option Example output 
A Input filename: 
B Total records: 229 
C Fewest steps: 2024-09-01 14:20 
D Largest steps: 2024-09-01 18:00 
E Mean step count: 427 
F Longest period start: 2024-09代 写XJCO1711、C++
代做程序编程语言-01 14:20 
Longest period end: 2024-09-01 18:00 
 
How it will be marked: 
1. Providing a menu system providing options A-F and Quit: 5 marks 
2. Successfully coping with an incorrect filename: 4 marks 
3. Displaying the total number of records: 4 marks 
4. Date and time of fewest steps: 4 marks  
UNIVERSITY OF LEEDS | SCHOOL OF COMPUTING
 
5. Date and time of largest steps:
 
 
 
 
 4 marks
 
6. Mean step count:
 
 
 
 
 
 
 4 marks
 
7. Longest continuous period:
 
 
 
 
 5 marks
 
  
UNIVERSITY OF LEEDS | SCHOOL OF COMPUTING 
Task 3: Outputting sorted data 
Difficulty level: SILVER 
 
Task 3 marks: 15 
 
This task requires you to write a utility program to output the data file sorted by descending order of step 
count (so the row with the highest step count should be at the top) in tab separated values (tsv) format. 
 
A .tsv file differs slightly from a .csv in that the delimiter isn’t a comma (,) but a tab character. This has the 
special code \t 
 
You won’t see this if printed on the screen, it will just look like a few spaces between the values. 
 
You will be supplied with a template file with the same tokeniseRecord helper function you used before. 
 
Your program should: 
 
 1. Provide a menu option to specify a filename, using the prompt: 
Enter Filename: 
2. Process the data file (read in and sort). It should be able to cope with an incorrect filename and to 
give an appropriate error message if the file is not in the correct format 
3. Write out the sorted data file with the same filename (but with the file extension .tsv). The record 
with the highest step count should be at the top and the record with the smallest step count should 
be at the bottom. You will need to think how to deal with any records where the step counts are the 
same. 
 
If the input file is: 
mydata.csv 
 
The output file will be: 
mydata.tsv 
 
 
How it will be marked: 
1. Providing the menu option and coping with an incorrect filename: 5 marks 
2. Coping with an incorrectly formatted file (the fields in the wrong order): 5 marks 
3. Creating an output file in the correct format: 5 marks 
  
UNIVERSITY OF LEEDS | SCHOOL OF COMPUTING 
Task 4: Simulating a 3-axis accelerometer for a step counter 
Difficulty level: GOLD 
 
This is an extension “stretch and challenge” task. We do not expect that all students will be able to 
complete it. 
 
Task 4 marks: 25 
 
Your task is to explore how a 3-axis accelerometer works and write a C program that will generate simulated 
data on all three axes for a 5 minute period. You’ll need to decide what axis or combination could be used to 
represent the steps. 
 
Your program should provide some mechanism to allow this value to be accessed or downloaded. 
 
This task will be assessed through a demonstration and short question and answer session with one of the 
lecturers or teaching assistants. 
 
You will need to book a slot to do this face-to-face or alternatively you may record a short (maximum 5-
minute) private Youku video and let us have the link by the final submission date. 
 
How it will be marked: 
1. Describing how you have looked at the data from the 3 axes and decided what might represent a step 
count (your experimental approach): 10 marks 
2. Writing and testing a C program that generates the step data for 5 minutes: 10 marks 
3. Providing some mechanism to download or access the number of steps: 5 marks 
  
UNIVERSITY OF LEEDS | SCHOOL OF COMPUTING 
Task 5: Understanding code quality 
Difficulty level: BRONZE 
 
Task 3 marks: 15 
 
For this task you will need to complete the multiple choice quiz in Class. You will only get one chance at this. 
 
It has 15 questions related to good programming practice. Once you start you must complete the quiz within 
45 minutes. 
 
You can refer to any materials you like but it should be your own work. 
 
How it will be marked: 
 
Each of the 15 questions is worth 1 mark.  
UNIVERSITY OF LEEDS | SCHOOL OF COMPUTING 
3. General guidance and study support 
Please refer to the module teaching materials in Minerva for any background support. 
 
4. Assessment criteria and marking process 
This assignment tests the Learning Objectives for this module: 
 
Marks and feedback will be returned to you approximately three working weeks after the final submission 
date. 
 
The passing mark for the assessment is 40% and this can be gained from any task or combination of tasks. 
 
5. Presentation and referencing 
You should produce working and tested C programs, uploaded to Gradescope with plenty of comments to 
explain your work. We also expect you to use meaningful variable names and for code to be indented to 
make it readable. 
 
If you use an idea in your solution that you have seen on the Web somewhere then add a comment to the 
code like this: 
 
// I based this on an idea I found here: 
// https://stackoverflow.com/questions/12901021/error-in-c-file-handling 
 
If you use a book or a printed resource then give the author and title: 
 
// I based this on an idea I got from here: 
// An Introduction to C and GUI Programming by Simon Long, pages 56-57 
 
If you used ChatGPT, the tell us the prompt you used: 
 
// I based this on a discussion with ChatGPT 
// Prompt: Explain how to import a CSV file in C 
 
6. Submission requirements 
All code should be uploaded to the submission points in Gradescope (we will explain fully how to do this in 
our sessions). 
 
7. Academic misconduct and plagiarism 
Leeds students are part of an academic community that shares ideas and develops new ones. 
  
UNIVERSITY OF LEEDS | SCHOOL OF COMPUTING 
You need to learn how to work with others, how to interpret and present other people's ideas, and how to 
produce your own independent academic work. It is essential that you can distinguish between other 
people's work and your own, and correctly acknowledge other people's work. 
 
All students new to the University are expected to complete an online Academic Integrity tutorial and test, 
and all Leeds students should ensure that they are aware of the principles of Academic integrity. 
 
When you submit work for assessment it is expected that it will meet the University’s academic integrity 
standards. 
 
If you do not understand what these standards are, or how they apply to your work, then please ask the 
module teaching staff for further guidance. 
 
By submitting this assignment, you are confirming that the work is a true expression of your own work and 
ideas and that you have given credit to others where their work has contributed to yours. 
 
8. Assessment/ marking criteria grid 
Task Description Marks available 
Part 1- task 1 Importing a file into an array of structs and printing first two rows 15 
Part 2- task 2 Analysing our data 30 
Part 2- task 3 Outputting sorted data 15 
Part 2- task 4 Simulating a 3-axis accelerometer for a step counter 25 
Part 2- task 5 Multiple choice quiz 15 
 
         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
