# Algorithms-Chapter1
Studio: Analyzing Algorithms

1. Given the un-reduced big-O value, calculate the reduced value.

a. 10               = O(1)
b. 10n              = O(n)
c. 5n2 + 2n         = O(n^2)
d. 3 log2n + 2      = O(log n)


2. For each of the following algorithms, calculate the big-O value. Be sure to specify which value n refers to.

a. Reversing a string

  reversed = ''
  for c in str:
     reversed = c + reversed
     
  = O(n) - (Where n is equal to the number of characters (c) in the string)
     
b. Printing out a matrix

  for row_idx in matrix.length:
   row = matrix[row_idx]
   for col_idx in row:
      print row[col_idx]  2n
      print " "
   print "\n"
   
   = n * (2n + 1) = 2n^2 + n = O(n^2) - (There is a nested loop with two operations, which results in the value of 2n.  The outer loop has one operation, 
   which results in n * (2n + 1), which multiplies out to 2n^2 + n.  The cancel rule removes the (+n) and the product rule reduce the 2n^2 to n^2.)
   
   
c. Reversing each string in an array

  Note: For this exercise, assume that each string has at most 10 characters.
  reversed_strings = []
  for str in strings:
   reversed = ''
   for c in str:
      reversed = c + reversed
   reversed_strings.append(reversed)
   
   = n * (n + 1) = n^2 + n = O(n^2) - (There is a nested loop with one operation, which results in the value of n.  The outer loop has one operation, 
   which results in n * (n + 1), which multiplies out to n^2 + n.  The cancel rule removes the (+n), which leaves the result O(n^2).)

3. Suppose you have an array of Customer objects, sorted in alphabetical order by last name. For each of the following tasks, determine the run time in terms of big-O.

a. Print the names of all of the customers.                                   = O(n) - (where n is equal to the number of customers)

b. Print the names of only the customers with last name starting with “A”.    = O(n^2) - (There is a nested loop with one operation, which results in the value of n.  
The outer loop does not have an operation, which results in n * (n), which is equal to O(n^2).)

c. Find all customers with last name beginning with “A”.                      = O(n^2) - (There is a nested loop with two operations, which results in the value of 2n.  
The outer loop does not have an operation, which results in n * (2n), which is equal to 2n^2. The product rule reduces the 2n^2 to O(n^2).)

d. Find all customers with first name beginning with “A”.                     = O(n^2) - (There is a nested loop with two operations, which results in the value of 2n.  
The outer loop has one operation, which results in n * (2n + 1), which multiplies out to 2n^2 + n. The cancel rule removes the (+n) and the product rule reduce the 2n^2 
O(n^2).)

4. Now suppose that you have a dictionary (or hash map) of customer objects, where the keys are letters and the values are arrays storing all customers with last name beginning with that letter. For example, if our dictionary is customers then customers["A"] is an array of all customers with last name ending with “A”. Within each array, the customer objects are not sorted in any way.

a. Print the names of all of the customers.                                = O(n^2) - (There is a nested loop with one operation, which results in the value of n.  
The outer loop does not have an operation, which results in n * (n), which is equal to O(n^2).)

b. Print the names of only the customers with last name starting with “A”. = O(n) - (where n is equal to the number of customers in array at Dictionary value A)

c. Find all customers with last name beginning with “A”.                   = O(n) - (where n is equal to the number of customers in array at Dictionary value A)

d. Find all customers with first name beginning with “A”.                  = O(n^2) - (There is a nested loop with two operations, which results in the value of 2n.  
The outer loop has one operation, which results in n * (2n + 1), which multiplies out to 2n^2 + n. The cancel rule removes the (+n) and the product rule reduce the 2n^2 
O(n^2).)
