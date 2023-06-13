# Chapter 1 Python Basics

To **add comments** to your Python script, you can use the **# tag**. 

Python is perfectly suited to do basic calculations. It can do addition, subtraction, multiplication and division, and there is also support for more advanced operations such as:
- Exponentiation: **. This operator raises the number to its left to the power of the number to its right. For example 3**4 is 3 to the power of 4 and will give 81.
- Modulo: %. This operator returns the remainder of the division of the number to the left by the number on its right. For example 18 % 7 equals 4 because 7 fits into 18 twice (7 x 2 = 14), leaving you with a remainder of 4 (18 - 14 = 4).
- Remember, **= in Python means assignment**, it doesn't test equality!

**Types**:
- To see the type of our bmi value, simply write type and then bmi inside parentheses: **type(bmi)**;
- **float**, which is python's way of representing a real number, so a number which can have both an integer part and a fractional part: 2.598;
- Python also has a type for **integers**: int, like this example 8;
- A **string** is Python's way to represent text. You can use both double and single quotes to build a string, as you can see from these examples;
-  The **Boolean** is a type that can either be True or False. You can think of it as 'Yes' and 'No' in everyday language. Booleans will be very useful in the future, to perform filtering operations on your data for example.
- o do this, you'll need to explicitly convert the types of your variables so that they are all strings. More specifically, you'll need str(), to convert a value into a string. str(savings), for example, will convert the integer savings to a string.
- Similar functions such as int(), float() and bool() will help you convert Python values into any type.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Chapter 2 Python Lists

**Lists**:
- a list is a **compound data type** so you can group values together;
- name of the collection of values;
- contain any type;
- content differnt types;
- contain lists as well;
- e.g.[1.23, 5.65, 8.99];
- fam = [["liz", 1.86], 
    ["mom", 1.65],
    ["dad", 1.95]]
- type(fam) = list !!

# Subsetting Lists

Subsetting Lists:
- zero-indexing;
- slicing [start:end](inclusive; exclusive)
-fam =  ['liz', 1.73, 'emma', 1.68, 'mom', 1.71, 'dad', 1.89]; fam[0]
- fam[-1] => the last element
- fam[:4] => inclusive
- Selecting single values from a list is just one part of the story. It's also possible to slice your list, which means selecting multiple elements from your list. Use the following syntax:
-my_list[start:end]    !The start index will be included, while the end index is not.
- However, it's also possible not to specify these indexes. If you don't specify the begin index, Python figures out that you want to start your slice at the beginning of your list. If you don't specify the end index, the slice will go all the way to the last element of your list. To experiment with this, try the following commands in the IPython Shell;
- fam_ext = fam + ["me", 1.79]del(fam[2])fam['lisa', 1.74, 1.68, 'mom', 1.71, 'dad', 1.86]
- Replacing list elements is pretty easy. Simply subset the list and assign new values to the subset. You can select single elements or you can change entire list slices at once.
- If you can change elements in a list, you sure want to be able to add elements to it, right? You can use the + operator:
- The ; sign is used to place commands on the same line. The following two code chunks are equivalent:
- Same line: command1; command2
- If you want to prevent changes in areas_copy from also taking effect in areas, you'll have to do a more explicit copy of the areas list. You can do this with list() or by using [:].
- **Create list areas**
    - areas = [11.25, 18.0, 20.0, 10.75, 9.50]
-  **Create areas_copy**
    - areas_copy = list(areas[:])
- **Change areas_copy**
    - areas_copy[0] = 5.0
- **Print areas**
    print(areas)

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Chapter 3 Functions and packages