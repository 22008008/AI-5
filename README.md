# Ex.No: 5 Logic Programming – Simple queries from facts and rules

NAME: SRI RANJANI PRIYA P
REGISTER NUMBER : 212222220049

# AIM:
To write a prolog program to find the answer of query.

# Algorithm:
Step 1: Start the program
Step 2: Convert the sentence into First order Logic
Step 3: Convert the sentence into Horn clause form
Step 4: Add rules and predicates in a program
Step 5: Pass the query to program.
Step 6: Prolog interpreter shows the output and return answer.
Step 8: Stop the program.

# Program:
# Task 1:
Construct the FOL representation for the following sentences
```
John likes all kinds of food.
Apples are food.
Chicken is a food.
Sue eats everything Bill eats.
Bill eats peanuts
Convert into clause form and Prove that John like Apple by using Prolog.
Program:
likes(john,X):-
food(X).
eats(bill,X):-
eats(sue,X).
eats(Y,X):-
food(X).
eats(bill,peanuts).
food(apple).
food(chicken).
food(peanuts).
```
# Output:
![image](https://github.com/user-attachments/assets/d7539a08-59b4-4c38-9794-d57dbd9b4e31)


# Task 2:
Consider the following facts and represent them in predicate form:
```
Steve likes easy courses.
Science courses are hard.
All the courses in Have fun department are easy
BK301 is Have fun department course.
Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”
Program:
likes(steve,X):-
easycourse(X).
hard(sciencecourse).
easycourse(X):-
course(X,dept(havefun)).
course(bk301,dept(havefun)).
```
# Output:
![image](https://github.com/user-attachments/assets/f72afece-95db-45df-9909-699b74b004c8)

# Task 3:
Consider the statement
“This is a crime for an American to sell weapons to hostile nations. The Nano , enemy of America has some missiles and its missiles were sold it by Colonal West who is an American”
Convert to Clause form and prove west is criminal by using Prolog.

# Program:
```
criminal(X):-
american(X),
weapon(Y),
hostile(Z),
sells(X,Y,Z).
weapon(Y):-
missile(Y).
hostile(Z):-
enemy(Z,X).
sells(west,Y,nano):-
missile(Y),
owns(nano,Y).
missile(m).
owns(nano,m).
enemy(nano,america).
american(west).
```
# Output:
![image](https://github.com/user-attachments/assets/f958fe3c-d034-4501-a0a7-77b37c76e096)


# Result:
Thus the prolog programs were executed successfully and the answer of query was found.
