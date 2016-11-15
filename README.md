# code-aid #2
Sometimes student leave a programming assignment with questions such as:

    What should I have done to get the program to work?
    Do I have good style? What should the style of this program really look like?
    I got it to work, but did I accomplish it in a good way? How might I have improved my program?

Questions to these answers are crucial to help you keep improving as a programmer. This extra credit assignment is meant to answer these types of questions.

You will receive extra credit points added to your midterm test score by completing this assignment. You will receive up to 10 extra credit points added to your exam score, based on the quality of your analysis, with the caveat that your total exam score cannot exceed 105 points. To receive credit, your analysis must be submitted before the published due date. There is currently a comment block at the top of the example code supplied for you. Just insert your analysis inside of and at the top of this block and submit. The autograde will show 1/1 because zyBooks ignores your comments and just submits the code we supplied with one test case from the exam. You may ignore the submission result. You submit just so that your analysis will be recorded and the TA can then read and grade your analysis at the top of the code block. Also, when you are ready for grading, use the Ycode exam section to request grading.

In this extra credit exercise we include the exact specs for the exam and also include a code solution from the professors. This is an opportunity to compare your code with a version of the code which is in good shape. This comparison exercise will help you to see areas where your coding is good and areas where you can improve. The code included will show you an example of correct style. It will also show you an appropriate programming solution to the problem. There is more than one good approach to solve this problem. Your task is to do a side by side comparison of your code for the exam and the code included here. You may copy out the included code and print it out or paste it to VS (where you can view the two tests in side by side windows), or a file, etc. so as to make it easier to compare.

1) Compare the style of your code with the code supplied and point out areas where you did a good job of following the style guide, and particularly discuss areas where your style could be improved. This is an area where there is much less room for flexibility and you should be able to pinpoint all key differences.

2) Compare the logical programming approach you took to the problem with the approach taken by the example code here. Where were your mistakes made if you had problems getting a correct solution? Analyze the difference in your approach and the supplied approach. Discuss the parts of your logical approach which were as good (or better) than the supplied example, and particularly discuss areas where you could have improved your approach. For this part you may, if you wish, go back to the exam lab and edit your code and submit as many times as you want to figure out where you went wrong and try to get the solutions correct. This could be good practice to get ready for the next exam.

If you take this exercise seriously it will help you improve your coding and will help you in your assignments and exams going forward. You will get the full 10 points if you do a thorough analysis and comparison of both style and logic between the two versions. Even if your exam code was rather incomplete, point out all the differences you can, including style used in the example which you have not been doing in general on your recent labs. ALSO, discuss what was causing you to struggle and explain how seeing the correct code helps you understand what was holding you back. In this case you will get points based on your effort and discussion. Your exam score will not be affected by any new updated auto-graded points, as we used your final/best version you submitted during your exam slot for that. Following is the specification you received for the exam.
Midterm 2 Exam - "Notes App"
Overview

In this midterm you will create a simple "Notes" application where the user can add notes (which are one line strings) to a note list, and manage the list with other operations. You will implement the list as a vector. We will be testing your general programming skills, and particularly your understanding of functions and vectors. You will have a loop allowing you to select from a set of options. You will implement each option as a separate function (which may in turn call other functions if necessary). The functions you implement are graded incrementally and they get increasingly harder as the program goes on. Work on the first ones first and get credit as you go. You may submit as many times as you want. You may not have time to finish all of the functions, but that is part of what we are testing on this exam.

To allow you to demonstrate your breadth of understanding, we sometimes give explicit directions on some parts of your functions (e.g. void, value vs reference passing, etc.). Follow these instructions carefully. We will put a "Special requirements" line under each operation below. For any parts not specified explicitly, you may implement those aspects however you please. We do not always mention all the parameters needed and you are expected to pass in what is necessary for the function. Use value and reference passing reasonably. If you happen to pass a parameter by reference that you will not update (i.e. you did it just to save processing time), then make it a const. If an option requires user input, you may query for that input before the call, or from inside the function, however you please.

At the bottom of the specification is an example of the full program input and output flow. We have turned off white space checking so that matching the exact number of newlines, etc. is not critical. However, we recommend that you try to follow the example below in terms of white space as closely as possible. For each of the functions described in the specification, review the input/output example for formatting, etc.

Important note: You may NOT use the C++ vector functions "insert" and "erase" in this program. You must write your own variations of these if needed. Once you have written your own functions, you may use your own versions for other functions that might benefit from their usage. Also, you may not use any higher level algorithms, such as those found in #include "algorithm". We want to see how you do writing your own code. You MAY use other basic functions found in your zyBook text such as string functions find, replace, etc.
Program Specification - "Notes App"
Menu (10 points)

Special requirements: none - This could be implemented as a function or just coded in main, however you would like.

Implement a looping menu which has the options shown in the example below. The only ones you need to implement right now are list and quit. The only time the users sees the option list is when the "list" option is chosen. When "quit" is chosen, print "Good Bye." and quit. If a user types an option not in the list, just prompt again with "Option: ". As discussed in the Style Guide, when using strings for your menu options, it is not necessary to replace them with constants.

Note: With the exception of an incorrect input option in the menu, (which you will type on accident occasionally), we will assume throughout the rest of this program that users will always enter reasonable valid inputs, and thus you do not need to test for inappropriate input. Of course, in real code, we would never assume that, but since time is tight, and you have done this many times in other labs, we make this simplifying assumption.

Friendly hint: In this exam the ONLY time that you should use cin.ignore is BEFORE a getline(), where the most recent preceding input operation was a cin. See section 7.2 for more details if you desire.
Add note and Print list (15 points)

Special requirements: None - Except that these and all options below must be implemented as functions.

In main, declare a vector of type string to store notes. Create functions for Add and Print. You will pass your notes vector, when needed, to these and other functions. The "Add" function queries the user for a one line note (an arbitrary string which could have spaces, etc.) and adds this note to the end of the current note vector. "Print" prints out the list (i.e. vector) of notes in the format shown in the example. You do not have to test for an empty list; you would just print out the header with no notes following.
Remove a note (15 points)

Special requirements: 1) returns an updated notes vector, 2) original notes vector is passed in by value

In addition to any other needed parameters, this function passes in an int, indicating which string to delete, where strings are numbered from 1 to the number of notes. You can see the number associated with a string when you choose "print" in the options menu. You may assume that the user will not try to remove a note from an empty list.
Insert a note (15 points)

Special requirements: 1) void function, 2) original notes vector is passed in by reference

Pass in an int indicating which will be the position (1 through current number of notes + 1) of the new passed in note.
Replacefirst (15 points)

Special requirements: none

For each note in the list, this function replaces the first occurrence of a user-input search phrase (string that may have spaces, etc.), with a user-input replace phrase. It returns the total number of replacements made. For this and the next function we recommend that you consider using the string find and replace functions as defined in Ch.test 3 of zyBooks.
Replaceall (5 points) - These are 5 well-earned points if you are able to get this far!!

Special requirements: none

For each note in the list, this function replaces all occurrences of a user-input search phrase with a user-input replace phrase. It returns the total number of replacements made.
Items Graded by the TA's Inspection (25 points):

    Style Guide Adherence. We do not require test cases in the header for this exam, but follow all other style expectations. However, you should still be doing your own test cases for each basic operation. For example, with remove (and insert) you would at least want to test does it work right when trying to remove the first, last, or a note in the middle, etc.
    Use functions for each operation, and where given, follow specific function specifications (5 points each).

Example Execution

*** Notes Program *** - type "list" to see options

Option: list
Options for the Notes program are: 
"add" - Add a note.
"print" - Print notes.
"remove" - Remove a note.
"insert" - Insert a note.
"replacefirst" - Replace first occurrence of a phrase in each note.
"replaceall" - Replace all occurrences of a phrase in each note.
"quit" - quit the Notes program.

Option: Gravy
Option: add
Enter note: Remember to read the Syllabus

Option: add
Enter note: Try to get the labs done without help

Option: print
Current List of notes:
Note 1: Remember to read the Syllabus
Note 2: Try to get the labs done without help

Option: remove
Note number to remove: 2

Option: print
Current List of notes:
Note 1: Remember to read the Syllabus

Option: insert
New inserted note number: 1
Enter new note: Start early!!

Option: print
Current List of notes:
Note 1: Start early!!
Note 2: Remember to read the Syllabus

Option: add
Enter note: Always read the scriptures and study the specs!

Option: replacefirst
Enter search phrase: read
Enter replace phrase: study
2 replacements done.

Option: print
Current List of notes:
Note 1: Start early!!
Note 2: Remember to study the Syllabus
Note 3: Always study the scriptures and study the specs!

Option: replaceall
Enter search phrase: study
Enter replace phrase: **study deeply**
3 replacements done.

Option: print
Current List of notes:
Note 1: Start early!!
Note 2: Remember to **study deeply** the Syllabus
Note 3: Always **study deeply** the scriptures and **study deeply** the specs!

Option: quit
Good Bye.
