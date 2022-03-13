# 🔁Sorting

Sorting is a C++ project that empirically verifies the upper bound
of various sorting algorithms, as well as gather performance data
on algorithms in the same Big-O class.

## Installation 

This project can be run in the commandline via g++, or by compiling in CLion using the CMakeLists.txt file with your chosen compiler. Below I will show you how to install g++.

First, check if g++ is installed.
```text
$ g++ --version
```
If it is not installed, install it.
```text
$ sudo apt-get install g++
```

## Usage
First, navigate to the project directory.
```text
$ cd FullFilePathHere
```
Next, compile all the relevant files using g++
```text
$ g++ src/main.cpp 
```
Run the program, this program takes __ command line arguments

```text
data/size100/100-60ascending_noDup.txt data/size100/100-random_20Dup.txt data/size100/100-random_40Dup.txt data/size1000/1000-60ascending_noDup.txt data/size1000/1000-random_20Dup.txt data/size1000/1000-random_40Dup.txt data/size10000/10000-60ascending_noDup.txt data/size10000/10000-random_20Dup.txt data/size10000/10000-random_40Dup.txt data/size50000/50000-60ascending_noDup.txt data/size50000/50000-random_20Dup.txt data/size50000/50000-random_40Dup.txt data/size100000/100000-60ascending_noDup.txt data/size100000/100000-random_20Dup.txt data/size100000/100000-random_40Dup.txt data/size500000/500000-60ascending_noDup.txt data/size500000/500000-random_20Dup.txt data/size500000/500000-random_40Dup.txt data/size1mil/60ascending_noDup.txt data/size1mil/ascending_noDup.txt data/size1mil/random_20Dup.txt data/size1mil/random_40Dup.txt data/size1mil/random_noDup.txt
```

## Dataset Generation
In order to test the efficiencies of each of the sorting algorithms, different datasets have been generated.
The datasets have been split into two categories, integer based and string based,
with 6 datasets each:
- a randomized dataset with 0% duplicates
- dataset with 0% duplicates in ascending order
- dataset with 0% duplicates with 60% already in sorted ascending
    - This was generated by placing the ascending elements in the first 60% of the list,
followed by the randomized elements
    - This will likely be changed in order to have a more even distribution
- randomized dataset with 20% duplicates
- randomized dataset with 40% duplicates

Each of these datasets were generated using a python script, src/main.py, which is included
in the repository, and are formatted as followed:
```
<number of elements>
<element 1>
<element 2>
...
```
In order to ease the generation of random sequences, the files containing the datasets
will be the same for both categories. The only difference being the way these elements will be stored, 
with either ints or string data types.

All datasets can be found in the data folder.


## Credits

This project was completed entirely by Zachary Suzuki and 
Daniel Ryan for CS3353, Fundamentals of Algorithms taught by Dr. Fontenot.

