# Student-Circles
Finds the least cost student circle of size 3 using gradient descent

### Problem Statement
The course staff of a certain Computer Science course randomly assigns students to teams for their rst
assignment of the semester to help force people to get used to the real-world situation of working on
diverse groups of teams of programmers. But since they are not completely heartless, the instructors
allow students to give preferences on their teams for future assignments. In particular, each student is
sent an electronic survey and asked to give answers to four questions:

(a) What is your user ID?  
(b) Would you prefer to work alone, in a team of two, in a team of three, or do you not have a
preference? Please enter 1, 2, 3, or 0, respectively.  
(c) Which student(s) would you prefer to work with? Please list their user IDs separated by commas,
or leave this box empty if you have no preference.  
(d) Which students would you prefer not to work with? Please list their IDs, separated by commas.

Assuming every student fills out the survey exactly once, ideally, student preferences would be
compatible with each other so that the group assignments would make everyone happy, but inevitably
this is not possible because of conflicting preferences. So instead, being selfish, the course staff would
like to choose the group assignments that minimize the total amount of work they'll have to do. They
estimate that:

* They need k minutes to grade each assignment, so total grading time is k times number of teams.
* Each student who requested a specific group size and was assigned to a dierent group size will
complain to the instructor after class, taking 1 minute of the instructor's time.
* Each student who is not assigned to someone they requested will send a complaint email, which
will take n minutes for the instructor to read and respond. If a student requested to work with
multiple people, then they will send a separate email for each person they were not assigned to.
* Each student who is assigned to someone they requested not to work with (in question 4 above)
will request a meeting with the instructor to complain, and each meeting will last m minutes. If
a student requested not to work with two specific students and is assigned to a group with both
of them, then they will request 2 meetings.

The total time spent by the course staff is equal to the sum of these components. Our goal is to write
a program to find an assignment of students to teams that minimizes the total amount of work the
course staf needs to do, subject to the constraint that no team may have more than 3 students.

For example, a sample input file might look like:

djcran 3 zehzhang,chen464 kapadia  
chen464 1 _ _  
fan6 0 chen464 djcran  
zehzhang 1 _ kapadia  
kapadia 3 zehzhang,fan6 djcran  
steflee 0 _ _  

To run the program enter the following line in your command prompt / terminal:

python3 assign.py \<input-file> \<k> \<m> \<n>
