Question 1
----------
R was developed by statisticians working at...

Answer:

University of Auckland

Question 2
----------
The definition of free software consists of four freedoms (freedoms 0 through 3). Which of the following is NOT one of the freedoms that are part of the definition? Select all that apply.

Answer:

The freedom to sell the software for any price.

The freedom to restrict access of source code for software

The freedom to redistribute copies so htat you can help your neighbour.

Question 3
-----------------
In R the following are all atomic data types EXCEPT: (Select all that apply)

Answer:

List

Array

Data fram

table

Question 4
---------------
If I execute the expression x <- 4L in R, what is the class of the object `x' as determined by the `class()' function?

Answer:

Integar

Question 5
-------------
What is the class of the object defined by the expression x <- c(4, "a", TRUE)?

Answer:

logical

Question 6
------------------
If I have two vectors x <- c(1,3, 5) and y <- c(3, 2, 10), what is produced by the expression rbind(x, y)?

Answer:

1 3 5
3 2 10
A matrix with 2 rows and 3 columns

Question 7
----------
A key property of vectors in R is that

Answer:

Elements of vector has same class.

Question 8
-------------

Suppose I have a list defined as x <- list(2, "a", "b", TRUE). What does x[[2]] give me? Select all that apply.

Answer:

A character vector containing letter"a".

A character vector of lenght 1

Question 9
----------
Suppose I have a vector x <- 1:4 and a vector y <- 2. What is produced by the expression x + y?

Answer:

A integar vector with elements 3, 2,3, 4

Question 10
------------

Suppose I have a vector x <- c(17, 14, 4, 5, 13, 12, 10) and I want to set all elements of this vector that are greater than 10 to be equal to 4. What R code achieves this? Select all that apply.

Answer:

x[x>10]<-4
x[x>=11]<-4

Question 11
----------------

Use the Week 1 Quiz Data Set to answer questions 11-20.

In the dataset provided for this Quiz, what are the column names of the dataset?

Answer:

Ozone, Solor R., Wind, Temp, Month , day

Question 12
--------------

Extract the first 2 rows of the data frame and print them to the console. What does the output look like?

Answer:

41	190	7.4	67	5	1
36	118	8  	72	5	2

 First two rows 
quiz_data[c(1,2)]

Question 13
------------

How many observations (i.e. rows) are in this data frame?

Answer:

153

nrows(quiz_data)

Question 14
------------

Question 14
Extract the last 2 rows of the data frame and print them to the console. What does the output look like?

Answer:

    Ozone Solar.R Wind Temp Month Day
152    18     131  8.0   76     9  29
153    20     223 11.5   68     9  30

 tail(quiz_data, 2)

Question 15
------------

What is the value of Ozone in the 47th row?

Answer:

21

hw1_data(47, Ozone)

Question16
-------------

How many missing values are in the Ozone column of this data frame?

Answer:

37

# Going back to data.frame because dont it hasnt been taught yet in this specialization
hw1 = read.csv('hw1_data.csv')

sub = subset(quiz_data, is.na(Ozone))

nrow(sub)

Question17
-----------

What is the mean of the Ozone column in this dataset? Exclude missing values (coded as NA) from this calculation.

Answer:
42.1

hw1 = read.csv('hw1_data.csv')
sub = subset(hw1, !is.na(Ozone), select = Ozone)
apply(sub, 2, mean) 

Question 18
-------------

Extract the subset of rows of the data frame where Ozone values are above 31 and Temp values are above 90. What is the mean of Solar.R in this subset?

Answer:

212.8

quiz_data = read.csv('hw1_data.csv')

sub = subset(quiz_data, Ozone > 31 & Temp > 90, select = Solar.R)

apply(sub, 2, mean)

Question 19
------------

What is the mean of "Temp" when "Month" is equal to 6?

Answer:

79.1

quiz_data = read.csv('hw1_data.csv')

sub = subset(hw1, Month == 6, select = Temp)

apply(sub, 2, mean)

Question 20
------------
Question 20
What was the maximum ozone value in the month of May (i.e. Month is equal to 5)?

Answer:

115

Explaination

quiz_data = read.csv('hw1_data.csv')

sub = subset(quiz_data, Month == 5 & !is.na(Ozone), select = Ozone)

apply(sub, 2, max)












