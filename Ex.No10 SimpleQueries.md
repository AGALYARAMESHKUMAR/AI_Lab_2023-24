# Ex.No: 10 Logic Programming – Simple queries from facts and rules
# DATE:
# REGISTER NUMBER : 212222040003
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

1. John likes all kinds of food.
2. Apples are food.
3. Chicken is a food.
4. Sue eats everything Bill eats.
5. Bill eats peanuts
6. Convert into clause form and Prove that John like Apple by using Prolog.
# Program:
```
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
![image](https://github.com/AGALYARAMESHKUMAR/AI_Lab_2023-24/assets/119394395/c708a5cb-b396-4e0a-b094-79f73e38033c)


# Task 2:
Consider the following facts and represent them in predicate form:

1. Steve likes easy courses.
2. Science courses are hard.
3. All the courses in Have fun department are easy
4. BK301 is Have fun department course.
5. Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”
# Program:
```
likes(steve,X):-
 easycourse(X).
hard(sciencecourse).
easycourse(X):-
 course(X,dept(havefun)).
course(bk301,dept(havefun)).
```
# Output:
![image](https://github.com/AGALYARAMESHKUMAR/AI_Lab_2023-24/assets/119394395/c1baa521-cef1-4536-9a71-167d6a9b91c7)


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
![image](https://github.com/AGALYARAMESHKUMAR/AI_Lab_2023-24/assets/119394395/5a428d28-b221-4cfd-9a8e-46275188177f)


# Result:
Thus the prolog programs were executed successfully and the answer of query was found.
