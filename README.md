Student Grades Management Program
Overview (SECTION A)
This Python program allows users to input multiple students and their corresponding grades for different subjects. The program calculates each student's average grade and also computes the overall class average. The program runs in a loop, allowing the user to input as many students and grades as needed until the user decides to stop by typing "done".

Python 3.6 or higher (The code was written for Python 3.6, but it should work with any Python 3 version.)
PyCharm IDE (You can run the code using PyCharm.)
We start by creating an empty list called students to store all our student data.
The main loop of the program is a while True loop. This means it will keep running until we explicitly break out of it. Inside this loop:

We ask for a student's name. If the user types 'done', we break out of the loop, finishing student entry.
If a name is entered, we create a new empty list called grades for this student's grades.
We then enter another while True loop to collect grades for this student:

We ask for a grade input.
If the user types 'done', we break out of this inner loop, finishing grade entry for this student.
If a number is entered, we convert it to a float and check if it's between 0 and 100.
If the grade is valid, we add it to the grades list.
If there's an error (like entering text instead of a number), we catch the ValueError and ask for input again.


After collecting all grades for a student, we add a tuple of (name, grades) to our students list.


After we've finished entering all students and their grades, we check if we have any student data:

If we do, we print out each student's name, all their grades, and their average grade.
We calculate each student's average grade by summing their grades and dividing by the number of grades.


To calculate the overall class average:

We use a list comprehension to create a flat list of all grades from all students.
We sum all these grades and divide by the total number of grades to get the class average.

Finally, we print the class average.

Output example:
You can type 'done' at any point to stop entering student data.
Enter the name of a student (or 'done' to finish): Tlotlo
Enter a grade for Tlotlo (0 - 100), or 'done' to finish grades: 78
Enter a grade for Tlotlo (0 - 100), or 'done' to finish grades: done
Enter the name of a student (or 'done' to finish): Leo
Enter a grade for Leo (0 - 100), or 'done' to finish grades: 87
Enter a grade for Leo (0 - 100), or 'done' to finish grades: done
Enter the name of a student (or 'done' to finish): Gail
Enter a grade for Gail (0 - 100), or 'done' to finish grades: 90
Enter a grade for Gail (0 - 100), or 'done' to finish grades: done
Enter the name of a student (or 'done' to finish): done

Student Grades:
Tlotlo: [78.0] (Average: 78.00)
Leo: [87.0] (Average: 87.00)
Gail: [90.0] (Average: 90.00)

Class Average: 85.00


