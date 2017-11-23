README for CS223 Algorithms Project 2
Caleb Wagner (cwagner)
November 21, 2017

******************************************************************************
RUNNING INSTRUCTIONS:
This program was written and tested using Python 3 on Mac OS. To run the program, open a command prompt, navigate to the directory where cwagnerProj2.py is stored, and then type in:

	python cwagnerProj2.py

The user interface will then instruct the user to the next steps.
******************************************************************************
SAMPLE OUTPUT:

Caleb Wagner Algorithms CS2223 Project 2:

Summary:
This project compares the efficiency of two different algorithms that
are used to find the two closest points in a set of n points.
The two algorithms tested are:
	  -a recursive divide and conquer algorithm
	  -a brute force algorithm
See the Project 2 Report for further explanation and analysis of the algorithms. 
Please see the README.txt for any issues running this program.
-----------------------------------------------------------------------------------

Input List:
0 	 0
7 	 6
2 	 20
12 	 5
16 	 16
5 	 8
19 	 7
14 	 22
8 	 19
7 	 29
10 	 11
1 	 13

The closest distance is:
2.8284271247461903

               |  Recursive   | Brute Force 
Time (seconds) | 0.0000536000 | 0.0000752000

Fastest Algorithm: Recursive
******************************************************************************
TEST CASES:

This program was tested with several different test cases, some of which are provided below. See the Project 2 Report for the timing details of the different two algorithms. The 
test cases below can be run in the terminal by editing the line in the function readFile():

 	f = open(“input.txt","r")

and change “input.txt” to the name of the text file that is desired to be run.

Some of the test cases provided are:

1) input.txt:
	[(0,1),(99,50),(153,22),(44,11)]

2) test.txt
	[(3,666),(616,223),(27,54),(69,73),(157, 323),(415,179)]

3) test2.txt
	[(0,0), (7,6), (2,20), (12,5), (16,16), (5,8), (19,7), (14,22), (8,19), (7,29), (10, 11), (1,13)]

4) test3.txt
	[(0,0), (-4, 1), (-7,-2), (4,5), (13,6)]

5) test4.txt
	[(2, 3), (12, 30), (40, 50), (5, 1), (12, 10), (3, 4)]

6) test5.txt
	[(0, 1), (1, 2), (3, 3)]

******************************************************************************
LIBRARIES:

Time: **DO NOT NEED TO DOWNLOAD**
This program uses the time library provided by Python to call the time.clock() function. This function is used calculate the runtime for the three algorithms. 

Math: **DO NOT NEED TO DOWNLOAD**
This program uses the math library provided by Python to call the math.sqrt() function. This function is used to calculate square roots. 

String: **DO NOT NEED TO DOWNLOAD**
This program uses the string library provided by Python to call string.punctuation. This is used to parse the input text file to remove unwanted characters (i.e. “[“)

******************************************************************************
ERROR CHECKING:
This program has some basic error checking, mostly alerting the user if the input file cannot be found. As such, it is important for the test cases to be added to a text file in the following format:

[(num1, num2), (num3, num4), (num5, num6)]

While the program will catch some errors, it is by no means an exhaustive error check, so responsibility lies on the user to have proper input. 
******************************************************************************
CODE STRUCTURE:
The program begins by calling startUp() which prints to the screen a description of the project and program. The program calls readFile() which reads in the test case from the
text file. The test case is stored as a list, which is sent to storeValues() and in turn converts the values to type Point. Point is a class that has an x and y value as its fields. After the list has been created, the listed is copied and then sorted twice using Merge Sort. The first time the list is sorted in nondecreasing order by its x values, and the second time the list is sorted in nondecreasing order by its y values. 
Next, effRec() is called, which runs EfficientClosestPair() twenty times while timing the 
function and averaging the total time. EfficientClosestPair() calculates the closest distance using a recursive approach. effBF() is called after, which runs bruteForce() twenty times while timing the function and averaging the total time. bruteForce() calculates the closest distance using an exhaustive test case (checking every combination). Lastly, the results of the program are outputted to the screen by calling 
the createTable() function. 
******************************************************************************
ADDITIONAL:
For additional analysis of the algorithms used in this program, please refer to the Algorithms Project 2 Report. 
******************************************************************************


 

