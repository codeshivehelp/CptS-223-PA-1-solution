# CptS-223-PA-1-solution

Download Here: [CptS 223 PA #1 solution](https://jarviscodinghub.com/assignment/cpts-223-pa-1-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

For this project, we will be empirically evaluating bubble sort and comparing it to our own Big­O
analysis. To do this, we will use a range of input values and time how long it takes bubblesort to finish
the sorting of N random values. These timings will be plotted on a Cartesian Coordinate grid to
compare with our expected algorithm behavior. We will also test bubblesort on best and worst case
inputs to see how it runs.
Bubblesort
The code for this project is written in the expected C++11 language and tested using g++.
The primary function will take an input of how many random integers to sort, and return how long it
took to sort the given vector of N randomly generated integers. This function will be called many
times to generate our statistics.
// sorts the vector of n elements passed in
// returns # of seconds to accomplish the sorting
float do_bubblesort(std::vector &arr, int n)
To calculate the length of the sort, I suggest you use the c++ chrono library. An example of using this
library to evaluate a different algorithm is shown here:
https://en.cppreference.com/w/cpp/chrono
That example code compiles and runs on the EECS SSH servers just fine. You can use that as a starting
point for you own work. You will need to compile it using the g++ command line option ­std=c++0x to
let g++ know to use the newer libraries than the defaults:
g++ ­Wall ­g ­std=c++0x myprogram.cpp
Fair warning: if the computer you are running on is busy with lots of work (such as a full server or you
playing games in the background), it could cause your program to take a long time to finish. It will also
make your statistics seem strange since they’ll be highly variable. Consider using your own computer
for final tests, or run when few people are busy on the various EECS servers (ssh1, ssh2, ssh3, ssh4).
Statistics
Run the do_bubblesort function many times, keeping the size of each sort and how long it took. These
results should be kept in a data structure. For each size N we sample for, run it 5 times and average
the results. Keep both the average and the individual runs for each size N to be outputted in your CSV
file.
We will need to run this for each size N: [10, 50, 100, 500, 1000, 5000, 10000, 50000, 100000]
Additionally, for each size N, we will gather the optimal run time and the worst case run time. In these
cases, the do_bubblesort function needs to not generate random arrays, but pre­sorted arrays. For
the optimal case test, the array should be pre­sorted before bubblesort runs on it. For the worst case,
it should be in reverse order. Each of these should be run 5 times and averaged. Only the final
averages should be kept for the output to the CSV file.
The results will need to be output in a single CSV format file. The file will have 9 columns:
Expected Output
Your program should generate one CSV file with the gathered statistics, called BSStats.csv, which
includes the statistics of running on random lists for the various size N values, along with their best
and worst case timings as well.
Based on that CSV file, which you can open in MS Excel, LibreOffice Calc, or Google Docs Sheets,
create a chart plotting your calculated times for sorting the various lists: Sort time vs. N size. Include
for each size N the average times of: Optimal (pre­sorted), Worst case (invert sorted), and Average
(randomly created). The chart needs to be exported to an image file (png), either via a screenshot or
other means. The chart should be named:
● OptimalWorstAverageCasePlot.png (the optimal, worst, and average case results)
Deliverables
You must upload your program through Blackboard no later than midnight on Friday, September 23,
2016. The program will be uploaded as a zip file containing:
● C++ source code
● The chart as and image (OptimalWorstAverageCasePlot.png)
● The CSV file your program output (BSStats.csv)
Grading Criteria
Your assignment will be judged by the following criteria:
● [70] Code operational success. Your code compiles, executes, and generates the CSV files.
● [10] Your code is well documented and generally easy to read.
● [10] Your program intelligently uses classes when appropriate and generally conforms to good
OOP design (i.e. everything isn’t slapped into main).
● [10] The CSV and chart in the correct format, with labeled axes, title, and legend (as
appropriate)


