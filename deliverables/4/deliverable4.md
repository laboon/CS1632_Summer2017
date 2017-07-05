# CS 1632 - Software Quality Assurance
Summer Semester 2017

__DUE 18 JULY 2017__

## Deliverable 4

For this assignment, you and a partner will develop KPIs for JBefunge, profile it, and improve its performance in some way.  Additionally, you will write appropriate pinning tests for any change made.  This will consist of several parts:

Code is available on Github (https://github.com/laboon/JBefunge).  Please _duplicate_ (https://help.github.com/articles/duplicating-a-repository/) it and create your own repository, which should be private and shared with me (laboon) and the TA (NannanWen).  

Please do _not_ use the JBefunge that you modified in Deliverable 2.  That is Befunge++, which is, as we all know, an entirely different language than Befunge.

## Format
Every assignment should have a title page with:
* The name of the students in the group, along with their GitHub usernames
* The title "CS 1632 - DELIVERABLE 4: Performance Testing Using VisualVM"

There is no need to print out the code.  It should be available on GitHub or a similar code-sharing site BY THE BEGINNING OF CLASS.

In order to determine the "hot spots" of the application, you will need to run a profiler such as VisualVM (download at https://visualvm.java.net/).  Using a profiler, determine a method you can use to measurably increase the speed of the application without modifying behavior.  

For the summary, describe how you determined the KPIs, and the method(s) to refactor.  At the end, discuss whether or not your program has met the KPIs.  If it has, discuss why you think those KPIs were sufficient.  If it has not, discuss what additional work or research you would want to do to ensure that KPIs are met before release.  The summary should be approximately one page. 

After this, include screenshots of VisualVM (or another profiler, if you use that) both before and after the refactor.  These screenshots should include the relevant sections that let you see what method to refactor.

As part of this assignment, you should create "pinning tests".  Pinning tests are unit tests which should check that the behavior of a modified method was not changed by your refactor (see the chapter on testing legacy code in AFIST for examples).  This program should work EXACTLY the same as before, except that it is more performant _in some way_ (more efficient memory usage, less time to execute, etc.).  The only exception is if you come across an error and fix it - no points will be taken off as long as you note it in your summary.

Pinning tests should always pass - both before and after refactoring.  Remember that refactoring modifies the code _without_ changing functionality.

For the coding change, there should be at least four pinning tests which test both the happy path and several different edge cases.  If you modify something in one of the `Program*.java` files (ProgramExecutor, ProgramStack, ProgramArea), these pinning tests _must_ be unit tests.  If you modify something in any other file, they may be unit tests _or_ manual tests.  If you use manual tests, remember to use the same format as used in Deliverable 1.

For the final analysis, you must run the program three times, and measure the improvement each time.  You should write each of these down, along with their arithmetic mean.  For example, let's say that you have modified code to minimize memory usage - you should run the program three times and mark down the total memory used each time.  If you improve execution speed, run a program three times and mark down how long it took to run it.  

I recommend you use `fizzbuzz.bf` for testing, but that may be inappropriate for your particular change.  For example, you may modify an opcode execution method which is not included in FizzBuzz.  You can write your own Befunge program to test it or use a Befunge program that you found online (as long as you credit the source).

Remember when modifying code that the end goal is to keep functionality exactly the same while only modifying performance.  If there is any doubt, you may want to run some other Befunge programs on your modified Befunge IDE before turning in the assignment.

## Grading
* Summary - 10%
* KPIs - 10%
* VisualVM (or other profiler) screenshots (before and after) - 5%
* Initial and final measurements (>= 3 of each + mean) included - 5%
* Method choice and refactoring - 45%
* Pinning Tests - 25%

Please feel free to email me or come to office hours to discuss any problems you have. 
 
