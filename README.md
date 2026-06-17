Welcome to my CS 300 (Analysis and Design) portfolio project. This repository contains the command line Course Planner application built for the academic advisors at ABCU.
The application reads a comma-separated text file of courses and loads them into a custom-built Binary Search Tree (BST) data structure. This allows advisors to view a sorted, alphanumeric list of all courses and look up specific course titles and prerequisites instantly.

**Features**

**Load Course Data:** Reads a comma separated values (CSV) text file into memory.
**Alphanumeric Sorting:** Displays all loaded courses sorted alphabetically by course number (using In Order traversal).
**Course Search:** Instantly look up any course to see its official title and prerequisites.
**Input Validation:** Prevents application crashes if users input incorrect menu commands or if courses contain missing prerequisites.

**Data Structure Choice**

For this project, I designed and implemented a Binary Search Tree (BST).

**Why a BST?**

Efficient Sorting: A BST automatically keeps courses sorted as they are loaded. By using an In Order Traversal (Left Root Right), the program prints the entire course list in alphabetical order without needing extra sorting steps.
Fast Searches: Searching for a specific course (such as CSCI400) runs in $O(\log N)$ average time, making lookups much faster than searching through a standard linear list or array.

**How to Compile and Run**

This program is written in standard C++11 and does not require any external dependencies or custom parser headers.

**Step 1: Compile the Code**

Open your terminal or command prompt and run:
sh
g++ -std=c++11 ProjectTwo.cpp -o CoursePlanner

**Step 2: Run the Executable**

Run the program from your terminal:
sh
./CoursePlanner

**Step 3: Load Data**

When you run the program, choose Option 1 and enter the name of your course data file (e.g., ABCU_Advising_Program_Input.txt).

**Code Structure**

ProjectTwo.cpp: Contains the entire program, including the custom structures, BST class methods, file parsing utilities, and the user interface menu.

-struct Course: Holds the course ID, title, and a list of prerequisite IDs.

-struct Node: Represents a single node in the tree holding a Course.

-class BinarySearchTree: Handles insertion, searching, sorting, and memory cleanup.
